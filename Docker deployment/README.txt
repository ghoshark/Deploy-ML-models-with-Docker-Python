To build docker image -> docker build -t "fastapi_deployment_app" .

To remove an image -> docker image rm <imageid>

To run as a container -> docker run -d -p 8000:5000 fastapi_deployment_app


To list all containers -> docker container ls 
                          docker ps -a

To list all images -> docker image ls

To kill & remove a container -> docker kill <container_id> 
                                docker rm -v 540c78f8fb7d 

To remove all dangling images, containers, volumes etc -> docker system prune -a 

Flask:

Web browser:
If running the docker container:
http://localhost:8000/apidocs/#/default/get_predict

or
If directly running the local server
http://localhost:5000/apidocs/#/default/get_predict


FastAPI:

Web browser:
http://localhost:8000/docs

pip install fastapi
pip install uvicorn
pip install python-multipart 

To run: (if running from command line with uvicorn)
uvicorn fastapi_predict_api:app --reload

Or
if __name__ == "__main__":
    uvicorn.run('fastapi_predict_api:app', host='0.0.0.0', port=5000)

python fastapi_predict_api.py
