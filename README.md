# docker_sample

This repository is for learing porposes.
It's a minimal out of the box docker sample.

Files: 
Dockerfile: describes docker instructions
package.json: contains dependencies needed to run the serverside application
app.js: serverside application (simple express server)


Create a image named "docker_sample" from the Dockerfile:
	docker build -t docker_sample .

Description:
docker build = default command to build a image
-t = tag = name for the image
. = take everything in the build directory (current filepath)


Run a docker-container based on the previously built image:
	docker run -p 3000:3000 -d docker_sample

Description:
docker run = default command to run a container
-p = port = binds port 3000 of the container (left side) to the port 3000 of the host (right side)
-d = detached mode = does not block console interaction (background task)


Visit the application:
	http://localhost:3000