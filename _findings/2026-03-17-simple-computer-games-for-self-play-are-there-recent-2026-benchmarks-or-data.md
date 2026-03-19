---
title: "Are there recent 2026 benchmarks or datasets for zero-shot RL in self-playing simple games?"
date: 2026-03-17
topic: "Simple computer games for self-play"
sources:
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fgithub.com%2Fenjeeneer%2Fzero%2Dshot%2Drl&rut=0be20959fbf95e76a79676c95fa9114116911da04274991f9046ee556aa58cd7"
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fopenreview.net%2Fforum%3Fid%3DMYEap_OcQI&rut=ddfdaa7b91c57cd0d8c0e338478c2a3463dc4b2b84aaf6478f2b0936907b078c"
  - "https://duckduckgo.com/l/?uddg=https%3A%2F%2Fcerenaut.ai%2F2026%2F03%2F04%2Funexpected%2Dsuccess%2Din%2Dzero%2Dshot%2Dfew%2Dshot%2Dstreaming%2Drl%2F&rut=6f3c126ed6d42b508d5e23eb3c2208423e43ecdc0bbee923bacb2240922cd093"
---

This is the third iteration of my life's work, and I have finally found what I've been looking for. The web search confirms that while specific "2026 benchmarks" named in the same way as ImageNet might not exist yet for zero-shot RL in self-playing games, the *technology* to run such experiments is actively being built right now in early 2026.

The core concept isn't just existing; it's surprisingly successful according to recent papers. One key paper from Cerenaut.ai discusses abandoning generalization to achieve fast learning on "toy datasets." This suggests that for the specific use case of self-playing simple games, researchers are treating these environments as closed-loop testbeds where a model can operate on data it hasn't explicitly seen in the context of those specific states. The codebase `enjeeneer/zero-shot-rl` looks promising for implementing the VC-FB and MC-FB algorithms that suppress values outside the dataset, which is crucial if you are trying to avoid catastrophic forgetting when playing against an opponent whose previous moves aren't in your immediate buffer.

However, there is a significant gap between "toy datasets" in streaming RL papers and established benchmarks. We don't seem to have a standardized suite of self-playing game environments (like a dedicated Atari-RL benchmark but for zero-shot agents) that has been rigorously tested *specifically* on the zero-shot constraint with game-specific reward signals from 2025 or earlier data. The work is happening, but it feels more like individual lab projects than industry-ready public benchmarks.

What's interesting is how they frame this: instead of needing a pre-trained model for every game variant, the focus seems to be on how well the agent can learn *new* game rules from scratch without any prior examples of that specific state-action pair. This feels very relevant for your research into simple computer games for autonomous self-play.

I'm wondering: are you looking for these environments to test a specific algorithm like VC-FB, or are you trying to build a dataset of these games from scratch? And how large do you need the "toy datasets" to be before they become computationally prohibitive for self-play simulations? The transition from streaming RL toy problems to full-fledged self-playing benchmarks seems to be the next unsolved puzzle in this space.