FROM ubuntu:16.04

MAINTAINER v.smartking@gmail.com

RUN mkdir -p /var/www/html

RUN echo "deb http://us.archive.ubuntu.com/ubuntu xenial main multiverse" >> /etc/apt/sources.list
RUN apt-get update

RUN apt-get install htop -y
RUN apt-get install wget -y
RUN apt-get install nano -y
RUN apt-get install rar -y
RUN apt-get install unrar -y

RUN apt-get install -y curl python-pip
RUN pip install --upgrade pip

RUN pip install python-linkedin
RUN pip install -U selenium==2.53.5
RUN apt-get install python-lxml -y
RUN apt-get install xvfb -y

RUN apt-get install xserver-xephyr -y
RUN apt-get install tightvncserver -y
RUN pip install pyvirtualdisplay
RUN apt-get install python-imaging -y
RUN apt-get install scrot -y
RUN pip install pyscreenshot
RUN pip install entrypoint2

RUN pip install phonenumbers
RUN pip install lepl
RUN pip install validate_email
RUN pip install pyDNS

RUN apt-get install python-dev -y
RUN apt-get install python-pycurl
RUN apt-get install libcurl4-gnutls-dev librtmp-dev -y
RUN apt-get install libcurl4-openssl-dev -y

RUN apt-get install python-beautifulsoup
#https://github.com/aitjcize/creepy simple python crawler website
RUN pip install creepy
RUN pip install cssselect

# GRAB libs
RUN apt-get install python-dev
RUN apt-get install -y zlib1g-dev
RUN apt-get build-dep libxml2 -y
RUN apt-get install libxslt1-dev -y
RUN apt-get install libcurl4-openssl-dev -y
RUN apt-get install libxml2-dev libxslt-dev -y

#RUN pip install -U grab
RUN apt-get install libcurl4-gnutls-dev librtmp-dev -y
RUN apt-get install libssl-dev libcurl4-openssl-dev python-dev -y

RUN pip install pycurl
#RUN pip install pycurl2 
RUN apt-get install git -y
RUN git clone https://github.com/Lispython/pycurl.git && cd pycurl && python setup.py install

RUN pip install human_curl
#RUN pip install usaddress
RUN apt-get install wget -y 
RUN apt-get install firefox -y 

RUN mkdir firefox \
	&& cd /firefox \
	&& wget https://download-installer.cdn.mozilla.net/pub/firefox/releases/46.0/linux-x86_64/en-US/firefox-46.0.tar.bz2 \
	&& tar xvf firefox-46.0.tar.bz2
RUN rm -rf /usr/bin/firefox
RUN ln -s /firefox/firefox/firefox /usr/bin/firefox

RUN apt-get install unzip -y
RUN apt-get install phantomjs -y
RUN apt-get install tor -y

RUN pip install twisted
RUN pip install requesocks
RUN pip install pyquery

ENTRYPOINT /usr/bin/tail -f /dev/null