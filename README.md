# docker_files
docker files for multiple purpose

## Build the docker image

    docker build -t <imagename> -f <dockerfilename> .

## Run the container with mounting the working directory

    docker run -i -d -v $(pwd):/mnt/workspace --name workstation <imagename>

## Login into the container to use as working environment

    docker exec -it $(docker ps | grep <imagename> | awk '{print $1}') bash    
