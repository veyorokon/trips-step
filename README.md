# Trips Step Parser for Docker.

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Docker implementation of the Trips Step parser.

# Step Parser

  - Parses passages as well as single sentences

### Tech

Trips uses a number of open source projects to work properly:

* [trips-step] - Parser for documents and passages.
* [docker] - Container management.
* [docker-compose] - Container orchestration.
* [graphviz] - Graph visualization.
* [wordnet] - Lexical database of any language

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

### Installation

This requires [Docker](https://docs.docker.com/install/) and [docker-compose](https://docs.docker.com/compose/install/) to run.

After cloning the repo, run the setup.sh script to clone the Step parser into the container directory.

```sh
$ ./setup.sh
```

Build and start the container
```sh
$ docker-compose build
$ docker-compose up
```

In a new terminal, build the files
```sh
$ docker-compose exec trips-step bash
$ make install
```

Start the Facilitator module

```sh
$ cd Facilitator
$ ./Facilitator
```

In a new terminal, start the TextTagger module
```sh
$ docker-compose exec trips-step bash
$ cd TextTagger
$ ./TextTagger
```

In a new terminal, start the lisp interface
```sh
$ docker-compose exec trips-step bash
$ cd Systems/STEP
$ sbcl --load test.lisp
```
Wait for the module to load. Then in the sbcl (* LISP) interaface, type:
```sh
* (run)
```

Test a parse
```sh
* (test-paragraph "Who is the president of the United State?")
```


   [docker]: <https://github.com/docker>
   [docker-compose]: <https://github.com/docker/compose>
   [trips-step]: <https://github.com/wdebeaum/step>
   [graphviz]: <https://gitlab.com/graphviz/graphviz>
   [wordnet]: <https://github.com/wordnet/wordnet>
