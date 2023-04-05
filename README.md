# Memorization

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
