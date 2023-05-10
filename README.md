# DockComPress (DCP)
Docker Compose for Wordpress is a `docker compose` configuration for single or multiple instaces of Wordpress with single Dokcer configuration.

## It is tested only for development environments

# Description
This configuration will allow you to run several Wordpress instances with different version if needed at the same time. I use this configuration when I need to update Wordpress and I need to have both (old and new) versions working at the same time.

# How to use
- Create `dcp` docker network with the following command in terminal/command line - `docker network create dcp`
- Edit `.env` file, there is a comment `# UPDATE BASED ON YOUR NEEDS` for every item that may be updated based on your needs
  - Change the values of the variables that you need, like: 
    - `PROJECT_1_NAME=myproject`
    - `PROJECT_2_NAME=myproject_old`
  - The value of `PROJECT_#_MYSQL_PORT` should be differnet for every project and you must use this port to connect to the DB container, like: 
    - `PROJECT_1_MYSQL_PORT=3306`
    - `PROJECT_2_MYSQL_PORT=3307`
- Open the folder containing the repo in terminal/command line and run `docker compose up -d`
- Don't forget to add the virtual hosts to `hosts` file
