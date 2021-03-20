# Network Inventory

I started this project in order to have solution for keeping an
inventory over my various servers and other network equipment.

The idea later expanded to be an inventory for multiple customers.
In addition the customers should be able to access their inventory but only see the items they own.

This project consists of the [backend](https://github.com/Network-Inventory/ni-backend) in Django and the [frontend](https://github.com/Network-Inventory/ni-frontend) written in VueJS.

## Production Setup

1. Clone the repository
2. Copy the `.env-example` file to `.env` and change the `POSTGRES_PASSWORD`
   and `DJANGO_SECRET_KEY` variables to something secure.
3. Run `docker-compose up` and connect to http://localhost

#### Environment Variables

To customise the application in the Docker container you can use environment
variables in the docker-compose.yml file. Currently the following variables are
supported.

- **DJANGO_SECRET_KEY** the secret key is mandatory, otherwise the application
  doesn't run. Make sure that it is some long random string.
- **DJANGO_DEBUG** settings this variable to any value enables the Django debug
  mode. Make sure that you don't set it on a production server.
- **DJANGO_SETTINGS_MODULE** the path to the settings file to use in the
  container. This requires a dotet syntax. The default is
  `network_inventory.settings.docker`.

## Documentation

Currently there isn't a lot of documentation present.
