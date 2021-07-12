
## run external app:
```
cd external/
docker build -t external-app .
docker run -p 8081:8081 external-app
```
## run internal app:
```
cd internal
docker build -t internal-app .
docker run -p 8080:8080 internal-app
```