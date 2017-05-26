#Deploy code

1. Pull following services from github
    * [Prestige Frontend](https://github.com/Ordineo/prestige-frontend)
    * [Prestige Eureka](https://github.com/Ordineo/prestige-eureka)
    * [Prestige Gateway](https://github.com/Ordineo/prestige-gateway)
    * [Prestige Employees service](https://github.com/Ordineo/prestige-employees-service)
    * [Prestige Endorsements service](https://github.com/Ordineo/prestige-endorsements-service)
    * [Prestige Config Server](https://github.com/ordina-jworks/prestige-config-server)  
    
    
1. Install docker: [Docker for ...](https://docs.docker.com/engine/installation/)      

1. Add Hibernate drivers
    * SQLJDBC  jar is not present in maven central repo.You have to install it manually.First download it from https://www.microsoft.com/en-in/download/details.aspx?id=11774 and install it by running the following command from the directory in which you put your jar.
    * Run: mvn install:install-file -Dfile=<PathToJar> -DgroupId=com.microsoft.sqlserver -DartifactId=sqljdbc42 -Dversion=6.0 -Dpackaging=jar  

1. Deployment order
    * The services need to be started in the following order if you want to run them manually:
        1. Config server and Eureka service
        1. Hystrix Service
        1. Employees service and Endorsements service
        1. Gateway service
        1. The frontend can be started whenever

1. Build java artifact and docker images
    * Before you can deploy, you need to build the docker images with maven:
        * On local machine: 
            * mvn -DskipTests=true clean install  <span style="color: red">-P docker-local</span>
        * On Azure: 
            * mvn clean -DskipTests=true install  <span style="color: red">-P build-docker</span>
            * To deploy you first need to push these images to the server with: 
                * _docker push ip-address:5000/prestige-employees-service_

1. Building the frontend
    * Building the frontend happens with the following commands:
        * _npm install -g @angular/cli_
        * _npm install_
        * _ng build (--prod) (--environment=red)_
        * _docker build -t ip-address:port/frontend ._
        
1. [Node RED](https://github.com/Ordineo/prestige-node-red)

1. Deploy code with docker-compose
    * Docker-compose automatically starts the services in the right order
    * Pull docker compose file from github [Prestige Config](https://github.com/ordina-jworks/prestige-config)
        * [Local development](https://github.com/ordina-jworks/prestige-config/tree/master/DockerComposeForLocalDeveloment): This file needs to be used to deploy on your local machine
        * [Azure](https://github.com/ordina-jworks/prestige-config/tree/master/DockerComposeForAzure): This file needs to be used to deploy the code to Azure
    * Insert ghorg and ghtoken as environment variables where needed
        * These can be found or created in the GitHub settings
    * Run following command where file is saved: docker-compose up -d
        * For deployment on azure this means you need to ssh to the docker VM and run this command in the ssh terminal
        * Check azure for the ip address
        * If you want to update one service you need to remove the according image in the docker VM for online deployment
    * Extra commands
        * Stop all microservices: docker-compose down
        * View all logs: docker-compose logs
        * View logs for specific service: docker-compose logs <service-name>