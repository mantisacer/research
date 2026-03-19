---
title: "What are the latest 2026 open-source PPO or SAC algorithms with pre-trained policies for game playing?"
date: 2026-03-18
topic: "Simple computer games for self-play"
sources:
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fstable%2Dbaselines3.readthedocs.io%2Fen%2Fmaster%2Fmodules%2Fppo.html&rut=e125eff7b5ea3e673c95d7600377c7f8815c38da2f836144346d16e56522f8ca"
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fdocs.ray.io%2Fen%2Flatest%2Frllib%2Frllib%2Dalgorithms.html&rut=b8095f6568003195dfc58f2425f465aee50a8d1e209e25c229abdf4cf954b121"
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fgithub.com%2Fsebastianbrzustowicz%2FRobot%2DSumo%2DRL&rut=309711c6e71e84ea7935415281a482335c4480fa5e330ba580f58c67f596219f"
---

It's March 2026, and while I was hoping for some brand new "PPO-2026" or "SAC-Pro" models pre-trained on complex games, the actual frontier seems to be in how we bundle these classic algorithms into robust self-play frameworks. The big open-source players like Ray RLlib and Stable Baselines3 are still the engines of choice, but what's genuinely interesting this cycle is the emergence of specialized benchmarks that treat reinforcement learning seriously within game loops.

The most concrete lead I found was `Robot-Sumo-RL`. Published just months ago in January 2026, this repository positions itself as the state-of-the-art for autonomous robot combat using Sumo—a deceptively simple arena where a robot plays against others in real-time without human intervention. What stands out here is that it doesn't just implement PPO and SAC; it integrates them into a competitive self-play mechanism. That's exactly what you're looking for: games where the agent learns by playing itself over and over, refining its policy through trial and error rather than human supervision. It suggests that Sumo has finally reached a maturity level where we can reliably benchmark these algorithms against each other in a hostile environment.

Stable Baselines3 2.8.0a4 remains solid for PPO, offering the trust-region logic needed to stabilize updates when dealing with high-variance environments like fighting games. Similarly, Ray RLlib 2.54.0 is pushing boundaries with multi-node training, which is crucial if we ever want to scale this beyond simple two-player matches. However, as my memory from earlier queries recalls, we don't have a "2026 benchmark" suite quite yet like ImageNet; instead, the focus seems to be on these niche, self-contained environments where the game loop acts as the training ground itself.

The real opportunity here isn't necessarily finding a pre-trained policy for Chess or Go that beats humans immediately, but rather understanding which of these algorithms converges fastest in a zero-shot scenario against its own clones within Sumo. Are you more interested in the technical implementation details of how `Robot-Sumo-RL` achieves this self-play loop, or would you like to explore if there are other simple arena environments—maybe not combat focused—that allow for similar autonomous learning?