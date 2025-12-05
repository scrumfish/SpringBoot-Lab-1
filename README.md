# Spring Boot Microservices - Lab 1
In this lab, you will run a node based microservice then add a Java SpringBoot microservice and test them both in Postman.
## Part 1
1. Open the bash terminal in VS Code.
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
```bash
docker compose up --build
```

When docker compose runs, it will build and spin up the timesheet-api service, but not the others. You will edit the docker compose file to add the Spring Boot service in a moment. For now, we'll test the service with Postman.
Once you have built with docker compose, you don't have to again until you change the code.
## Part 2
In your bash terminal inside VS Code follow these teps.
1. Run 
```bash
curl http://localhost:3000/users
```
2. You will see two users returned.

3. Next, POST a user to the same URL.

```bash
curl -X POST http://localhost:3000/users \
  -H "Content-Type: application/json" \
  -d '{"firstName":"Sammy","lastName":"Hagar","hoursWorked":12}'
```

4. Finally, run the GET again and observe your new record is listed.
## Part 3
The final part of this lab is to observe the pattern laid out for the timesheet-api and add the payroll-api to the docker-compose.yml file. Use curl to get http://localhost/8080/api/employees and verify it is working.
## Conclusion
In this lab you ran a simple node express based microservice, then added a Java based microservice to the infrastructure. This is an example of polygot architecture.