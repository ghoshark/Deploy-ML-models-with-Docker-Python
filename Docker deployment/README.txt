To build docker image -> docker build -t "flask_deployment_app" .

To run as a container -> docker run -d -p 8000:8000 flask_deployment_app

To list all containers -> docker container ls 
                          docker ps -a

To list all images -> docker image ls

To kill & remove a container -> docker kill <containerid> 
                                docker rm -v 540c78f8fb7d 

To remove all dangling images, containers, volumes etc -> docker system prune -a 
