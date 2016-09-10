ThreadFix is a software vulnerability aggregation and management system that helps organizations aggregate vulnerability data, generate virtual patches, and interact with software defect tracking systems.

The `threadfix-docker-mysql` image uses Dockerize to pass Environment variables to the `jdbc.properties` file on run. These values should correspond with your Mysql database URL, user, and password.

1. Build the images: `docker build -t app/threadfix .` (not necessary once images are pushed to Docker Hub)
2. `docker pull app/threadfix` (only if image is pushed to repository)
2. Launch the container using your credentials. `docker run -d -p 8443:8443 -e MYSQL_USERNAME="<your_db_username>" -e MYSQL_PASSWORD="<your_db_pass>" -e MYSQL_DB_URL="your_db_url" app/threadfix`
3. Threadfix is now available on your localmachine https://<yourdockerip>:8443/threadfix


*Always remember to change the default UI credentials!*