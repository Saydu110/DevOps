FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY *.sln ./
COPY MyApp/*.csproj ./MyApp/
RUN dotnet restore
COPY . .
RUN dotnet publish -c Release -o /app MyApp

FROM mcr.microsoft.com/dotnet/aspnet:7.0
WORKDIR /app
COPY --from=build /app .
EXPOSE 80
ENTRYPOINT ["dotnet", "MyApp.dll"]
