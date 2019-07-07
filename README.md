# go-docker

## Basic build
`docker build -t go-docker .`

To run locally on port 8080
`docker run -d -p 8080:8080 go-docker`

Then you can interact with it in your terminal using
`curl http://localhost:8080?name=Noah`

## Build with volume storage
`$ docker build -t go-docker-volume -f Dockerfile.volume .`

Create a directory in which you'd like to store logs
`mkdir ~/app-logs`

Then run locally on port 8080
`docker run -d -p 8080:8080 -v ~/app-logs:/go-docker/logs go-docker-volume`

Check out your logs in the directory you stored them!


