FROM ubuntu:15.04 
RUN apt-get update && apt-get install -y \
	 apache2 \
	 && apt-get clean \ 
	 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*I 

ENTRYPOINT ["apache2ctl","-D","FOREGROUND" ]

