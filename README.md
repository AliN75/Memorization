# Memorization

## Create environment with conda 

`conda create --prefix /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune python=3.8`

## Activate environment

`conda activate /work/pi_ahoumansadr_umass_edu/Memorization/envs/finetune`

## Install PyTorch 2.0

`conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia`

## Install HuggingFace

`conda install -c huggingface transformers`

## Install HuggingFace's datasets

`conda install -c conda-forge datasets`

## Install HuggingFace's evaluate

`conda install pip`
`pip install evaluate`

## Add environment to JupyterHub

`conda install ipykernel`

`python -m ipykernel install --user --name finetune --display-name="Finetune"`

If the above was done within JupyterHub, reload the page. If that doesn't work, restart your JupyterHub server.
