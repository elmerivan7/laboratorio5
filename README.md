
JENKINFILE 
Nombrar como archivo docker-compose.yml. Como segundo paso copiar con el siguiente contenido ##########################################################################################

version: "3"

services:

nexus:

      image: sonatype/nexus3
	  
      volumes:
	  
          - "nexus-data:/nexus-data"
		  
      ports:
          - "8081:8081"
          
          - "8082:8082"
jenkins:

      image: jenkins/jenkins:latest
	  
      ports:
	  
          - "8080:8080"
		  
      volumes:
	  
          - "./jenkins-data:/var/jenkins_home"
          
volumes:

nexus-data: {}

#######################################################################################





# Dockerfile
# docker-compose.yml

Comando para levantar Backend y Frontend en Debian

docker-compose up -d
