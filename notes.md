git clone https://github.com/eitanturok/hlb-CIFAR10.git
cd hlb-CIFAR10
git switch -c tinygrad

uv venv
source .venv/bin/activate
uv pip install -r requirements.txt
uv pip install -e ../tinygrad
uv pip install setuptools ninja

PYTHONPATH="../tinygrad" TINY_BACKEND=1 python main.py
