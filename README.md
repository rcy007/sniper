# Sniper
Net Worth and Investing

## Setup

Pre-requisites:

-[conda (Miniconda)](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html)
-[autoenv](https://github.com/hyperupcall/autoenv)

```sh
git clone https://github.com/rcy007/sniper.git

cd sniper

# conda create -n sniper-dev-env python=3.12

```

If installed autoenv via Homebrew on Mac then edit:
/opt/homebrew/opt/autoenv/activate.sh

```sh
sed -i '' '1s/^/AUTOENV_ENABLE_LEAVE=1\
AUTOENV_ASSUME_YES=1\
/' /opt/homebrew/opt/autoenv/activate.sh
```

This above code coupled with our .env and .env.leave files will make sure we always activate our dev conda environment
whenever we are in our project directory, and exit to our base environment whenever we leave it.

[Bug]: Works while CD ing into sub-directories directly from root, but does not exit the dev conda if we CD out of a sub-directory.

```sh
conda env create -f dev-conda-env.yml

conda activate sniper-dev-env

npm install -g ts-node

# npm install -g npm@10.9.0 # Not sure
```
