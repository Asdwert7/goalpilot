FROM mcr.microsoft.com/dotnet/sdk:10.0 AS build
WORKDIR /src
COPY GoalPilot.sln ./
COPY GoalPilot.Api/GoalPilot.Api.csproj GoalPilot.Api/
RUN dotnet restore
COPY . .
RUN dotnet publish GoalPilot.Api/GoalPilot.Api.csproj -c Release -o /app/publish --no-restore

FROM mcr.microsoft.com/dotnet/aspnet:10.0 AS runtime
WORKDIR /app
COPY --from=build /app/publish .
ENV ASPNETCORE_URLS=http://+:8080
EXPOSE 8080
ENTRYPOINT ["dotnet", "GoalPilot.Api.dll"]
