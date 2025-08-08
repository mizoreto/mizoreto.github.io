---
permalink: /projects/volumetric-path-tracing/
title: "Volumetric Path Tracing with Participating Media"
excerpt: "Monte Carlo path tracer supporting absorption, scattering, and heterogeneous volumes"
author_profile: true
layout: default
---

<div style="text-align: center; margin: 30px 0;">
  <img src="/images/projects/volumetric_path_tracing/smoke.png" alt="Volumetric Path Tracing" style="max-width: 65%; height: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
</div>

<h1 style="font-size: 1.75rem; font-weight: 700;">Volumetric Path Tracing</h1>

## Project Overview
This project implements a physically-based **volumetric path tracer** with support for **participating media**, including both **homogeneous** and **heterogeneous** volumes. The implementation is integrated into the [Lajolla](https://github.com/BachiLi/lajolla_public) renderer and follows the radiative transfer equation to simulate light absorption, scattering, and transmission through volumes.

- [🔗 View GitHub Repo](https://github.com/mizoreto/lajolla-renderer) 

The tracer supports:

- Absorption-only media (Beer-Lambert law)
- Single-scattering and multiple-scattering media
- Isotropic and Henyey-Greenstein phase functions
- Chromatic extinction and scattering coefficients
- Null-scattering acceleration (delta tracking) for heterogeneous media
- Next event estimation with multiple importance sampling (MIS)
- Interaction between surface BSDFs and volume effects

---

## Rendered Scenes

<div style="text-align: center; margin: 20px 0;">
  <img src="/images/projects/volumetric_path_tracing/spheres.png" style="max-width: 85%; border-radius: 6px;">
</div>

<div style="text-align: center; margin: 20px 0;">
  <img src="/images/projects/volumetric_path_tracing/cbox.png" style="max-width: 85%; border-radius: 6px;">
</div>

<div style="text-align: center; margin: 20px 0;">
  <img src="/images/projects/volumetric_path_tracing/cbox_teapot.png" style="max-width: 85%; border-radius: 6px;">
</div>

<div style="text-align: center; margin: 20px 0;">
  <img src="/images/projects/volumetric_path_tracing/smoke.png" style="max-width: 85%; border-radius: 6px;">
</div>

---

