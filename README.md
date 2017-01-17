# Docker for LIMES

Assembled from LIMES.0.6.RC4.zip from https://github.com/aksw/limes.
This version of LIMES is deprecated. Use "limes-service" branch for up-to-date version.

## Using
To build docker file run:
```
    make
```

For running test-example run:
```
    make run-example
```

For running your own configuration:
```
    cp your-own-config.xml ./config/linking-configuration.xml
    make run
```

Results of the example configuration will be saved in the ./results folder. For your own configuration, you must point output to the ./results folder. Otherwise, the data will be lost.

## Comments
The results of the LIMES run are saved into ./results folder mounted as a volume. The volumes are mounted on docker host. Therefore this repository as it is right now designated to run on docker host machine.
Tested on Ubuntu 14.04 with Docker version 1.9.0, build 76d6bc9

## TODOs
* Configure continuous delivery with the git repository (under development at the moment): https://github.com/AKSW/LIMES-dev
* Logging should be written in the same folder as results
