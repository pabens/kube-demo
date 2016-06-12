# kube-demo

Create a containerized, single node Kubernetes cluster and launch KubeDNS, Dashboard and the 2 tier Guestbook App into it.


## up

1. Create a Kubernetes single local node on OSX docker-machine.
2. Configure kubectl
3. Port forward 8080 between localhost and docker-machine
4. Create KubeDNS
5. Create Kubernetes dashboard
6. Create Guestbook application

```
./up
```


## down

1. Destroy Kubernetes (and ALL running containers!)

```
./down
```


## update

1. Perform a rolling update of the Guestbook application frontend from the initial controller v3 to v4 available from the gcr.io registry

```
./bin/update-gb-frontend
```


## test dns

1. Perform a few test lookups

```
./bin/test-dns
```

# Reference & Credit

[The Guestbook example](http://releases.k8s.io/release-1.1/examples/guestbook/README.md)

[Dashboard](https://github.com/kubernetes/dashboard)

[Running Kubernetes Locally via Docker](http://kubernetes.io/docs/getting-started-guides/docker/)

[Deploying DNS](http://kubernetes.io/docs/getting-started-guides/docker-multinode/deployDNS/)
