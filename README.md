# Login-Form-PHP-MYSQL-Docker
This is a login form made using PHP, which stores the data to mysql and this application runs on docker
Steps to run this project : 
1) Firstly store the files in a directory then locate this directory using a terminal ( VS Code would be good ), then run the command "docker-compose up -d" to run containers in detached mode.
2) Next step is to go to web browser and open "localhost://8081" , where you will see phpmyadmin image, then put user--> "USER" and password --> "PASS", then you will be logged in to the phpmyadmin, where you can run the following query to create a table "users" : CREATE TABLE `users` (
`id` int NOT NULL,
`name` varchar(100) NOT NULL,
`email` varchar(100) NOT NULL,
`mobile` BIGINT NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
ALTER TABLE `users`
ADD PRIMARY KEY (`id`);
ALTER TABLE `users`
MODIFY `id` int NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;
3) Followed by which you can see the created table, now go to web browser and open "localhost://8000", where you can see the login form , where you put the data and click on Submit and now you can see the data updated in users table in database.
4) You can use the command "docker-compose down" to stop and remove the containers.
Reference from : " https://blog.devops.dev/run-php-application-on-docker-with-mysql-phpmyadmin-d19db6c2a9a3 ".
