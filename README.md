Django-notes-app Project
Clone the repository (example):
1.	git clone https://github.com/LondheShubham153/django-notes-app.git
2.	docker build -t notes-app . (build the Docker image)
3.	Generate a personal access token on Docker Hub and log in using the command line.
4.	docker tag notes-app:latest adityabhosale212223/notes-app:latest
docker tag <local_image_name>:<tag> <your_dockerhub_username>/<repository_name>:<tag>
5.	docker push <image_name_with_tag>
create namespace (namespace should be same everywhere)
create service (with port)
create deployment (with image name)
port forward : 
k port-forward service/note-app-service -n notes-app 8000:8000 --address=0.0.0.0
•	kubectl port-forward service/note-app-service -n notes-app → creates a temporary tunnel from your machine to the Service inside the notes-app (namespace you given).
•	8000:8000 → maps local port 8000 to the Service’s port 8000.
•	--address=0.0.0.0 localhost.
