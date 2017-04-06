#Deploy code

1. Pull following services from github
    * [Prestige Frontend](https://github.com/Ordineo/prestige-frontend)
    * [Prestige Eureka](https://github.com/Ordineo/prestige-eureka)
    * [Prestige Gateway](https://github.com/Ordineo/prestige-gateway)
    * [Prestige Employees service](https://github.com/Ordineo/prestige-employees-service)
    * [Prestige Endorsements service](https://github.com/Ordineo/prestige-endorsements-service)
    * [Prestige Config Server](https://github.com/ordina-jworks/prestige-config-server)  
    
    
2. Install docker: [Docker for ...](https://docs.docker.com/engine/installation/)  


3. Build java artifact and docker images (build without tests add: -DskipTests=true) 
    * On local machine: mvn clean install  <span style="color: red">-P docker-local</span>
    * On Azure: mvn clean install  <span style="color: red">-P build-docker</span>  
    

4. Add Hibernate drivers
    * SQLJDBC  jar is not present in maven central repo.You have to install it manually.First download it from https://www.microsoft.com/en-in/download/details.aspx?id=11774 and install it by running the following command from the directory in which you put your jar.
    * Run: mvn install:install-file -Dfile=<PathToJar> -DgroupId=com.microsoft.sqlserver -DartifactId=sqljdbc42 -Dversion=6.0 -Dpackaging=jar  
    

5. Deploy code with docker-compose
    * Pull docker compose file from github [Prestige Config](https://github.com/ordina-jworks/prestige-config)
        * [Local development](https://github.com/ordina-jworks/prestige-config/tree/master/DockerComposeForLocalDeveloment): This file needs to be used to deploy on your local machine
        * [Azure](https://github.com/ordina-jworks/prestige-config/tree/master/DockerComposeForAzure): This file needs to be used to deploy the code to Azure
    * Run following command where file is saved: docker-compose up -d
    * Extra commands
        * Stop all microservices: docker-compose down
        * View all logs: docker-compose logs
        * View logs for specific service: docker-compose logs <service-name>