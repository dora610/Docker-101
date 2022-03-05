    echo 'http://dl-cdn.alpinelinux.org/alpine/v3.9/main' >> /etc/apk/repositories
    echo 'http://dl-cdn.alpinelinux.org/alpine/v3.9/community' >> /etc/apk/repositories
    apk update
    apk add mongodb yaml-cpp=0.6.2-r2
    mongo -version

Build docket image

    docker build .

Run docker image

    doccker run <id>
    
open another instance and check

    docker ps --all
    docker exec -it <container id> sh