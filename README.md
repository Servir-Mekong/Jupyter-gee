# Jupyter-gee
Install GEE Jupyter Notebook

**1: Download and install ANACONDA [(Select 2.7 python and 64 bit for ML installation)](https://www.anaconda.com/download/#windows)**

NOTE: DO NOT CHECK ANYHTING UNDER THE ADVANCED OPTIONS TAB DURING INSTALL (This will destroy your ArcGIS Installation)

**2: Add Community package management system**

Start "Anaconda Prompt" with admin privileges
```
conda config --prepend channels conda-forge
```
//START HERE IF YOU HAVE ANACONDA INSTALLED

**3: Create GEE environment**
```
conda create -n gee python=2.7
conda activate gee
conda install jupyter
```

**4: Install GEE API**

[From GOOGLE EE PYTHON API SITE:](https://developers.google.com/earth-engine/python_install_manual)

```
pip install google-api-python-client
python -c "from oauth2client import crypt"
pip install earthengine-api
```
**5: GEE Authentication**
```
python
```
Test Authentication
```python 
import ee
ee.Initialize()
```
\\You might get an initialization error.  Exit from python using the ctrl-C command

Setup Authentication (Only needed if you received an error above)
```
earthengine authenticate
```
This will open a browser and prompt you to login to your google account once logged in, copy and paste the authorization code into your command prompt

Exit python once you have entered your key using the "ctrl-c" command

**6: Link a IPython kernel to the gee environment**
```
python -m ipykernel install --name gee --display-name "Python (gee)"
```
Deactivate gee environment
```
conda deactivate
```
**7: Install Common Libraries That are used with GEE**
```
conda install folium
conda install bokeh
conda install pandas
```

**8: Start Jupyter environment by running the command**

change directory to your notebook folder location
```
jupyter lab
```
