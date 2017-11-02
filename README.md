# pipeline-ngnix-lua
Nginx deployment in kubernetes with helm.

Deployment done in jenkins with Jenkinsfile.

Pipline:
1. Build nginx v.1.13.6 with lua-nginx-module v.0.10.11rc2
2. Build docker image with custom nginx.conf and index.html from github repo, pushing docker image to the public repo at hub.docker.com (https://hub.docker.com/r/corvuscoraxx/nginx/)
3. Deployment of the docker image with helm chart at kubernetes cluster 

Code published at github.
Jenkins build task is triggered by git push into the master.
Jenkins server http://130.211.18.211
