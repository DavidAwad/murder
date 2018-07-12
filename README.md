# Murder

This is a command line interface for spreading files throughout a fleet over the bittorrent protocol.

## start the tracker
```shell
python murder_tracker.py
```

## create a torrent file
in this case, let's make a torrent out of a sample file we want to deploy. we'll call it `deploy.tar.gz`

```shell
$ python murder_make_torrent.py <file> <trackerhost:port> <target>

# for example:  python murder_make_torrent.py deploy.tar.gz tracker.twitter.com:8998 deploy.torrent
```

## seed the package
```shell
python murder_client.py seed deploy.torrent deploy.tar.gz
```

## from peers get the package
```shell
python murder_client.py peer deploy.torrent
```
