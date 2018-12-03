# Conanos CI enviroment
Conanos CI enviroment is objective to provide facility 


This repository is objective to provide facilities to help build conanos packages on build,verify and manage in local enviroment.

To complete build job of conanos, we may need docker, python, nodejs ... package, so a lot of downloading from internet would happened, so we have to setup native mirror or source for the build to improve the speed of build. Here is list of component for the CI envirment, here we assume host name is vss.kedacom.com



 * Docker Image

   currently we have to manual pull docker image from hub.docker.com or elsewhere, then public in local registry

   third part pull images list [TBD](./docker-registry/docker.list) 

   location: http://vss.kedacom.com/ci/docker-registry

 * Vagrant Box
   
   has to be published via http as we have no vargant box server tools

   location: http://vss.kedacom.com/ci/vagrant

 * pypi
   
   pypiserver or others to be investigation

   location: http://vss.kedacom.com/ci/pypi

 * npm
   sinopia  or others to be investigation
   
   location: http://vss.kedacom.com/ci/npm

 * Git
   use gitlab 

   location: http://vss.kedacom.com/ci/gitlab
   status: done http://172.16.64.65/

 * conan
   use [jfrog open source solution](https://jfrog.com/open-source/#os-arti)

   location: http://vss.kedacom.com/ci/conan

   note: some bincrasters conan-communit package need to be sync

   http://172.16.64.65:8081/artifactory
   


 * Ubuntu Native mirror
   
   apt-mirror

   (ubuntu) location: http://vss.kedacom.com/ci/mirror/ubuntu
   (centos)  location: http://vss.kedacom.com/ci/mirror/centos (TO DO later)

All above serverice may not able to run in a host, we plan to use a nigix to redirecto to the node, nginx openresty would have ben used.