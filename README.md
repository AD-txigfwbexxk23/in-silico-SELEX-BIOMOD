# in-silico-SELEX-BIOMOD

Tools to generate/score RNA secondary structures for in-silico SELEX.  
Right now the repo **does not** bundle heavy installers (Miniconda/ViennaRNA) since it was giving me commit issues for being too large. I add the steps to downloading them here:

## Quick start

```bash
# 1) Clone
git clone https://github.com/AD-txigfwbexxk23/in-silico-SELEX-BIOMOD.git
cd in-silico-SELEX-BIOMOD

# 2) Create a virtual env for Python
python3 -m venv .venv
source .venv/bin/activate

# 3) Install Python deps (if any later get added)
pip install -r requirements.txt   # safe to skip if file doesn’t exist

# 4) Install ViennaRNA so `RNAfold` is available on PATH (see below)

# 5) Run
python Main.py
