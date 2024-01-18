# Use the official Nginx image as the base image
FROM nginx:alpine

# Copy the index.html file into the default Nginx HTML directory
COPY index.html /usr/share/nginx/html

# Create a simple endpoint to expose container ID
RUN echo "$(hostname)$(ifconfig eth0 | grep 'inet ' | awk '{print $2}')" > /usr/share/nginx/html/container-id

# Expose the port on which Nginx is listening
EXPOSE 8088
