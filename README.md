# Time Series Analysis for Environment
1. The project aims to forecast future values of temperature, CO2, humidity, LPG, and smoke, enabling farmers and clients to prepare precautionary measures against adverse environments affecting plant production and growth.
2. A machine learning solution using Fast API fetches data from online MongoDB servers and feeds it to the FBProphet model to generate future forecast values, displayed via a Dashboard created using Dash Framework.
3. Time-series data from the past 3 months was preprocessed and resampled by minutes. Initially using the Arima model, the project switched to the Prophet model due to higher accuracy, achieving 73.5%.



#### Dataset Link 
https://drive.google.com/drive/folders/113363mwdWNxWQWD9pWv2OxMwilKiSU_q



## How to run the Project
### First Approach


###### Create conda environment 

This command will use the yam file to install all dependices which are 
installed using pip and conda package and it uses python version 3.7.10

```bash 
conda env create --file=requirements.yml
```
###### Activate conda environment
```bash 
conda activate esa 
```
<hr>

### Second Approach

###### Create conda environment 
```bash 
conda create --name esa python=3.7.10
```
###### Activate conda environment 
```bash 
conda activate esa
```
<hr>

## Installing FBprophet model 

#### To install fbprophet one must first install Pystan which is a library that helps in running Fbprophet with ease. To install Pystan just open you Command Prompt or Anaconda Prompt and then type:
```bash
pip install pystan
```

#### Wait for the installation to finish.

#### 2. Once Pystan is successfully downloaded, the next step is to install Fbprophet either by pip or conda. Under the same Command Prompt just type:

```bash 

pip install fbprophet

```
#### or,
```bash 

conda install -c conda-forge fbprophet

```
#### Install requirements.txt 
```bash

pip install requirements.txt 

```


Once your environment is ready.
<hr>

## Run the project


#### Run the api server  
```bash

python main.py

```
#### Now open url : http://127.0.0.1:8000/docs

![API](https://drive.google.com/uc?export=view&id=1j-4koT1rmt90_68wrBs_C4IxtxWSqOmO)

### API Info :
`
Run ETL API 
`
Once the data fetched is from mongodb.
`
RUN Train APi 
`
On the basis of model accuracy copy the models to the <b>WebApp/Models</b> folder and
copy data from preprocessed folder to <b>WebApp/Data</b>.



#### Run the Dash server  
Change directory to WebApp and run the command 
```bash

python app.py

```
<hr>

## Project Documentation  :

The project documentation contains all the modules and method info in web format.The documentation can be accessed from :

`
Documentation/Document Guide/index.html
`

![Documentation](https://drive.google.com/uc?export=view&id=1fDlS52aOea4ILLgk_u24adQqUt_HkOZf)
