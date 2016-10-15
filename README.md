#Simple Lamp docker for development

Its based on nginx-alpine , php5.6-fpm and mysql docker images , with some custom configs

To use just copy you app into site folder and run the following command

`docker-compose start`

If is the first time you are running this environnment run

`docker-compose build`

To stop this environment just run

`docker-compose stop`

**NOTES:** All of this commands must be executed from this root directory.