# docker-scriptform

[scriptform](https://github.com/fboender/scriptform) containerized

## build

As usual, e.g.:

    you=YOUR_USERNAME
    docker build -t "${you}/scriptform" .

## run

Run an example (see [examples](https://github.com/fboender/scriptform/tree/master/examples) for more):

    docker run -p 8080:80 -it "${you}/scriptform" /scriptform/examples/validate/validate.json

now go to http://localhost:8080


Or run your own scripts:

    docker run -v "$(pwd)/scripts:/scripts" -p 80:80 -it "${you}/scriptform" /scripts/myscript.json


The entrypoint:

    ENTRYPOINT ["/usr/bin/scriptform", "-f", "-p80"]


See https://github.com/fboender/scriptform for documentation about options, scripting etc.

