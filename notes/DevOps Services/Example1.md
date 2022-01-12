Enabling service
```
gcloud services enable containerregistry.googleapis.com  
```
Initializing ProjectID
```
export PROJECT_ID=<PROJECT ID> # Replace this with your GCP Project
ID  
```
Getting Busybox
```
docker pull busybox  
docker images  
```

Creating code (using vim Dockerfile)
```
cat <<EOF >>Dockerfile  
from busybox:latest  
CMD ["date"]  
EOF
```

Building
```
docker build . -t mybusybox  
```

Tagging following GCP Container Registry convention
```
docker tag mybusybox gcr.io/$PROJECT_ID/mybusybox:latest  
```

Running
```
docker run gcr.io/$PROJECT_ID/mybusybox:latest  
```

Wiring credentials of GCP Container Registry with Docker
```
gcloud auth configure-docker  
```

Pushing image to container registry
```
docker push gcr.io/$PROJECT_ID/mybusybox:latest
```