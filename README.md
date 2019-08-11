# Data-Science-test
Assignment for ALIZ

## 1.Basics

This contains two folder ` Flask_app` and `model_build`

### 1.1 model_build
The `model_build` folder contains `main.py` file which builds the logistic regression model using dataset stored in folder `Data` in root directory.
The model is succcessfully saved in `1.Basics\Flask_app\pklobjects\`

To build the logistic regression model just navigate to `1.Basics\model_build\` directory and run `python main.py`

### 1.2 Flask_app

The `Flask_app` folder contains the <b> Flask app </b> the deploys the already built model into production

#### To run the model locally
1) Create a virtual environment by installing all dependencies listed in `1.Basics\Flask_app\requirements.txt` file
2) Just navigate to `1.Basics\Flask_app\` directory and run `python main.py`
3) This will the flask app at http:\
4) This will the flask app at http://localhost:8000/ 
5) To change the port navigate to `1.Basics\Flask_app\main.py` and change port in `app.run(host='localhost', port=8000, debug=True)`

#### To deploy the model in Google Cloud
1) Download and put your gcloud JSON service key to `1.Basics\Flask_app\`
2) Navigate to `1.Basics\Flask_app\main.py ` and put the following command there `os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="<key.json>"` replace <key.json> to name your JSON service key file.
3) Navigate to `1.Basics\Flask_app\main.py` and change the command `app.run(host='localhost', port=8000, debug=True)` to `app.runt(debug=Fasle)`
4)Upload folder `1.Basics\Flask_app\` to your Gcloud console
5)Navigate to folder where your `app.yaml` file is and run `gcloud init` and then `gcloud app deploy`

 


  




