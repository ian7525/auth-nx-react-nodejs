Node version: v20.18.1

Init project step:
1. npx create-nx-workspace@latest auth-nx-react-nodejs
2. cd auth-nx-react-nodejs to go into auth-nx-react-nodejs folder
3. npm i -D @nx/react
    npm i -D @nx/expredd
    npm i -D @nx/node
4. cd apps => go into apps folder
5. nx g @nx/react:application frontend => frontend
6. nx g @nx/express:application backend => backend
7. cd .., in auth-nx-react-nodejs folder, 
    mkdir libs
    mkdir tools
8. nx g @nx/js:library shared-types => create shared libs


How to run?
Only frontend: nx serve frontend
Only backend: nx serve backend
Frontend/Backend at the same time: nx run-many --target=serve --projects=frontend,backend
