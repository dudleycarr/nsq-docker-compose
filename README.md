# nsq Docker Compose

Example configurations for running [nsq](https://nsq.io) within Docker Compose.

The examples require additional configuration before they're ready for
production use. In particular, pay attention to securing ports,
authentication, and storage for services such as nsqd and graphite.

# Inventory

* `basic` | Basic configuration
  <br>A minimal configuration for running nsqd, nsqlookupd, and nsqadmin.
* `with_graphite` | nsq configuration with nsqadmin graphs enabled.
  <br>The basic nsq configuration along with statsd and graphite to support graphs within nsqadmin.
* `multiple_nsqds` | nsq configuration with multiple nsqds.
  <br>The `with_graphite` configuration with 3 nsqds instead of 1.

# Requirements

* Docker Compose
* [Taskfile](https://taskfile.dev) (Optional)

# Getting Started

Running the basic configuration:

```shell
$ task basic:run
```

The nsq services will be running in the background within Docker Compose. You can access
nsqadmin via [http://localhost:4171](http://localhost:4171).

To stop nsq with the basic configuration:

```shell
$ task basic:stop
```

## Run nsq with graphs enabled

```shell
$ task with_graphite:start
```

## Run mutliple nsqds

```shell
$ task multiple_nsqds:start
```

Stopping:
```shell
$ task multiple_nsqds:stop
```
