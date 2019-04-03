## Steps to start Keycloak
Running the following command will start Keycloak with Postgres and a sample realm.

`docker-compose -f docker/app.yml up`

Running the docker-compose will create a keycloak directory in your root folder and use that for saving
all the Postgres and Keycloak files that you will need to sustain a restart or cleaning up of the image.
*This will not work in a Windows environment.*

## Access Keycloak
You should see Keycloak admin portal up and running at http://localhost:9080

Will be able to login to the admin portal using the following credentials:
userid: admin
pwd: admin

## Documentation for Keycloak
Refer to the following documentation for Keycloak to get a good understanding of all the features and
on how to set it up for usage with your application:

https://www.keycloak.org/documentation.html

Please go through the following documents in detail, especially the authorization services guide to 
learn the basic concepts and features in Keycloak. For the securing applications you can skip the first
4 units and concentrate on 5-7. We are only looking into using Keycloak for OIDC and not SAML.

https://www.keycloak.org/docs/latest/securing_apps/index.html
https://www.keycloak.org/docs/latest/authorization_services/index.html

If you are curious to test it with a Node application to play with, here are the steps to get started:
https://www.keycloak.org/docs/latest/securing_apps/index.html#_nodejs_adapter

The code for the above is on github: https://github.com/keycloak/keycloak-nodejs-connect

## CKAN with Keycloak
Following extension seems to support the integration of CKAN and Keycloak:

https://github.com/etri-odp/ckanext-keycloak

