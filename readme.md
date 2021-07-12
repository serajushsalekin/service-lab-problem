# Summery
> The problem is there is two localhost, so we have to create a network to solve this problem.

## create docker network
```
docker network create my_micro_service
```
## run external app:
```
cd external/
docker build -t external-app .
docker run -d --rm --net my_micro_service --name external -p 8081:8081 external-app
```
## run internal app:
```
cd internal
docker build -t internal-app .
docker run -d --rm --net my_micro_service --name internal -p 8080:8080 internal-app
```