[![Elevator](http://dl.dropbox.com/u/2497327/baneer.png)](http://elevator.readthedocs.org)

[![Build Status](https://secure.travis-ci.org/oleiade/Elevator.png)](http://travis-ci.org/oleiade/Elevator)

Key-Value store written in Python and based on levelDB, allows high performance on-disk bulk read/write.

Allows async, multithreaded and/or remote access to a multi-leveldb backend.

Relying on the zeromq network library and msgpack serialization format, it is made to be portable between languages and
platforms.

See [Documentation](http://oleiade.github.com/Elevator) for more details


### Depends on

- zmq-3.X
- pyzmq (built with zmq-3.X)
- leveldb
- py-leveldb


### Installation


```bash
$ pip install fabric
$ fab build
$ pip install -r requirements.txt
$ python setup.py install
```


### Usage

When elevator is installed, you can then launch the server using the elevator executable.
Note that a --daemon option is disposable, and allows you to run elevator server as a daemon,
storing it's pid in .pid file in /tmp.

See config/elevator.conf for an example of Elevator configuration.

*Example*:

```bash
$ elevator --help
usage: elevator [-h]
                [--daemon] [--config CONFIG FILE] [--transport tcp | ipc] [--bind BIND] [--port PORT]
                [--workers WORKERS COUNT] [--paranoid SHOULD IT BREAK ON UNHANDLED EXCEPTIONS?]

Elevator command line manager

optional arguments:
    -h, --help       show this help message and exit
    -d, --daemon      Launch elevator as a daemon
    -c, --config      Path to elevator server config file, eventually
    -t, --transport   Transfert protocol (tcp | ipc)
    -b, --bind        Ip to bind server to
    -p, --port        Port the server should listen on
    -w, --workers     How many workers should be spawned (Threads with concurrent access to all the db store)
    -P, --paranoid    If option is set, Elevator will shutdown and log on first unhandled exception
```

### Clients

*Python* : [py-elevator] (http://github.com/oleiade/py-elevator)

*Go* : [go-elevator](http://github.com/oleiade/go-elevator) (Early early, so early version)

*Clojure* : *Coming soon*

*C* : *Coming soon*


### Thanks

Thanks to [srinikom](https://github.com/srinikom) for its [leveldb-server](https://github.com/srinikom/leveldb-server) which was a very good base to start from.
