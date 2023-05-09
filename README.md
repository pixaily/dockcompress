# DockComPress (DCP)
Docker Composer for Wordpress is a `docker compose` configuration for single or multiple instaces of Wordpress with single Dokcer configuration.

## It is not tested for production evironments

# Description
This configuration will allow you to run several Wordpress instances with different version if needed at the same time. I use this configuration when I need to update Wordpress and I need to have both (old and new) versions working at the same time.

# How to use
- Create a docker network - `docker network create dcp`
- Open `.env` file
- Change the values of the variables that you need, like: `PROJECT_1_NAME=project`
- Open the folder containering the repo in terminal/command line and run `docker-compose up -d`
