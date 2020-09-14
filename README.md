# SML Project1 Team 22
## Team Members
* [Yichao Xu - 1045184](https://github.com/FlashXu)
* [Xinglin Qiang - 1153086](https://github.com/qiangxinglin)
* [Shaohua Liu - 1150336](https://github.com/sliu15)

## [Kaggle Leaderboard](https://www.kaggle.com/c/comp90051-2020-sem2-proj1/leaderboard)
AUC Score: 0.92258

## Environment Setup

From Debian 9 scratch

System dependencies

- `glibc` ≥ 2.27 (add `deb http://ftp.debian.org/debian sid main` to /etc/apt/sources.list)
- `CUDA` ≥ 11.0
- `Python` ≥ 3.6

Python dependencies (recommend to manage the packages by Anaconda)

- `jupyterlab` latest
- `TensorFlow` 2.3.0
- `Pytorch` 1.3.1
- `GraphVite` 0.2.2 [Package Link](https://github.com/DeepGraphLearning/graphvite)

## Example Invocation

Run command:

`graphvite run my_config.yml`

Here's the config file that we used for the final submission where you can tune the hyper-parameters:

[`./my_config.yml`](https://github.com/qiangxinglin/COMP90051-Project1-Team22/blob/master/my_config.yml)

The graph embedding file (in pickle format) will be generated into the directory specified in the config file.

Then you can use the code in [`eval/evaluate.ipynb`](https://github.com/qiangxinglin/COMP90051-Project1-Team22/blob/master/eval/evaluate.ipynb) to generate the formatted probability CSV file for Kaggle submission.

## Scripts Roles

* `my_config.yml`  - Config settings for running GraphVite.
* `adj2edge.ipynb` - Transforming adjacent list form to edge list form. 
* `evaluate.ipynb` - Calculating AUC scores and Kaggle competition results.
* `split_dataset.ipynb` - Randomly splitting the raw data into 8:2 dataset, while generating fake edges in the 20% dataset.
* `eval.ipynb` - Making evaluation on the embeddings.
* `logistic_reg.ipynb` - Trying Logitic Regression based on the embeddings.
