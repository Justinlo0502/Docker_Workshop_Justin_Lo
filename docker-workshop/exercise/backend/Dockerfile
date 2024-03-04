# Define the base image for the container, using a pre-built image with Node.js 18
FROM node:18
# Copy all files and directories from the current directory into the "/app" directory inside the container
COPY . /app/
# Set the working directory within the container to "/app", making it the starting point for subsequent commands
WORKDIR /app
# Run the "npm install" command inside the container to install the dependencies listed in the "package.json" file
RUN npm install
# Set an environment variable named "PORT" with a value of "8000", potentially used by the application
ENV PORT=8000
# Define the default command to be executed when the container starts, which is to run "node index.js"
CMD ["node", "index.js"]
