# netbox-kubernetes
Kubernetes manifest resources for Netbox.  all images are pulled from docker hub. Netbox images pulled from https://hub.docker.com/r/ninech/netbox/


## Quickstart

To get NetBox up and running:

```
$ git clone -b master https://github.com/vishnoisuresh/netbox-kubernetes.git
$ cd netbox-kubernetes
$ kubectl apply -f netbox-namespace.yaml
$ kubectl apply -f postgres-all.yaml
$ kubectl apply -f netbox-all.yaml
$ kubectl apply -f nginx-all.yaml
```

At the moment you can access the application using follwing command. 
```
$ kubectl port-forwarder Nginx-Pod-Name localport:80
```
The application will be available after a few minutes.
"http://localhost:localport"


Default credentials:

* Username: **admin**
* Password: **admin**

## Dependencies
https://hub.docker.com/r/ninech/netbox/

## Configuration

You can configure the app using environment variables. These are defined in `netbox.env`.



## About
This is a living document. If you spot areas that can be improved or rewritten, contributions are welcome! 