# this file describes how to build tsuru nodejs image
# to run it:
# 1- install docker
# 2- run $ docker build -t tsuru/nodejs https://raw.githubusercontent.com/tsuru/basebuilder/master/nodejs/Dockerfile

from	ubuntu:14.04
run	apt-get update
run	DEBIAN_FRONTEND=noninteractive apt-get install wget curl apt-transport-https -y --force-yes
run	wget http://github.com/tsuru/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/nodejs/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/base/start /var/lib/tsuru
run	curl -s https://deb.nodesource.com/gpgkey/nodesource.gpg.key | apt-key add -
run	echo 'deb https://deb.nodesource.com/node trusty main' > /etc/apt/sources.list.d/nodesource.list
run	apt-get update
run	apt-get install nodejs -y --force-yes
run	/var/lib/tsuru/base/install
