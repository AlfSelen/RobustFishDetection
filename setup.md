# Setup

1. Create new environment, activate it, and prepare ipykernel
python -m venv myenv
myenv/scripts/activate.ps1
pip install ipykernel jupyterlab
2. Install the environment with jupyter compability
python -m ipykernel install --name=myenv --user
3. Install pytorch with cuda support
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
4. Install rest of requirements
pip install -r requirements.txt

# Perform these steps if there requirements doesn't get installed
pip install protobuf https://github.com/protocolbuffers/protobuf/releases
pip install cython
pip install --use-pep517 super-gradients
pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI

# Troubleshooting jupyter, this command shows which environments that are installed with jupytyer
jupyter kernelspec list 