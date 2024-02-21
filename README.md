Getting Started
===============

***Installing Prerequisites***
    Go toolchain: https://go.dev/doc/install
    Docker: https://docs.docker.com/engine/install/

***Starting Jaeger backend with Docker***

    docker run -d -p6831:6831/udp -p16686:16686 jaegertracing/all-in-one:latest

And, to open the Jaeger UI paste: http://127.0.0.1:16686/ into your browser.

***Running HotROD from Source***

    git clone git@github.com:jaegertracing/jaeger.git jaeger
    cd jaeger
    go run ./examples/hotrod/main.go all
        
To open the UI paste: http://127.0.0.1:8080/ into your browser.

***Optionally run from Docker file***

To build:

    docker-compose-f *path-to-.yml-file* up
    
To Shutdown:

    docker-compose-f *path-to-.yml-file* down

