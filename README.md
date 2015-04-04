# gtfs-docker


Install to private registry:

cd myql-data
docker build -t mysql-data .
docker tag -f mysql-data registry.docker.helyx.io:5000/mysql-data
docker push registry.docker.helyx.io:5000/mysql-data

cd ..
cd mysql-gtfs
docker build -t mysql-gtfs .
docker tag -f mysql-gtfs registry.docker.helyx.io:5000/mysql-gtfs
docker push registry.docker.helyx.io:5000/mysql-gtfs

cd ..
cd ssdb-data
docker build -t ssdb-data .
docker tag -f ssdb-data registry.docker.helyx.io:5000/ssdb-data
docker push registry.docker.helyx.io:5000/ssdb-data

cd ..
cd ssdb-gtfs
docker build -t ssdb-gtfs .
docker tag -f ssdb-gtfs registry.docker.helyx.io:5000/ssdb-gtfs
docker push registry.docker.helyx.io:5000/ssdb-gtfs
