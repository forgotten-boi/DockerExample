#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat

# FROM mcr.microsoft.com/dotnet/core/sdk:3.1-nanoserver-1903 AS build
FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build
EXPOSE  5000
WORKDIR /src
COPY ["NewApp.csproj", "./"]
RUN dotnet restore "./NewApp.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "NewApp.csproj"
 # -c Release -o /app/build
# RUN dotnet run "NewApp.csproj"
ENTRYPOINT ["dotnet", "run"]