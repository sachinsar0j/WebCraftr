# WebCraftr
#To Run Project

 1️⃣ Stop and Remove Existing Container 
Run: 
bash 
Copy 
Edit 
docker ps -a 
Find the image ID of the running container and replace <IMAGE_ID> in the command below: 
bash 
Copy 
Edit 
docker stop <IMAGE_ID> && docker rm <IMAGE_ID> 
2️⃣ Navigate to the Project Directory 
Go to your project folder: 
bash 
Copy 
Edit 
cd ~/project/VvvebJs 
3️⃣ Build the Docker Image 
Run: 
bash 
Copy 
Edit 
docker build -t page-builder:v1️ . 
export DOCKER_BUILDKIT=0 use this before  docker build for ERROR: BuildKit
4️⃣ Run the Container 
Run: 
bash 
Copy 
Edit 
docker run -d --name page-builder -p 8080:80 -v $(pwd):/var/www/html page-builder:v1️ 
docker run -d --name page-builder -p 8080:80 -v $(pwd):/var/www/html page-builder:v1 [corrected]
5️⃣ Open in Browser 
Go to: 
http://localhost:8080/editor.php
