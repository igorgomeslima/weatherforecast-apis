#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /src
COPY ["WeatherForecast.Api.Https.csproj", "."]
RUN dotnet restore "./WeatherForecast.Api.Https.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "WeatherForecast.Api.Https.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "WeatherForecast.Api.Https.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .

# For DEMO purposes only, copying certificates into an image isn't recommended ➤ https://docs.microsoft.com/pt-br/aspnet/core/security/docker-compose-https?view=aspnetcore-5.0#certificates
ADD /__needs/user-secrets /root/.microsoft/usersecrets
COPY /__needs/certs/https/WeatherForecast.Api.Https.pfx /root/.aspnet/https/

#COPY WeatherForecast.Api.Https.pfx /root/.aspnet/https/ #from root folder of Dockerfile
#COPY /__needs/user-secrets/* /root/.microsoft/usersecrets

ENTRYPOINT ["dotnet", "WeatherForecast.Api.Https.dll"]