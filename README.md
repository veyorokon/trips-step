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
$ cd trips-step-parser
$ ./setup.sh
```


   [docker]: <https://github.com/docker>
   [docker-compose]: <https://github.com/docker/compose>
   [trips-step]: <https://github.com/wdebeaum/step>
   [graphviz]: <https://gitlab.com/graphviz/graphviz>
   [wordnet]: <https://github.com/wordnet/wordnet>
