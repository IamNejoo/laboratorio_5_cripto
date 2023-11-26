# Utiliza Ubuntu 20.10 como imagen base
FROM ubuntu:20.10

# Cambia los repositorios a old-releases y actualiza los paquetes
RUN sed -i 's|http://archive.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|' /etc/apt/sources.list && \
    sed -i 's|http://security.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y sudo net-tools openssh-client openssh-server tshark

# Configuración del usuario 'test'
RUN useradd -m test && \
    echo "test:test" | chpasswd && \
    adduser test sudo

# Crea el directorio necesario para SSH
RUN mkdir /run/sshd

# Expone el puerto 22 para SSH
EXPOSE 22

# Inicia el servidor SSH cuando el contenedor se ejecuta
CMD ["/usr/sbin/sshd", "-D"]
