# Memorization

## Create environment with conda 

`conda create --prefix /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune python=3.8`

## Activate environment

`conda activate /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune`

## Install PyTorch 2.0

`conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia`

## Install HuggingFace libraries

Do the following:

`conda install -c huggingface transformers`

`conda install -c conda-forge datasets`

`conda install pip`

`pip install evaluate`

Optional:

`pip install accelerate`

## Add environment to JupyterHub

`conda install ipykernel`

`python -m ipykernel install --user --name finetune --display-name="Finetune"`

If the above was done within JupyterHub, reload the page. If that doesn't work, restart your JupyterHub server.
