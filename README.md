# Bank-Note-Authentication

## Table of Content
  * [Demo snapshot](#demo)
  * [Overview](#overview)
  * [Motivation](#motivation)
  * [Technical Aspect](#technical-aspect)
  * [ Docker Installation](#installation)
  * [Directory Tree](#directory-tree)
  * [Technologies Used](#technologies-used)
  * [License](#license)
  * [Credits](#credits)
  
## Demo
Link: [http://localhost:8000/apidocs/](http://localhost:8000/apidocs/)

[![](https://github.com/Engwabel/Bank-Note-Authentication/blob/main/flasgger%20app.png)](http://localhost:8000/apidocs/)

Link: [http://localhost:8501/](http://localhost:8501/)

[![](https://github.com/Engwabel/Bank-Note-Authentication/blob/main/streamlit%20snapshot.png)](http://localhost:8501/)


## Overview
Bank Note Authentication
Data were extracted from images that were taken from genuine and forged banknote-like specimens. For digitization, an industrial camera usually used for print inspection was used. The final images have 400x 400 pixels. Due to the object lens and distance to the investigated object gray-scale pictures with a resolution of about 660 dpi were gained. Wavelet Transform tool were used to extract features from images.
Dataset Link: https://www.kaggle.com/ritesaluja/bank-note-authentication-uci-data

This is a simple classification Flask app trained on a RandomForest Classifier .The trained model is implemented using Flask and Dockers then deployed with Flasgger and Streamlit.


## Motivation
Developing apps today requires so much more than writing code. Multiple languages, frameworks, architectures, and discontinuous interfaces between tools for each lifecycle stage creates enormous complexity. Docker simplifies and accelerates your workflow, while giving developers the freedom to innovate with their choice of tools, application stacks, and deployment environments for each project.And that introduced me to containers which are a standardized unit of software that allows developers to isolate their app from its environment, solving the “it works on my machine” headache.You can lrean more about Dockers [this](https://www.docker.com/) amazing tool.

## Technical Aspect
This project is divided into three parts:
1. Training a machine learning model using random forest classifiers in scikit-learn.
2. Building and Implementing a Flask web app on Docker Desktop .
    - Write the __Docker File__ .
    - Build the __Docker Image__ .
    - Run __Money authentication app__ .
3. Building and hosting a Flask web app on Flasgger and Streamlit.
    - A user can enter the 4 features extracted from the money image and classify it as authntic[1] or forged[0] .
    - Imported __Swagger from flasgger__ to deploy and test the web app by entering features values or uploading a test file.
    - Used __Streamlit__ to deploy the flask app as a the front-end.
    

## Installation
The Code is written in Python 3.7. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```

## Directory Tree 
```
├── Model 
│   ├── BankNote_Authentication.csv,TestFile.csv(Data set)
│   ├── Training_model.ipynb
│   └── classifier.pkl 
│   
├── Docker  app container
│   ├── Docker file
├── requirements.txt
├── Flask app  
│   ├── flask_api.py (flasgger deployement)
│   └── app1.py (streamlit deployement)   
├── LICENSE
├── README.md

```

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://github.com/Engwabel/Bank-Note-Authentication/blob/main/1200px-Scikit_learn_logo_small.svg.png"width=200>](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html) 
[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) 
[<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) 
[<img target="_blank" src="https://github.com/Engwabel/Bank-Note-Authentication/blob/main/streamlit.png" width=200>](https://www.streamlit.io/) 

[<img target="_blank" src="https://github.com/Engwabel/Bank-Note-Authentication/blob/main/flasgger.png" width=270>](https://pypi.org/project/flasgger/0.5.4/) [<img target="_blank" src="https://github.com/Engwabel/Bank-Note-Authentication/blob/main/dockerhero.jpg" width=100>](https://www.docker.com/)

## License
[![Apache license](https://img.shields.io/badge/license-apache-blue?style=for-the-badge&logo=appveyor)](http://www.apache.org/licenses/LICENSE-2.0e)

Copyright 2020 

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits
- (https://github.com/krishnaik06),(https://youtu.be/ipFUANeStYE) - This project wouldn't have been possible without the beautiful explantation by Krish naik .
