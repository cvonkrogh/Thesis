# Thesis

## Quick-start (macOS · Python 3.11.5)

```bash
# 1 · clone the repo
git clone https://github.com/<your-user>/bachelor-thesis-group32.git
cd bachelor-thesis-group32

# 2 · create + activate a virtual-env  (keeps deps isolated)
python3 -m venv .venv
source .venv/bin/activate          # zsh/bash

# 3 · install libraries
pip install --upgrade pip
pip install -r requirements.txt

# 4 · drop any annual report into 0_data/
cp ~/Downloads/UniCredit.pdf 0_data/
