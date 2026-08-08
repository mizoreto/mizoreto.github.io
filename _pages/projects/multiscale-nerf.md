---
permalink: /projects/multiscale-nerf/
title: "Multiscale NeRF"
excerpt: "Scale-conditioned NeRF for mitigating aliasing in multiscale rendering"
author_profile: true
layout: default
---

<div style="text-align: center; margin: 30px 0;">
  <img src="/images/projects/multiscale_nerf/multiscaleNeRF.png" alt="Multiscale NeRF" style="max-width: 65%; height: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
</div>

<h1 style="font-size: 1.75rem; font-weight: 700;">Multiscale NeRF</h1>

## Project Overview

Neural Radiance Fields (NeRF) achieve strong performance in scene reconstruction and novel view synthesis, but exhibit aliasing artifacts when rendering at different spatial resolutions. Mip-NeRF addresses this by integrating positional encoding over a conical frustum instead of sampling along a single ray, enabling scale-aware rendering. But Mip-NeRF simultaneously changes both the sampling strategy and the feature representation, making it unclear whether the improvement comes from the integrated positional encoding itself or from the explicit availability of scale information.

This project investigates a simpler alternative: explicitly conditioning a vanilla NeRF network on the approximate pixel footprint at each sample point, while retaining the original NeRF architecture. The goal is to isolate the role of explicit scale information and evaluate whether it alone can mitigate aliasing effects.

- [📄 View Report (PDF)](/images/projects/multiscale_nerf/Report.pdf)


---

## Results

<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/multiscale_nerf/comparison1.png" alt="Qualitative comparison at 1/4 resolution" style="max-width: 100%; border-radius: 8px;">
  <p style="font-size: 0.9em; color: gray;">Qualitative comparison at 1/4 resolution on the lego scene.</p>
</div>

<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/multiscale_nerf/comparison2.png" alt="Qualitative comparison at 1/8 resolution" style="max-width: 100%; border-radius: 8px;">
  <p style="font-size: 0.9em; color: gray;">Qualitative comparison at 1/4 resolution on the ship scene.</p>
</div>

The scale-conditioned model (Ours w/ PE) consistently outperformed vanilla NeRF across scales and achieved competitive PSNR and SSIM relative to Mip-NeRF. While our model attained slightly higher average PSNR on both scenes, Mip-NeRF generally retained stronger SSIM and LPIPS performance.

<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/multiscale_nerf/results.png" alt="Multiscale NeRF Results" style="max-width: 100%; border-radius: 8px;">
</div>

<p style="font-size: 0.85em; font-style: italic; color: gray;">Note: Mip-NeRF was evaluated using the Nerfstudio implementation trained on the full-resolution single-scale Blender dataset, whereas our models were trained and evaluated under the multiscale setting. The comparison should therefore be interpreted as approximate rather than strictly controlled.</p>

---

## Discussion

These results suggest that explicit scale conditioning is a simple and effective inductive bias for multiscale neural rendering. It substantially improves over vanilla NeRF, but the remaining gap in SSIM and LPIPS suggests that Mip-NeRF’s integrated positional encoding contributes beyond scale information alone.

---

## Vanilla NeRF on Custom Scenes

<div style="text-align: center;">
  <video width="90%" controls preload="metadata" style="border-radius: 8px; margin: 20px 0;">
    <source src="/images/projects/multiscale_nerf/bear_statue.mp4" type="video/mp4">
    <p>Your browser does not support the video tag. <a href="/images/projects/multiscale_nerf/bear_statue.mp4" target="_blank">Click here to download the video</a></p>
  </video>
  <p style="font-size: 0.9em; color: gray;">Bear Statue</p>
</div>

<div style="text-align: center;">
  <video width="90%" controls preload="metadata" style="border-radius: 8px; margin: 20px 0;">
    <source src="/images/projects/multiscale_nerf/cse.mp4" type="video/mp4">
    <p>Your browser does not support the video tag. <a href="/images/projects/multiscale_nerf/cse.mp4" target="_blank">Click here to download the video</a></p>
  </video>
  <p style="font-size: 0.9em; color: gray;">CSE Building</p>
</div>

<div style="text-align: center;">
  <video width="90%" controls preload="metadata" style="border-radius: 8px; margin: 20px 0;">
    <source src="/images/projects/multiscale_nerf/chezbob.mp4" type="video/mp4">
    <p>Your browser does not support the video tag. <a href="/images/projects/multiscale_nerf/chezbob.mp4" target="_blank">Click here to download the video</a></p>
  </video>
  <p style="font-size: 0.9em; color: gray;">Chezbob Shelf</p>
</div>

<div style="text-align: center;">
  <video width="90%" controls preload="metadata" style="border-radius: 8px; margin: 20px 0;">
    <source src="/images/projects/multiscale_nerf/chezbob_close.mp4" type="video/mp4">
    <p>Your browser does not support the video tag. <a href="/images/projects/multiscale_nerf/chezbob_close.mp4" target="_blank">Click here to download the video</a></p>
  </video>
  <p style="font-size: 0.9em; color: gray;">Chezbob Close-up</p>
</div>

---
