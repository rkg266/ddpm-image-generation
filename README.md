# ddpm-image-generation
Implementation of Denoising Diffusion Probabilistic Model (DDPM) for study purposes. 

## Requirements
- Python 3.10
- Packages Upgrade pip for installing latest tensorboard
  ```sh
  pip install -U pip setuptools
  pip install -r requirements.txt
- Download precalculated statistic for dataset: <br/>
  [cifar10.train.npz](https://drive.google.com/file/d/1YTvr4DULZcMe8NXwUZQ1Beu6S_0mv30Z/view?usp=sharing) <br/>
  Create folder `stats` for `cifar10.train.npz`. <br/>
  stats <br/>
  └── cifar10.train.npz
