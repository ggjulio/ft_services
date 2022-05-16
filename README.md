## Disclaimer:
This project has been removed from our cursus for several reasons.  
First one, k8s is too hard for an introduction to containers...  
Second, the subject was not great.

# ft_services

- http://phusion.github.io/baseimage-docker/
- https://medium.com/@codingwithmanny/configure-self-signed-ssl-for-nginx-docker-from-a-scratch-7c2bcd5478c6
- https://hub.docker.com/_/nginx
- https://hub.docker.com/_/mysql   
- https://wiki.alpinelinux.org/wiki/MariaDB   
- https://mariadb.com/kb/en/running-mysqld-as-root/    
- https://cloud.google.com/solutions/best-practices-for-building-containers
- https://cloud.google.com/solutions/best-practices-for-operating-containers
- https://rtfm.co.ua/en/kubernetes-clusterip-vs-nodeport-vs-loadbalancer-services-and-ingress-an-overview-with-examples/ 

- https://medium.com/kubernetes-costa-rica/kubernetes-nodeport-vs-loadbalancer-vs-ingress-cuando-usar-cu%C3%A1l-5930df5619c



- https://github.com/kelseyhightower/kubernetes-the-hard-way

#### metallb

- https://medium.com/faun/metallb-configuration-in-minikube-to-enable-kubernetes-service-of-type-loadbalancer-9559739787df
- https://medium.com/@shoaib_masood/metallb-network-loadbalancer-minikube-335d846dfdbe  
- https://metallb.universe.tf/installation/

#### other
- https://www.redhat.com/cms/managed-files/cm-oreilly-kubernetes-patterns-ebook-f19824-201910-en.pdf
- http://www.projectatomic.io/docs/docker-image-author-guidance/

#### dockerfile : Entrypoints + CMDs + Signals and processes
- https://stackoverflow.com/questions/39082768/what-does-set-e-and-exec-do-for-docker-entrypoint-scripts
- https://stackoverflow.com/questions/32255814/what-purpose-does-using-exec-in-docker-entrypoint-scripts-serve/32261019#32261019
- https://stackoverflow.com/questions/50898134/what-does-docker-stopsignal-do
- https://hynek.me/articles/docker-signals/
- https://ubuntu.com/blog/avoiding-dropped-connections-in-nginx-containers-with-stopsignal-sigquit
- https://stackoverflow.com/questions/36781372/docker-using-gosu-vs-user
- https://docs.docker.com/develop/develop-images/dockerfile_best-practices/
- https://stackoverflow.com/questions/50319492/difference-between-and-set-ex-in-dockerfiles
- https://gist.github.com/mohanpedala/1e2ff5661761d3abd0385e8223e16425
- https://github.com/koalaman/shellcheck/issues/1489
- https://coderwall.com/p/fkfaqq/safer-bash-scripts-with-set-euxo-pipefail
- https://www.freebsd.org/cgi/man.cgi?query=sh&sektion=&n=1
- https://stackoverflow.com/questions/40547032/bash-read-returns-with-exit-code-1-even-though-it-runs-as-expected
#### MYSQL

- https://hub.docker.com/_/mysql
- https://github.com/docker-library/mysql/blob/master/8.0/Dockerfile
- https://github.com/docker-library/mariadb/blob/master/10.5/Dockerfile
- https://github.com/docker-library/mysql/blob/master/8.0/docker-entrypoint.sh
- https://github.com/docker-library/mariadb/blob/master/10.5/docker-entrypoint.sh
- https://mariadb.com/kb/en/installing-system-tables-mysql_install_db/
- https://dev.mysql.com/doc/refman/5.6/en/mysql-install-db.html
- https://mariadb.com/kb/en/configuring-mariadb-for-remote-client-access/
- https://stackoverflow.com/questions/14779104/mysql-how-to-allow-remote-connection-to-mysql
- https://success.mirantis.com/article/use-a-script-to-initialize-stateful-container-data
- https://unix.stackexchange.com/questions/265149/why-is-set-o-errexit-breaking-this-read-heredoc-expression/265151
- https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/

#### phpmyadmin
- https://www.nginx.com/resources/wiki/start/topics/examples/likeapache/
- https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/
- https://serverfault.com/questions/379675/nginx-reverse-proxy-url-rewrite?rq=1
- https://stackoverflow.com/questions/54700282/nginx-reverse-proxying-to-https-upstream-getting-502-bad-gateway

http2 not supported by nginx as backend server (for reverse proxy)
- https://serverfault.com/questions/765258/use-http-2-0-between-nginx-reverse-proxy-and-backend-webserver

