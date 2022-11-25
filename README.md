# Simple Chat App

This is a simple website that uses Web Sockets and is deployed to Google Cloud Run. 

## To Run in Cloud Shell

pip install -r requirements.txt

python -m uvicorn main:app


## To Build the Docker Image and Deploy using Cloud Shell

gcloud builds submit --tag=gcr.io/$GOOGLE_CLOUD_PROJECT/chat-app:v1.0 .

gcloud run deploy chat-app --image=gcr.io/$GOOGLE_CLOUD_PROJECT/chat-app:v1.0 --allow-unauthenticated --region=us-central1 --port=8000

__Notes:__ The above commands assume you are running in Google Cloud Shell. If not, create a variable `GOOGLE_CLOUD_PROJECT`, and set it to your project ID before running the commands. 

Make sure you change the port in cloud Shell to use 8000 (the default is 8080)
