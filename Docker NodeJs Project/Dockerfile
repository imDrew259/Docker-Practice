# First we define what dependency we would like to fetch from Docker Hub
# Means these are those software which should be installed on our system
FROM node 

# In docker container we also have a file system
# We start from the root directory / 
# but instead we create a folder in that root directory /app
# Now setting the working directory as /app
# This will move ust to /app thus all commands will run in /app
WORKDIR /app

# Now we would like to copy all of our files to image
# Copy command contains two parameters:- first what to copy <space> Where to copy
# First parameter . means copy all the folder, files present parallel to docker file
# Second parameter is where to copy-> in this we can give absolute path or relative
# /app is absolute, ./ is relative as we have set /app as WORKDIR
COPY . /app

# After copying this is the command we would likt to run in the image
# this command will run in image and not while creating a container
RUN npm install

# The node app which resides in container, to make it available
# we expose the port
EXPOSE 80

# This is the command that runs when we create a container instance
# Run commands work when an image is created
# while CMD command runs when container is created
CMD ["node", "server.js"]