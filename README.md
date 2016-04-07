# docker-scriptform
https://github.com/fboender/scriptform containerized

run the examples:

    docker run -p 80:80 -it ctorff/scriptform /scriptform/examples/validate/validate.json

or run your own scripts:

    docker run -v "$(pwd)/scripts:/scripts" -p 80:80 -it ctorff/scriptform /scripts/myscript.json

The entrypoint is:

    ENTRYPOINT ["/usr/bin/scriptform", "-f", "-p80"]

See https://github.com/fboender/scriptform for documentation abount options, scripting etc.
