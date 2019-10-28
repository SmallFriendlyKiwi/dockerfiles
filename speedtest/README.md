Dockerfile based on work at tianon/dockerfiles/speedtest

Updated to the latest version of speedtest-cli to support the --no-upload and --no-download switches

To build:

`docker build -t sfk/speedtest:latest .`

Where sfk is arbitrary.  It could be your name or alias that you use.

Samples:

    run speedtest and delete container at the end

    docker run --rm --net=host sfk/speedtest
    docker run --rm --net=host sfk/speedtest --version
    docker run --rm --net=host sfk/speedtest --list
    docker run --rm --net=host sfk/speedtest --server 11326

Yada, yada, yada...

`--net=host` is not _required_, but if we're wanting to test native performance then we want direct access to the relevant interface without any overhead.
