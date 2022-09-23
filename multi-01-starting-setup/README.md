#  Command for excution

### backend
- docker run --name goals-backend --rm  80:80 -v logs:/app/log
 --network goals-net -p 80:80 -v logs:/app/logs -v C:\Usertarting-setup\backend:/s\X\IndividualProjects\docker_study\multi-01-starting-setup\backend:/app -v /app/node_modules -d goals-node
 
 ### frontend
 - docker run --name goals-frontend --rm -it -p 3000:3000 goals-react

### DB
- docker run --name mongodb --rm -d --network goals-net -v data:/data/db mongo
