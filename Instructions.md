1: Download and install ANACONDA
https://www.anaconda.com/download/#windows
*For windows users do not add to path

2: start Anaconda prompt in admin privilege 
conda config --add channels conda-forge (THIS IS A PACKAGE MANAGEMENT)

3: Create GEE environment
conda create -n gee python=2.7
conda activate gee
conda install jupyter
From GOOGLE EE PYTHON API SITE: 
https://developers.google.com/earth-engine/python_install_manual
pip install google-api-python-client
python -c "from oauth2client import crypt"
pip install earthengine-api
python 
import ee
ee.Initialize()
You might get an initialization error.  Exit from python using the ctrl-C command
earthengine authenticate
this will open a browser and prompt you to login to your google account once logged in, copy and paste the authorization code into your command prompt
Link a IPython kernel to the gee environment
python -m ipykernel install --name gee --display-name "Python (gee)"
didactive gee environment
conda deactivate
Start Juypiter environment by running the command
Jupyter lab
