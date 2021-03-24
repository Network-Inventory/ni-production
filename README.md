# Network Inventory

I started this project in order to have solution for keeping an inventory
over my various servers and other network equipment.

The idea later expanded to be an inventory for multiple customers. In
addition the customers should be able to access their inventory but only see
the items they own.

This project consists of the
[backend](https://github.com/Network-Inventory/ni-backend) in Django and the
[frontend](https://github.com/Network-Inventory/ni-frontend) written in
VueJS.

## Production Setup

1. Clone the repository
2. Copy the `.env-example` file to `.env` and change the `POSTGRES_PASSWORD`
   and `DJANGO_SECRET_KEY` variables to something secure.
3. Replace the value for `NI_HOST` to the domain of your website.
   If you want to debug the backend `NI_MODE` to `development`.
3. Run `docker-compose up` and connect to domain defined in `NI_HOST`

#### Environment Variables

To customise the application in the Docker container you can use environment
variables in the docker-compose.yml file. Currently the following variables are
supported.

- **DJANGO_SECRET_KEY** the secret key is mandatory, otherwise the application
  doesn't run. Make sure that it is some long random string.
- **DJANGO_SETTINGS_MODULE** the path to the settings file to use in the
  container. This requires a dotet syntax. The default is
  `network_inventory.settings.docker`.
- **NI_HOST** the domain from you serve the application. This is required in
  order for the backend to work properly.
- **NI_MODE** the state of the application, should be `production` for a
  production environment.

## Documentation

Currently there isn't a lot of documentation present.
