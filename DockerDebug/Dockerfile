FROM registry.angusido.com/aspnetcore-rdbg:latest
ARG source
WORKDIR /app
#exposes port 80 to linked services
EXPOSE 80

COPY . .

RUN mkdir ~/.ssh/
RUN mv /app/authorized_keys ~/.ssh/authorized_keys


ENTRYPOINT service ssh start && dotnet /app/bin/Debug/netcoreapp2.0/DockerDebug.dll && /bin/bash