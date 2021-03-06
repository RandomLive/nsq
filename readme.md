# Docker compose file for quick start nsq development server

## First

clone this repo
```shell
    git clone git@github.com:RandomLive/nsq.git && cd nsq
```

## Usage

```shell
    docker-compose up
```

run in background
```shell
    docker-compose up -d
```

## Advanced Usage

put below lines in your shell init file

```shell
    # nsq start
    nsqup() {
        cd /your nsq repo path/nsq && docker-compose up -d
        cd -
    }

    nsqdown() {
        cd ~/your nsq repo path/nsq && docker-compose down
        cd -
    }

    nsqstart() {
        nsqdown;
        nsqup;
    }
    # nsq end
```

and source your init file

then

use ```nsqup``` command to start nsq development server

use ```nsqdown``` command to stop nsq development server

use ```nsqrestart``` command to restart nsq development server
