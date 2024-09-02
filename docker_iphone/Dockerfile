FROM nginx:alpine

WORKDIR /usr/share/nginx/html/
RUN apk add --no-cache curl unzip
RUN rm -rf index.html
COPY . .

# Expose port 80 for web traffic
EXPOSE 80


# Start Nginx as the foreground process
CMD ["nginx", "-g", "daemon off;"]