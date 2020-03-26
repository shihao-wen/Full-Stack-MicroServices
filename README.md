# Full-Stack-MicroServices
Docker + Kubernetes + CI/CD

## Docker
```bash
docker run --rm --publish 8080:8080 -v $HOME/.aws:/root/.aws --env POSTGRESS_HOST=$POSTGRESS_HOST --env POSTGRESS_USERNAME=$POSTGRESS_USERNAME --env POSTGRESS_PASSWORD=$POSTGRESS_PASSWORD --env POSTGRESS_DB=$POSTGRESS_DB --env AWS_REGION=$AWS_REGION --env AWS_PROFILE=$AWS_PROFILE --env AWS_BUCKET=$AWS_BUCKET --env JWT_SECRET=$JWT_SECRET --name feed <your_dockerhub_username_lowercase>/udacity-restapi-feed
```
Publish to Dockerhub:
```bash
docker push yourdockerhubname/udacity-restapi-feed
docker push wenshihao1993/udacity-restapi-feed
```
Docker-compose:
```bash
docker-compose -f docker-compose-build.yaml build --parallel
docker-compose up
docker-compose up -d 
```
![DockerHub](/images/DockerHub.png)
After Verification: http://localhost:8100/
```bash
docker-compose stop
docker-compose down
```
