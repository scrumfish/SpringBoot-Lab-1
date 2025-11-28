# Spring Boot Microservices - Lab 1
In this lab, you will run a node based microservice then add a Java SpringBoot microservice and test them both in Postman.
## Part 1
1. Open PowerShell. The icond should be in your task bar.
2. Change into the `lab-1` folder.
3. Run `ls` to view the contents of the folder.

```
├── employee-timesheet
│   ├── public
│   ├── routes
│   ├── .dockerignore
│   ├── .gitignore
│   ├── app.js
│   ├── Dockerfile
│   ├── package.json
│   └── README.md
└── README.md
```
4. Run the microservice: 
```powershell
docker compose up --build
```

When docker compose runs, it will spin up the employee-timesheet service, but not the others. You will edit the docker compose file to add the Spring Boot service in a moment. For now, we'll test the service with Postman.
## Part 2
Open Postman, the icon should be on your desktop. Once loaded, we will get the employees from the service. There is no backing databse, so the employee list will reset on each restart of this system.
1. Run postman. Use minimal mode. It is not necessary to login.
2. 