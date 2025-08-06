---
permalink: /projects/disney-bsdf/
title: "Disney BSDF Implementation in Monte Carlo Path Tracer"
excerpt: "Physically-based rendering with Disney principled BSDF in a Monte Carlo path tracer"
author_profile: true
layout: default
---

<div style="text-align: center; margin: 30px 0;">
  <img src="/images/projects/disney_bsdf/disney_bsdf.png" alt="Disney BSDF" style="max-width: 65%; height: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
</div>

<h1 style="font-size: 1.75rem; font-weight: 700;">Disney BSDF</h1>

## Project Overview
This project implements the **Disney principled BSDF** in a custom **Monte Carlo path tracer** ([Lajolla](https://github.com/BachiLi/lajolla_public)) for physically-based rendering. Inspired by production shaders in Blender, Unreal Engine, and Renderman, the Disney BSDF unifies several reflection and transmission lobes into a single flexible material model.

The implementation includes support for five core components:

- **Diffuse** — retroreflective scattering with optional subsurface approximation  
<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/disney_bsdf/disney_diffuse.png" style="max-width: 50%; border-radius: 8px;">
</div>
- **Metal** — Cook-Torrance microfacet model with anisotropic GGX distribution  
<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/disney_bsdf/disney_metal.png" style="max-width: 50%; border-radius: 8px;">
</div>
- **Clearcoat** — secondary specular layer with wide lobe  
<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/disney_bsdf/disney_clearcoat.png" style="max-width: 50%; border-radius: 8px;">
</div>
- **Glass** — rough dielectric reflection and transmission with Fresnel effects  
<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/disney_bsdf/disney_glass.png" style="max-width: 50%; border-radius: 8px;">
</div>
- **Sheen** — retroreflection lobe for cloth-like materials
<div style="text-align: center; margin: 30px 20px;">
  <img src="/images/projects/disney_bsdf/disney_sheen.png" style="max-width: 50%; border-radius: 8px;">
</div>

Each lobe supports **importance sampling**, **PDF evaluation**, and **physically-inspired parameterization**. These components are combined following the Disney 2015 shading model, with appropriate energy weights and inside-outside logic.
- [🔗 View GitHub Repo](https://github.com/mizoreto/lajolla-renderer) 

