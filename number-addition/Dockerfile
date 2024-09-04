# Use the latest Ubuntu image as the base
FROM ubuntu:latest

# Label the Docker image
LABEL image="frontendstatic"

# Update package lists, install Apache2 and unzip, and remove default index.html
RUN apt-get update && \
    apt-get install -y apache2 unzip && \
    rm -rf /var/www/html/index.html

# Copy the zip file to the container
COPY "number addition.zip" /var/www/html/

# Set the working directory
WORKDIR /var/www/html

# Unzip the source code
RUN unzip "number addition.zip" && \
    rm "number addition.zip"  # Optional: Remove zip file after extraction

# Expose port 80
EXPOSE 80

# Start Apache in the foreground
CMD ["apachectl", "-D", "FOREGROUND"]
