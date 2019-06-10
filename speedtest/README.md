Dockerfile based on work at tianon/dockerfiles/speedtest

Updated to the latest version of speedtest-cli to support the --no-upload and --no-download switches

To build:

`docker build -t sfk/speedtest:latest .`

Samples:

    run speedtest and delete container at the end

    docker run --rm --net=host sfk/speedtest
    docker run --rm --net=host sfk/speedtest --version
    docker run --rm --net=host sfk/speedtestdocker --list
    docker run --rm --net=host sfk/speedtestdocker --server 2025

Yada, yada, yada, yada...

`--net=host` is not _required_, but if we're wanting to test native performance then we want direct access to the relevant interface without any overhead.