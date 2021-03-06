# Welcome to the Cowrie Docker GitHub repository

This is the official repository for the Cowrie SSH and Telnet
Honeypot Docker effort. It contains Dockerfiles that you can use
to build [Cowrie](https://github.com/micheloosterhof/cowrie) Docker
images.

# What is Cowrie

Cowrie is a medium interaction SSH and Telnet honeypot designed to
log brute force attacks and the shell interaction performed by the
attacker.

# Configuring Cowrie in Docker

Cowrie in Docker is set up to use an 'etc' volume to store configuration
data.  Create ```cowrie.cfg``` inside the etc volume with the
following contents to enable Telnet in your Cowrie Honeypot in
Docker

```
[telnet]
enabled = yes
```

# docker-compose volumes

If you want to map local directories into the docker image, you need
to make sure that the direcories cowrie expects already exist, or it
will start failing in a never-ending loop.

```
mkdir -p var/log/cowrie var/run
```

# 
