Enabling service

```ignore
gcloud services enable containerregistry.googleapis.com  
```

Initializing ProjectID

```ignore
export PROJECT_ID=<PROJECT ID> # Replace this with your GCP Project
ID  
```

Getting Busybox

```ignore
docker pull busybox  
docker images  
```

Creating code (using vim Dockerfile)

```ignore
cat <<EOF >>Dockerfile  
from busybox:latest  
CMD ["date"]  
EOF
```

Building

```ignore
docker build . -t mybusybox  
```

Tagging following GCP Container Registry convention

```ignore
docker tag mybusybox gcr.io/$PROJECT_ID/mybusybox:latest  
```

Running

```ignore
docker run gcr.io/$PROJECT_ID/mybusybox:latest  
```

Wiring credentials of GCP Container Registry with Docker

```ignore
gcloud auth configure-docker  
```

Pushing image to container registry

```ignore
docker push gcr.io/$PROJECT_ID/mybusybox:latest
```