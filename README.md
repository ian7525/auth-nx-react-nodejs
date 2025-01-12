Node version: v20.18.1

Init project step:
1. npx create-nx-workspace@latest auth-nx-react-nodejs
2. cd auth-nx-react-nodejs to go into auth-nx-react-nodejs folder
3. npm i -D @nx/react
    npm i -D @nx/express
    npm i -D @nx/node
4. cd apps => go into apps folder
5. nx g @nx/react:application frontend => frontend
6. nx g @nx/express:application backend => backend
7. cd .., in auth-nx-react-nodejs folder, 
    mkdir libs
    mkdir tools
8. nx g @nx/js:library shared-types => create shared libs

Add docker for running mongoDB
1. Enable vt-d setting in BIOS
2. install WSL: wsl --install
3. Download and install Docker Desktop: https://docs.docker.com/desktop/setup/install/windows-install/
4. After install and re-start compouter, the docker should be running
    If there is a WSL error, "wsl --shutdown" in command and re-start Docker Desktop
5. If success, can check docker version
    docker --version: Docker version 27.4.0, build bde2b89
    docker-compose --version: Docker Compose version v2.31.0-desktop.2


How to run?
Only frontend: nx serve frontend
Only backend: nx serve backend
Frontend/Backend at the same time: nx run-many --target=serve --projects=frontend,backend
docker-compose: docker-compose up -d
