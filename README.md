# Jupyter-gee
Install GEE Jupyter Notebook

**1: Download and install ANACONDA (Select 2.7 python and 64 bit for ML installation)**
https://www.anaconda.com/download/#windows

NOTE: DO NOT CHECK ANYHTING UNDER THE ADVANCED OPTIONS TAB DURING INSTALL (This will destroy your ArcGIS Installation)

**2: Add Community package management system**

Start "Anaconda Prompt" with admin privileges
```
conda config --add channels conda-forge
```
//START HERE IF YOU HAVE ANACONDA INSTALLED

**3: Create GEE environment**
```
conda create -n gee python=2.7
conda activate gee
conda install jupyter
```
From GOOGLE EE PYTHON API SITE: 
https://developers.google.com/earth-engine/python_install_manual


```
pip install google-api-python-client
python -c "from oauth2client import crypt"
pip install earthengine-api
python
```
**4: GEE Authentication**

Test Authentication
```python 
import ee
ee.Initialize()
```
\\You might get an initialization error.  Exit from python using the ctrl-C command

Setup Authentication
```
earthengine authenticate
```
This will open a browser and prompt you to login to your google account once logged in, copy and paste the authorization code into your command prompt
Link a IPython kernel to the gee environment
```
python -m ipykernel install --name gee --display-name "Python (gee)"
```
deactivate gee environment
```
conda deactivate
```
**4: Start Jupyter environment by running the command**
```
jupyter lab
```
