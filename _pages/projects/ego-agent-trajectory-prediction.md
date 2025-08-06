---
permalink: /projects/ego-agent-trajectory-prediction/
title: "Ego-Agent Trajectory Prediction in Argoverse 2"
excerpt: "Deep learning model for autonomous driving trajectory forecasting"
author_profile: true
layout: default
---

<div style="text-align: center; margin: 30px 0;">
  <img src="/images/projects/trajectory_prediction_cover.png" alt="Ego-Agent Trajectory Prediction" style="max-width: 65%; height: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
</div>

<h1 style="font-size: 1.75rem; font-weight: 700;">Ego-Agent Trajectory Prediction in Argoverse 2</h1>

## Project Overview

This project implements a deep learning model for forecasting the future motion of an ego vehicle in complex multi-agent driving scenarios. Built with PyTorch and trained on a modified version of the Argoverse 2 Motion Forecasting Dataset, the model was developed for a [Kaggle-hosted course challenge](https://www.kaggle.com/competitions/cse-251-b-2025).

Our model is inspired by the [ADAPT](https://kuis-ai.github.io/adapt/) architecture, and designed to handle long-horizon trajectory prediction by encoding temporal and social context. Specifically, we:

- Use bidirectional LSTM to encode past trajectories for all agents
- Apply multi-head self-attention to model agent-agent interactions
- Predict a coarse future endpoint, refine it, and condition trajectory generation on it
- Detach gradients between stages for training stability

We trained our model on agent-centric motion features: position (x, y), velocity (vx, vy), heading angle, and object type. **No map-based information (such as HD lanes, semantic raster, or traffic light states) was provided**, highlighting the model’s ability to perform under minimal context assumptions.

[🔗 View GitHub Repo](https://github.com/mizoreto/Autonoumous_Driving_Motion_Forecast)

[📄 View Report (PDF)](/images/projects/251B_Project_Final_Report.pdf)  

---

## Model Architecture

![Model Architecture](/images/projects/trajectory_prediction_architecture.png)

---

## Results
The model was evaluated using trajectory-level Mean Squared Error (MSE) between predicted and ground-truth ego-agent trajectories.

| Metric                 | Value   |
|------------------------|---------|
| Validation MSE         | 7.17    |
| Validation MAE         | 1.27    |
| Final Submission Score on Public Leaderboard | 7.23    |
| Final Submission Score on Private Leaderboard | 7.25   |
| Public Leaderboard Rank | **6th** |
| Private Leaderboard Rank | **7th** |

---
