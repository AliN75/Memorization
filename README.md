# Memorization

## Introduction

- Files that contain the word pre-processing are for generating the fine-tuning data
- fine-tuning: For fine-tuning a model
- generate_measurement_data: For using a model to generate text
- generate_metrics: For calculating the memorization metrics using the generated text
- analyze_metrics: For aggregating the metrics and analyzing the memorization effect
- plot-scatter: For creating the scatterplots for memorization vs perplexity
- agg_metrics_with_perplexity.csv: Our aggregated metrics results combined with perplexity

## Create environment with conda 

`conda create --prefix /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune python=3.8`

## Activate environment

`conda activate /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune`

## Install PyTorch 2.0

`conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia`

## Install scikit-learn

`conda install -c anaconda scikit-learn`

## Install nltk

`conda install -c conda-forge nltk`

## Install sentence-transformers

`conda install -c conda-forge sentence-transformers`

## Install HuggingFace libraries

Do the following:

`conda install -c huggingface transformers`

`conda install -c conda-forge datasets`

`conda install pip` and `pip install evaluate` (or `conda install -c anaconda evaluate` without the pip installation)

Optional:

`pip install accelerate`

Make sure to open python and try importing these libraries before going to the next steps. If you run into trouble when importing `evaluate` with this message: `ImportError: libssl.so.10: cannot open shared object file: No such file or directory`, then try `conda install tokenizers --force-reinstall` (or `conda update tokenizers`).

## Add environment to JupyterHub

`conda install ipykernel`

`python -m ipykernel install --prefix=/work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune --name finetune --display-name="Finetune"`

If the above was done within JupyterHub, reload the page. If that doesn't work, restart your JupyterHub server.
