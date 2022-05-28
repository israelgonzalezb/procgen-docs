---
hide-toc: true
---

# Procgen Benchmark

## [Blog Post](https://openai.com/blog/procgen-benchmark/) [Paper](https://arxiv.org/abs/1912.01588)

16 simple-to-use procedurally-generated [gym](https://github.com/openai/gym) environments which provide a direct measure of how quickly a reinforcement learning agent learns generalizable skills.  The environments run at high speed (thousands of steps per second) on a single core.

We ran a competition in 2020 which used these environments to measure sample efficiency and generalization in RL. You can learn more [here](https://www.aicrowd.com/challenges/neurips-2020-procgen-competition).

```{figure} https://raw.githubusercontent.com/openai/procgen/master/screenshots/procgen.gif
   :alt: Procgen
```

**These environments are associated with the paper [Leveraging Procedural Generation to Benchmark Reinforcement Learning](https://cdn.openai.com/procgen.pdf) [^citation].  The code for running some experiments from the paper is in the [train-procgen](https://github.com/openai/train-procgen) repo.  For those familiar with the original [CoinRun environment](https://github.com/openai/coinrun), be sure to read the updated CoinRun description below as there have been subtle changes to the environment.**

Compared to [Gym Retro](https://github.com/openai/retro), these environments are:

* Faster: Gym Retro environments are already fast, but Procgen environments can run >4x faster.
* Randomized: Gym Retro environments are always the same, so you can memorize a sequence of actions that will get the highest reward.  Procgen environments are randomized so this is not possible.
* Customizable: If you install from source, you can perform experiments where you change the environments, or build your own environments.  The environment-specific code for each environment is often less than 300 lines.  This is almost impossible with Gym Retro.

**Supported platforms:**

- Windows 10
- macOS 10.14 (Mojave), 10.15 (Catalina)
- Linux (manylinux2010)

**Supported Pythons:**

- 3.7 64-bit
- 3.8 64-bit
- 3.9 64-bit
- 3.10 64-bit

**Supported CPUs:**

- Must have at least AVX

[citation]

Please cite using the following bibtex entry:

```
@article{cobbe2019procgen,
  title={Leveraging Procedural Generation to Benchmark Reinforcement Learning},
  author={Cobbe, Karl and Hesse, Christopher and Hilton, Jacob and Schulman, John},
  journal={arXiv preprint arXiv:1912.01588},
  year={2019}
}
```
