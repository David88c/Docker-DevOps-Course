FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build
MAINTAINER David
WORKDIR /src
COPY . .
RUN dotnet restore
RUN dotnet publish -o /app


FROM mcr.microsoft.com/dotnet/aspnet:3.1
WORKDIR /app
EXPOSE 80
COPY --from=build /app .
ENTRYPOINT [ "dotnet", "dotnet-core-helloworld.dll"]

