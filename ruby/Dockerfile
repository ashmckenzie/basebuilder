# this file describes how to build tsuru ruby image
# to run it:
# 1 - tsuru-admin platform-add ruby -d https://raw.github.com/ashmckenzie/basebuilder/master/ruby/Dockerfile

from	ubuntu:14.04
run	apt-get update
run  apt-get install -y --force-yes software-properties-common wget
run	wget http://github.com/ashmckenzie/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/ruby/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/base/start /var/lib/tsuru
run	/var/lib/tsuru/ruby/install
