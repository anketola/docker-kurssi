sudo docker run -it -d --name p115 ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

sudo docker exec -it p115 bash

Inputs: 
apt-get update
apt-get install curl

sudo docker attach p115

input:
helsinki.fi
