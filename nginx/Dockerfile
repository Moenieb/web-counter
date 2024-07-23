#Let's try our luck with Alpine
FROM nginx:alpine

# Copy custom index.html to the Nginx default directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80
EXPOSE 80

# Start Nginx server
# -g is the command line parameter for directives
# We essentially starting the nginx instance and running it as daemon
CMD ["nginx", "-g", "daemon off;"]

