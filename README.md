# Prestige Wiki

The Prestige project consists of 7 core services that work together like a well-oiled machine.

The job of the Config server is to provide the configuration to every micro-service. This configuration is stored in the prestige-config repository.
This service runs on port __:42061__.

The Eureka service is used to check the status of every micro-service and runs standard on port __:8761__.

The Employees service is a REST webservice that exposes the roles and employees of the application. 
Every midnight it checks GitHub for new or changed users from the given GitHub organization and stores their data in the database.
The reason I implemented this is because there were problems when working with direct GitHub authentication.
Employees that are automatically imported are defaulted to enabled = 0. For the moment a default user 'admin' is created with password 'default'.
This service provides a /login endpoint. This checks the database for imported employees. It only lets enabled users log-on and if the login was successful it sends back a jwt token.
This endpoint expects a POST request with the following JSON format.
```json
{
  "username": "admin",
  "password": "default"
}
```
To enable an employee you can send a POST request to the __/register__ endpoint with following parameters: __?username=admin&password=test123__.
This is very unsafe and is only a temporary solution. This way everyone can register an account if they know the GitHub handle of an employee.
Therefore I suggest that there will be sent an email to that employee's email address when the employee registers.
The problem with this is that the employee needs to put an email address public on GitHub because only public email addresses can be imported.
* Endpoints on port __:8081__
    * /
    * [/employees](https://github.com/Ordineo/prestige-wiki/#employees)
    * [/roles](https://github.com/Ordineo/prestige-wiki/#roles)
    * /register
    * /login

The Endorsements service is a REST webservice that exposes all the endorsements granted or received.
* Endpoints on port __:8082__
    * /
    * [/endorsements](https://github.com/Ordineo/prestige-wiki/#endorsements)
    * [/categories](https://github.com/Ordineo/prestige-wiki/#categories)
    * [/likes](https://github.com/Ordineo/prestige-wiki/#likes)

The Hystrix service should guarantee a consistent up-time. If other micro-services fail the hystrix service should replace them.
This service can be up and running but is not yet doing it's job.

The last micro-service is the gateway. This services needs to be in between the front end and the backend. This way the frontend
should only send requests to one port __:9900__. The gateway maps requests to the employees service to __:9900/employees-service/*__
and requests to the endorsements service to __:9900/endorsements-service/*__

## Used github repositories
* [Prestige Frontend](https://github.com/Ordineo/prestige-frontend)
* [Prestige Eureka](https://github.com/Ordineo/prestige-eureka)
* [Prestige Gateway](https://github.com/Ordineo/prestige-gateway)
* [Prestige Employees service](https://github.com/Ordineo/prestige-employees-service)
* [Prestige Endorsements service](https://github.com/Ordineo/prestige-endorsements-service)
* [Prestige Hystrix service](https://github.com/Ordineo/prestige-hystrix-service)
* [Prestige Node RED](https://github.com/Ordineo/prestige-node-red)

## Private repositories
The ordina-jworks admin (Ken Coenen) need to grant you access  

* [Prestige Config](https://github.com/ordina-jworks/prestige-config)
* [Prestige Config Server](https://github.com/ordina-jworks/prestige-config-server)


## Best practices:
* [Git](https://ordineo.github.io/prestige-wiki/git)

## Deploying code (Docker)
* [Deploy code](https://ordineo.github.io/prestige-wiki/deploy-code)