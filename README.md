# rundeck
This repository contains the source for the [Rundeck](http://rundeck.org/) [docker](https://docker.io) image.

## docker
To build new image.

'''
docker build -t tagore22/rundeck:3.3.4 docker/
docker push tagore22/rundeck:3.3.4

'''

## helm
Helm chart repository for rundeck with an practical values.yaml and instructions to roll out. Goal of this repo is to present instructions for deploying a productin ready rundeck instance on kubernetes cluster.

The chart hosted in the repo is based from community [rundeck](https://github.com/helm/charts/tree/master/incubator/rundeck) chart with minor bug fixes.
