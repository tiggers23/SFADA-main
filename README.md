# Source-Free Domain Adaptation with Unrestricted Source Hypothesis


This is a Pytorch implementation of "Source-Free Domain Adaptation with Unrestricted
Source Hypothesis".


## Install

`pip install -r requirements.txt`


## Data Preparation

Please download datasets: [Office-31](https://faculty.cc.gatech.edu/~judy/domainadapt/), [Office-Home](http://ai.bu.edu/visda-2017/), and [VisDA-C](http://ai.bu.edu/visda-2017/) to your home directory.

## Training
(1) Pre-train the source model on dataset office-31:

`python image_source.py --s 0 --gpu_id 0 --dset office --lr 1e-2
`

(2) Train the target model on dataset office-31:

`python main.py --s 0 --t 1 --gpu_id 0 --dset office --lr 3e-3 --T 3.0
`
