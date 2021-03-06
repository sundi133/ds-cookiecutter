# Getting Started

- Get Data

  - If data exists on Local, copy it to the server with scp
    - If data sits on the cloud, download it inside the server
  - Optional: Copy SSH keys `scp -rp ~/.ssh user@remote-server:/tmp/.ssh`

- SSH into the Server

  - Pull a Docker Container from https://hub.docker.com/u/dushyantkhosla/

```
docker pull <image>
docker images
```

- Get the code for your project if it exists, or clone *this* repository

```
git clone git-url
# git clone https://github.com/dushyantkhosla/ds-cookiecutter.git ./project-01
```

- Start a Docker Container using the appropriate image, map ports and mirror directories

```
docker run -it -v $pwd:/home \
               -p 8080:8080 \
               -p 5000:5000 \
               -p 3128:3128 \
               your-docker-image
```

- *If Docker commands do not work, run `systemctl start docker` as root and try again*  
- Setting `alias docker='sudo docker'` in your `.bashrc` helps.

- Configure Git

```
git config --global http.proxy http://proxy-url:port
git config --global user.email 'you@domain.com'
git config --global user.name 'FirstName LastName'
```
