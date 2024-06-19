# ddpm-image-generation
Implementation of Denoising Diffusion Probabilistic Model (DDPM) for study purposes. 

## Requirements
- Dataset: CIFAR10
- Python 3.10
- Packages Upgrade pip for installing latest tensorboard
  ```sh
  pip install -U pip setuptools
  pip install -r requirements.txt
- Download precalculated statistic for dataset: <br/>
  [cifar10.train.npz](https://drive.google.com/file/d/1YTvr4DULZcMe8NXwUZQ1Beu6S_0mv30Z/view?usp=sharing) <br/>
  Create folder `stats` for `cifar10.train.npz`. <br/>
  ```sh
  stats 
  └── cifar10.train.npz

## Training
- Take CIFAR10 dataset to train.
  ```sh
  python main.py --train \
      --flagfile ./config/CIFAR10.txt
- [Optional] Overwrite arguments
  ```sh
  python main.py --train \
    --flagfile ./config/CIFAR10.txt \
    --batch_size 64 \
    --logdir ./path/to/logdir

## Evaluate
- A `flagfile.txt` is autosaved to your log directory. The default logdir for `config/CIFAR10.txt` is `./logs/DDPM_CIFAR10_EPS`
- Start evaluation
  ```sh
  python main.py \
    --flagfile ./logs/DDPM_CIFAR10_EPS/flagfile.txt \
    --notrain \
    --eval