- https://docs.nginx.com/nginx/admin-guide/security-controls/securing-http-traffic-upstream/
- https://stackoverflow.com/questions/24520540/nginx-does-redirect-not-proxy
- https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy 
#### pod : php + nginx
- https://medium.com/@marekbartik/autoscale-nginx-and-php-fpm-independently-on-google-kubernetes-engine-290aead64f7f
- https://cloud.google.com/kubernetes-engine/docs/concepts/cluster-architecture
- https://cloud.google.com/kubernetes-engine/docs/tutorials/persistent-disk
- https://github.com/kubernetes/examples
- https://cloud.google.com/endpoints/docs/openapi/custom-nginx
- https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/
- https://www.nginx.com/resources/wiki/start/topics/recipes/wordpress/
- https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/
## configmap and volume to avoid custom image
- https://cloud.google.com/endpoints/docs/openapi/custom-nginx
- https://stackoverflow.com/questions/64178370/custom-nginx-conf-from-configmap-in-kubernetes
- https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#populate-a-volume-with-data-stored-in-a-configmap
- https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#populate-a-volume-with-data-stored-in-a-configmap
- https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#add-configmap-data-to-a-specific-path-in-the-volume
- https://unofficial-kubernetes.readthedocs.io/en/latest/tasks/configure-pod-container/configmap/
- > https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-initialization/
- https://kubernetes.io/docs/concepts/workloads/pods/init-containers/
- https://medium.com/hackernoon/mount-file-to-kubernetes-pod-without-deleting-the-existing-file-in-the-docker-container-in-the-88b5d11661a6
## Using docker driver, create a network for metallb

warning: if u have run `eval $(minikube docker-env)`. All commands will not be executed in the host...(check with `docker ps`...) -> `eval $(minikube docker-env --unset)`
#### docker network
- check network that already exist `Docker network ls`
If u already started you should see a network called `minikube`. The minikube ip is on this network.
https://docs.docker.com/network/

- Create a new network for setting up externals ip for your settings.
`docker network create my-network --driver=bridge`
`docker network inspect my-network`
`IPAM.Config.Subnet` is the subnet you should use inside your metallb config.
- connect this network to the minikube container:
`docker network connect my-network minikube` (`minikube` == alias to minikube container ->`docker ps`)
`docker network inspect my-network` -> the minikube container should be added...

- Configure metallb
My `IPAM.Config.Subnet`is`172.18.0.0/16` so I given range `.0.10`-`0.20` to metallb

Instead of all this steps. We can choose ourself the subnet:
```bash
docker network create --subnet=172.20.0.0/16 my-net
docker network connect my-net minikube
```

#### Persistent storage
- https://docs.openshift.com/container-platform/4.1/storage/understanding-persistent-storage.html#persistent-storage-overview_understanding-persistent-storage
- https://docs.openshift.com/container-platform/4.1/nodes/containers/nodes-containers-volumes.html#nodes-containers-volumes-subpath_nodes-containers-

#### defployment strategy
- https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#strategy
- https://docs.openshift.com/container-platform/3.3/dev_guide/deployments/deployment_strategies.html
- https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/

#### service networking and network beyond cluster
- https://kubernetes.io/docs/concepts/services-networking/service/#defining-a-service
- https://metallb.universe.tf/concepts/
- https://metallb.universe.tf/concepts/layer2/
- https://metallb.universe.tf/concepts/bgp/

- https://kubernetes.io/docs/concepts/services-networking/ingress/
- https://www.stackrox.com/post/2020/01/kubernetes-networking-demystified/

# telegraf
- https://docs.wavefront.com/nginx.html
- https://github.com/influxdata/telegraf/blob/master/docs/CONFIGURATION.md
- https://kubernetes.io/docs/tasks/administer-cluster/access-cluster-api/
- https://sysdig.com/blog/how-to-monitor-kubelet/
- https://www.influxdata.com/blog/scaling-kubernetes-deployments-influxdb-flux/
##### inputs.kubernetes deprecated. And not working...
- https://github.com/influxdata/telegraf/issues/6959
- https://kubernetes.io/docs/concepts/cluster-administration/system-metrics/
- https://docs.influxdata.com/platform/integrations/kubernetes/#collect-kubernetes-metrics-with-telegraf
- https://stackoverflow.com/questions/58911806/how-to-expose-kubernetes-metric-server-api-to-curl-from-inside-the-pod
- https://github.com/influxdata/telegraf/issues/6959
- https://github.com/influxdata/telegraf/tree/master/plugins/inputs/kubernetes
