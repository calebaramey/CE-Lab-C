Getting Started
===============

***Installing Prerequisites***
    Go toolchain: https://go.dev/doc/install
    Docker: https://docs.docker.com/engine/install/

***Starting Jaeger with Docker***

    ```
    docker run -d -p6831:6831/udp -p16686:16686 jaegertracing/all-in-one:latest
    ```
    
    And, to open the Jaeger UI paste: http://127.0.0.1:16686/ into your browser.

***Running HotROD from docker***

    ```
    docker run \
        --rm \
        --link jaeger \
        --env OTEL_EXPORTER_JAEGER_ENDPOINT=http://jaeger:14268/api/traces \
        -p8080-8083:8080-8083 \
        jaegertracing/example-hotrod:latest \
        all
    ```
    To open the UI paste: http://127.0.0.1:8080/ into your browser.


