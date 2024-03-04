# Use the pre-built image "node:18" as the base for our container. This image already includes Node.js 18 and the necessary environment.
FROM node:18

# Copy all files and directories from the current directory (where the Dockerfile resides) into the "/app" directory within the container.
# This includes your application code, package.json, and any other relevant files.
COPY . /app/

# Set the working directory inside the container to "/app". All subsequent commands will be executed from this directory.
WORKDIR /app

# Run the command "npm install" to install the dependencies listed in your project's "package.json" file.
# This ensures that your application has all the necessary libraries and tools to function correctly.
RUN npm install

# Define an environment variable named "PORT" and set its value to "3000". This variable will likely be used by your application to listen for incoming requests on this port.
ENV PORT=3000

# Define another environment variable named "REACT_APP_BACKEND_URL" and set its value to "http://localhost:8000". 
# This variable might be used by your front-end application (presumably written in React) to specify the URL of the backend service. 
# The URL "http://localhost:8000" points to the backend service, assuming it's running on the same machine and uses port 8000 (as configured in a separate Dockerfile or docker-compose file).
ENV REACT_APP_BACKEND_URL=http://localhost:8000

# Set the default command to be executed when the container starts. This command runs "npm start", which typically starts the development server for your front-end application.
CMD ["npm", "start"]
