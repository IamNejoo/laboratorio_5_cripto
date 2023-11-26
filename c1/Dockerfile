# Usar Ubuntu 14.10
FROM ubuntu:14.10

# Cambiar los repositorios a old-releases
RUN sed -i 's/http:\/\/archive.ubuntu.com\/ubuntu\//http:\/\/old-releases.ubuntu.com\/ubuntu\//g' /etc/apt/sources.list \
    && sed -i 's/http:\/\/security.ubuntu.com\/ubuntu\//http:\/\/old-releases.ubuntu.com\/ubuntu\//g' /etc/apt/sources.list

# Actualizar la lista de paquetes e instalar paquetes necesarios
RUN apt-get update && apt-get install -y sudo net-tools openssh-client

