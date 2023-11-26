FROM ubuntu:20.10

# Actualiza los repositorios a old-releases y elimina referencias a los repositorios de seguridad
RUN sed -i 's|http://archive.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list && \
    sed -i 's|http://security.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list

# Establece variables de entorno
ENV DEBIAN_FRONTEND=noninteractive


# Instala los paquetes necesarios para la compilación
RUN apt update
RUN apt install -y sudo
RUN sudo apt install -y git
RUN sudo apt install -y gcc
RUN sudo apt install -y libssl-dev
RUN sudo apt install -y autoconf
RUN sudo apt install -y make
RUN sudo apt install -y vim
RUN sudo apt install -y zlib1g-dev