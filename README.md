# Nextcloud docker-client
This image provides you an alpine based image for syncing your files with a remote [nextcloud server ](https://nextcloud.com/)

This image is based on the work made by: [Martin Peters](https://github.com/FreakyBytes)

## Example

    docker run -it --rm \
      -v $(pwd)/sync-folder:/media/nextcloud \
      -e NC_USER=$username -e NC_PASS=$password \
      -e NC_URL=$server_url\
      juanitomint/nextcloud-client
    
replace:
 $username
 $password 
 $server_url 
 with valid values for an existing and valid user on a Nextcloud Server.

## ENV variables to customize your deploy
##### NC_USER 
The user name to log in 
Default: username
##### NC_PASS 
Valid password for the user above in clear text
Default: password

##### NC_SOURCE_DIR
The directory inside de docker container to be synced, usually you will have a local mount here or a named volume
default: /media/nextcloud/

##### NC_SILENT
whather or not output activity to console
default: false



##### USER
The system user inside the container you want to use for runing the sync

default: ncsync

##### USER_GUID
The system user group id inside the container you want to use for runing the sync

default: 1000

##### USER_UID
The system user id inside the container you want to use for runing the sync

default: 1000

##### NC_TRUST_CERT
whather or not trust self signed certificates

default: 1000




