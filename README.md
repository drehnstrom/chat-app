# chat-app

## To Run inCloud Shell

pip install -r requirements.txt

python -m uvicorn main:app


## To Create Docker Image with Cloud Build

gcloud builds submit --tag=gcr.io/$GOOGLE_CLOUD_PROJECT/chat-app:v1.0 .

gcloud run deploy chat-app --image=gcr.io/$GOOGLE_CLOUD_PROJECT/chat-app:v1.0 --allow-unauthenticated --region=us-central1 --port=8000
