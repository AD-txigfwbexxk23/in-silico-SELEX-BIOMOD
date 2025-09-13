# in-silico-SELEX-BIOMOD

Tools to generate/score RNA secondary structures for in-silico SELEX.  
Right now the repo **does not** bundle heavy installers (Miniconda/ViennaRNA) since it was giving me commit issues for being too large. I add the steps to downloading them here:

---

## Quick start & Setup

```bash
# 1) Clone the repository
git clone https://github.com/AD-txigfwbexxk23/in-silico-SELEX-BIOMOD.git
cd in-silico-SELEX-BIOMOD

# 2) Create a Python virtual environment
python3 -m venv .venv
source .venv/bin/activate

# 3) Install Python dependencies
pip install -r requirements.txt   # safe to skip if file doesn’t exist
# Or manually install basics:
pip install numpy pandas biopython matplotlib

# 4) Install ViennaRNA (provides RNAfold)

## Option A: Conda (recommended)
conda install -c bioconda viennarna

## Option B: macOS/Linux from source
tar -xvzf ViennaRNA-2.6.4.tar.gz
cd ViennaRNA-2.6.4
./configure --prefix=$HOME/viennaRNA
make
make install
export PATH=$HOME/viennaRNA/bin:$PATH   # add to PATH

## Option C: Precompiled binaries
# - macOS: download .pkg or .tar.gz from ViennaRNA releases
# - Windows: use .exe installer from ViennaRNA

# Verify ViennaRNA installed
RNAfold --version

# 5) (Optional) Install Miniconda if not available
bash Miniconda3-latest-MacOSX-arm64.sh
source ~/miniconda3/bin/activate

# 6) Run the main script
python Main.py
