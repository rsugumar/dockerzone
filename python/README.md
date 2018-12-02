# python in docker
**Run any python scripts in docker container now.**

Just write any python script file and we can run in docker following the below:

* To Build image: docker-compose build
* To Run image with arg: docker-compose run <service-name> <python-filename>; eg., docker-compose run myapp print-name.py
* To Run image without arg(default): docker-compose run <service-name>; eg., docker-compose run myapp; this will ru un myapp; this will run default py file as in docker-compose myapp:command
