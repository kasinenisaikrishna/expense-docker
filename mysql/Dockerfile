FROM mysql:8.0
# we can get the below variable name from docker hub documentation it self https://hub.docker.com/_/mysql
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 
# we need to place the script in /docker-entrypoint-initdb.d location for docker so when container is started for the first time the scripts will be executed https://hub.docker.com/_/mysql
# create a folder called script and place schema code and add using add instruction and place *.sql in /docker-entrypoint-initdb.d docker will take care
ADD scripts/*.sql /docker-entrypoint-initdb.d
    # MYSQL_DATABASE=transactions \
    # MYSQL_USER=expense \
    # MYSQL_PASSWORD=ExpenseApp@1