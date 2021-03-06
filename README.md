# YOUR_PROJECT_NAME

Welcome to the project template repository for the UBC Computer Vision group. Please follow the steps in the checklist below to archive this project. If you have trouble archiving the project (e.g. getting the pip requirements and the versions of your dependencies), please contact the SHIELD admin of our group. 

CHECKLIST:
- [x] Fork the latest version of this repository into your personal GitHub account. 
- [ ] In your forked repository, restructure your code using the folder system below. 
- [ ] Organize your code following this folder structure.
- [ ] Update this `README.md` file to suit your needs.
  - Feel free to add/remove sections in this `README.md` as long as it is easy for others to fully make use of this repo.

> **Warning: DO NOT use the Fork button on GitHub, it will make your repository public.** Instead, head over to GitHub and create an empty private repository. 
> 
> Suppose it has an identifier `https://github.com/USER_NAME/my_private_project.git` and now you can fork this repository into a private repository by entering the following commands.

~~~
MY_GIT_REPO=https://github.com/USER_NAME/my_private_project.git
git clone --bare https://github.com/zc-alexfan/cv_project.git
cd cv_project.git 
git push --mirror $MY_GIT_REPO
cd ..
rm -rf cv_project.git
git clone $MY_GIT_REPO
~~~


## Introduction

(Give a few sentences to tell us about your project.)

## Directory structure

The overall directory structure of your new project should look like as follows. You are welcome to add/remove folders or files, but make sure to keep the overall structure.

```
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── processed      <- Processed data such as the extracted features, bounding box proposals, etc.
│   └── raw            <- The original dataset obtained. 
│
├── trained_models     <- Trained model weights, e.g. created by `torch.save(model.state_dict(), ..)`.
│
├── scripts            <- Scripts such as for data preprocessing (e.g. `preprocess.py`)
│
├── notebooks          <- Jupyter notebooks for cool demos. 
│
├── reports            <- E.g. LaTeX files for a conference
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
└── src                <- Source code for use in this project.
```

**Note: all files in `data/processed` and `data/raw` should be symbolic links to the `/shield/datasets` directory. Please contact the SHIELD admin with write permission to store into this directory.**

## Benchmarking

This section stores the trained model(s) for this project and its benchmark performance. 

(For example, Object Detection):

source  | backbone | model | bs | lr  | lr_decay | mAP@0.5 | mAP@0.50:0.95
--------|--------|--------|:------:|:------:|:-------:|:------:|:------:
[LINK_TO_TRAINED_MODEL](URL-TO-TRAINED-MODEL) | Res-101 | faster r-cnn | 6 | 5e-3 | 70k,90k | 24.8 | 12.8


## Setup

This section shows how to setup this repository including installing requirements (including the software versions used), setting up the files to run this repository, etc. 

### Requirements

- Python X.X
- PyTorch X.X
- CUDA X.X

### Dependencies

Install all the Python dependencies using pip:

~~~
pip install -r requirements.txt
~~~

Install Ubuntu libraries with: 

~~~
apt-get install some-software
~~~

## Useful Features and/or Processed Data for Future Projects

This section mentions potential useful processed data or features that might be useful for future projects (e.g. bounding box proposals).

- `PATH/TO/FEATURES`: a description of what it is.

For example,

- `data/processed/proposals`, you could find the bounding box proposals used. 

## Training

This section provides instructions to training this model from scratch. 

For example,
~~~
python main.py --config-file configs/faster_rcnn_res101.yaml
~~~

## Evaluate

This section shows how to evaluate a trained model on a dataset to reproduce the benchmark performance. 

For example,
~~~
python main.py --config-file configs/faster_rcnn_res101.yaml --inference --resume $CHECKPOINT
~~~

## Contact and Reference

- For more information, please contact REPO-OWNER@cs.ubc.ca

~~~
@inproceedings{latex-citation-name,
    title={THE TITLE OF YOUR REPORT/PAPER},
    author={LAST NAME, FIRST NAME},
    booktitle={REPORT TYPE/CONFERENCE TYPE},
    year={20XX}
}
~~~
