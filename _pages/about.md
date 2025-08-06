---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>
I'm a rising second-year Master's student in Computer Science at the University of California, San Diego, advised by Prof. [Tzu-Mao Li](https://cseweb.ucsd.edu/~tzli/). I received my B.S. degree in Computer Science, with a minor in Physics, from the University of Illinois Urbana-Champaign. I'm broadly interested in computer graphics as a way to reconstruct, simulate, and reinterpret the physical world through computation. My current focus lies in rendering, perception, and scalable graphics systems. I'm also interested in computer vision, XR, and robotics, especially where they intersect with graphics.

I'm always open to connecting and sharing ideas. Please feel free to reach out!

# Education
<div style="display: flex; align-items: center; margin-bottom: 1em;">
  <img src="images/educations/ucsd_logo.jpeg" width="60" style="margin-right: 30px;">
  <div>
    <strong>University of California, San Diego</strong><br>
    <span style="color: gray;">Sep 2024 – Jun 2026</span><br>
    M.S. in Computer Science, GPA: 3.97
  </div>
</div>

<div style="display: flex; align-items: center; margin-bottom: 1em;">
  <img src="images/educations/uiuc_logo.jpeg" width="60" style="margin-right: 30px;">
  <div>
    <strong>University of Illinois Urbana-Champaign</strong><br>
    <span style="color: gray;">Jan 2021 – May 2024</span><br>
    B.S. in Computer Science, minor in Physics, GPA: 3.95
  </div>
</div>

# Experience
<div style="display: flex; align-items: flex-start; margin-bottom: 1em;">
  <img src="images/industries/aws_logo.jpeg" width="60" style="margin-right: 30px;">
  <div>
    <strong>Amazon Web Services (AWS)</strong><br>
    <span style="color: gray;">Jun 2024 – Sep 2024 | Seattle, WA</span><br>
    Software Development Engineer Intern<br>
    <ul style="margin-top: 0.5em;">
      <li>Designed and built an automated benchmarking framework, reducing a 1-2 day manual setup process to a 2-3 minute one-command execution, saving significant engineering time.</li>
      <li>Developed a resource cleanup handler to simplify teardown of benchmarking environments, streamlining post-test workflows.</li>
      <li><strong>Technologies</strong>: Python, Lambda, Step Functions, CDK, EC2</li>
    </ul>
  </div>
</div>

<div style="display: flex; align-items: flex-start; margin-bottom: 1em;">
  <img src="images/industries/aws_logo.jpeg" width="60" style="margin-right: 30px;">
  <div>
    <strong>Amazon Web Services (AWS)</strong><br>
    <span style="color: gray;">Jun 2023 – Aug 2023 | Seattle, WA</span><br>
    Software Development Engineer Intern 
    <ul style="margin-top: 0.5em;">
      <li>Developed a diagnostic library for Network Load Balancers that resolved noisy mismatch issues in dependency auditing systems, cutting false positive rate by 80%.</li>
      <li>Implemented intelligent mismatch snapshot adjustment via Amazon S3 client APIs, enabling customizable time windows for more accurate and timely debugging.</li>
      <li><strong>Technologies</strong>: Python, Amazon S3, EC2, SQL</li>
    </ul>
  </div>
</div>

# Projects
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Physically-Based Rendering</div><img src='images/projects/disney_bsdf/disney_bsdf.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[Disney BSDF](#)** [C++, Monte Carlo, Path Tracing, BSDF]

Implemented the Disney principled BSDF in a Monte Carlo path tracer (Lajolla). Combined microfacet-based BRDFs with importance sampling to support a wide range of realistic materials, including metal, glass, clearcoat, and retroreflective fabrics.

- [🔗 View GitHub Repo](https://github.com/mizoreto/lajolla-renderer) 
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Open-Vocabulary 3D Scene Understanding</div><img src='images/projects/fmgs_optimization/relmap_comparisons.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[Keep your ARMS and LEGS: Assuaging VRAM and Training Speed constraints in Language Embedded 3D Gaussian Splats](#)** [3DGS, CLIP, DINO]

Modified the [FMGS](https://xingxingzuo.github.io/fmgs/) pipeline to reduce VRAM usage and training time in open-vocabulary 3D scene understanding. Our approach replaces MLP-based decoding of multi-resolution hash encodings with CNNs applied to rendered feature fields, achieving **37% faster training** and **24% lower memory usage** while maintaining accuracy on the LERF benchmark.

- [📄 View Report (PDF)](/images/projects/fmgs_optimization/Report.pdf)


</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Autonomous Driving Forecasting</div><img src='images/projects/trajectory_prediction/cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[Ego-Agent Trajectory Prediction in Argoverse 2](#)** [Python, PyTorch]

Built an [ADAPT](https://kuis-ai.github.io/adapt/)-inspired deep learning model for ego-agent trajectory prediction in a Kaggle competition using a modified Argoverse 2 dataset. The model captures temporal and social context through LSTM and attention modules, and generates long-horizon forecasts via coarse-to-fine endpoint conditioning.

- [🔗 View GitHub Repo](https://github.com/mizoreto/Autonoumous_Driving_Motion_Forecast) 
- [📄 View Report (PDF)](images/projects/trajectory_prediction/Report.pdf)

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">3D Platformer Game</div><img src='images/projects/crystal_quest/crystal_quest_cover.jpg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[Crystal Quest](#)** [Unreal Engine, Blueprint Visual Scripting]

Crystal Quest is a 3D platformer designed with a progression-driven level structure and intuitive visual guidance. Built in Unreal Engine using Blueprint, the game challenges players to navigate dynamic environments through stealth, timing, and light combat mechanics.
</div>
</div>


# Misc
I enjoy photography, hiking, playing pool and chess, and hanging out with my cat, Yuki😼. I also like watching movies and reading in my free time.

📸 My photography: [@mizoreto](https://www.instagram.com/mizoreto/)

🧶 My cat: [@_yukiiii_i](https://www.instagram.com/_yukiiii_i/)



<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).


# 🔥 News
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2016</div><img src='images/500x300.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Deep Residual Learning for Image Recognition](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Kaiming He**, Xiangyu Zhang, Shaoqing Ren, Jian Sun

[**Project**](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=DhtAFkwAAAAJ&citation_for_view=DhtAFkwAAAAJ:ALROH1vI_8AC) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
</div>
</div>

- [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020**

# 🎖 Honors and Awards
- *2021.10* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.09* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 

# 💬 Invited Talks
- *2021.06*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.03*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  \| [\[video\]](https://github.com/)

# 💻 Internships
- *2019.05 - 2020.02*, [Lorem](https://github.com/), China. -->