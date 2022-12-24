

- mongodb
    
    ```
    docker run -it -d --name net-microservices-course-mongodb \
    		-p 27017:27017 --network net-microservices-course-network \
    		--restart always \
    		-v mongodb_data_container:/data/db \
    		mongo:latest
    ```
    
- SQL SERVER
    
    ```
    docker run -d --name sql-container \
    	--network mydockernetwork \
    	--restart always \
    	-e 'ACCEPT_EULA=Y' \
    	-e 'SA_PASSWORD=$tr0ngS@P@ssw0rd02' -e 'MSSQL_PID=Express' \
    	-p 1433:1433 mcr.microsoft.com/mssql/server:2017-latest-ubuntu
    ```