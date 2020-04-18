cntrl+p > docker add to workspace.

docker build -t newapp:v1 .
docker images
docker run -it -rm -p 8080:80 newapp:v1

docker run -v ${pwd}:/src -p 5000:80 newapp:v1 
docker run -v ${pwd}:/src -e Development -p 5000:80 newapp:v1


 <!-- docker run -v ${PWD}:/app --workdir /app microsoft/dotnet:2.1-sdk dotnet new mvc --auth Individual -->