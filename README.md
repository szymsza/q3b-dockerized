# Usage
## Initisation
- Clone CUDD-3val into `./cudd-3val`
- Clone Q3B-pBDD into `./q3b`
- Put your testing benchmarks into `./testing`
- Initialise Docker container, open shell (see below), and run initial compilation `/helpers/init`

## Running benchmarks
- Run Q3B from inside the Docker shell `/Q3B/build/q3b /testing/yourfile.smt2`

# Various commands
## Outside Docker shell

### Initial build and rebuild after Dockerfile change
`docker-compose up -d --build q3b`

### Start container
`docker-compose up -d q3b`

### Stop container
`docker stop q3b`

### Open shell
`docker exec -it q3b bash`

### Copy executable outside
`docker cp q3b:/Q3B/build/q3b q3b`

## Inside Docker shell

### Recompile various tools
`/helpers/cudd-recompile`, `/helpers/q3b-recompile`, `/helpers/both-recompile`