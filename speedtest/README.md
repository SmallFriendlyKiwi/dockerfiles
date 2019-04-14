Dockerfile based on work at tianon/dockersiles/speedtest

Updated to the latest version of speedtest-cli to support the --no-upload and --no-download switches

Samples:

    docker run --rm --net=host tianon/speedtest
    docker run --rm --net=host tianon/speedtest --version
    docker run --rm --net=host tianon/speedtestdocker --list
    docker run --rm --net=host tianon/speedtestdocker --server 2025

Yada, yada, yada

`--net=host` is not _required_, but if we're wanting to test native performance (or use `--source some-specific-host-IP`) then we want direct access to the relevant connections without any overhead.

To build:

docker build -t smallfriendlykiwi/speedtest:latest .
