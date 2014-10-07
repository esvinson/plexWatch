This is a Dockerfile setup for plexWatch (https://github.com/ljunkie/plexWatch) and plexWatchWeb (https://github.com/ecleese/plexWatchWeb)

Setup:

Follow steps 1 through 3 and ONLY steps 1 through 3 here: https://github.com/ljunkie/plexWatch#install

To run:

```
docker run -d --net="host" --name="plexWatch" -v /path/to/plexWatch:/plexWatch -v /path/to/plex/logs:/logs -v /etc/localtime:/etc/localtime:ro -p 8082:8082 needo/plexwatch
```

Edge
------
If you would like to run the latest updates from the master branch run:

```
docker run -d --net="host" --name="plexWatch" -v /path/to/plexWatch:/plexWatch -v /path/to/plex/logs:/logs -v /etc/localtime:/etc/localtime:ro -e EDGE=1 -p 8082:8082 needo/plexwatch
```

To access plexWatchWeb visit:

http://server:8082/plexWatch/

Troubleshooting:
----------

Log files of plexWatch is available where you installed plexWatch.pl for troubleshooting.
