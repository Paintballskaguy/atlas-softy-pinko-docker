#using the latest Nginx image as the base
FROM nginx:latest

#copy the soft-pinko front-end files to the right dir
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

#Copy the Nginx config file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf