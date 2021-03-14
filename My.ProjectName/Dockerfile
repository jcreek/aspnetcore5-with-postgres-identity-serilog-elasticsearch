#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /src
COPY ["My.ProjectName/My.ProjectName.csproj", "My.ProjectName/"]
RUN dotnet restore "My.ProjectName/My.ProjectName.csproj"
COPY . .
WORKDIR "/src/My.ProjectName"
RUN dotnet build "My.ProjectName.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "My.ProjectName.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "My.ProjectName.dll"]