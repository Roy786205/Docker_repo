# Use the official NGINX image from the Docker Hub
FROM nginx:alpine

# Copy the application files to the NGINX HTML directory
COPY index.html /usr/share/nginx/html/
COPY style.css /usr/share/nginx/html/
COPY app.js /usr/share/nginx/html/

# Expose port 80 to access the application
EXPOSE 80