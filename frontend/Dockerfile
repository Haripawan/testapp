#FROM
#MAINTAINER
#RUN
#ADD
#COPY
#ENV
#EXPOSE
#CMD
#ENTRYPOINT
#USER
#WORKDIR
#VOLUME
#ARG

#always start with a image  . An image can be created from another image If there is no image the it is FROM scrach

# 1.Update of all existing package :yum -y updae
# 2. Insatll Platform -yum -y install httpd
# 3. Copy the code to document : /var/www/html
# 4. Set any env variable for bacjend : BACKENDLB
# 5. Apache is running on port 80
# 6. START Apache

FROM centos:7
MAINTAINER haripawan.k@gmail.com
RUN yum -y update
RUN yum -y install httpd

#RUN useradd apachectl
#USER apache 

#RUN mkdir /apps

# WORKDIR /apps

# Add copies the files from a folder. ADD can be used for a url to folder too
ADD code /var/www/html

#use copy or ADD

#Copy copies the folder itself
#COPY code /var/www/html

ENV BACKENDLB=test
EXPOSE 80

#CMD apachectl - D FOREGROUND this is equavalent to sh -c " command" . Problem with this is shell will run as first proess where docker engine only monitors the ist process. IT is always suggested to run actual applicationas first process.
#Exec format of CMD
CMD ["apachectl", "-D", "FOREGROUND"]
