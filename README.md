# Docker and Kubernetes Complex Project

This project is from Stephen Grider's course on Udemy - [Docker and Kubernetes: The Complete Guide](https://www.udemy.com/course/docker-and-kubernetes-the-complete-guide/)

## Project

### Launching Kubernetes

`kubectl apply -f k8s`

### Launching Kubernetes Dashboard

`kubectl proxy`

Get token:

```
kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}')
```

Open dashboard at

```
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/overview?namespace=default
```

### Launching Docker

Create symbollic links from the travis-aws directory at the top level. i.e.:

```
ln -s travis-aws/Dockerrun.aws.json
ln -s travis-aws/docker-compose.yml
```

### Contributing

You are welcome to contribute provided you accept the [Contributor Covenant Code of Conduct](CONTRIBUTING.md).

That being said, these are my notes from when I did the course, so maybe you just want to clone and keep your own changes? I won't mind, but I'm always open to learning new things.

### Versioning

This project uses [Semantic Versioning 2.0.0](http://semver.org/). Please see [tags on this repository](https://github.com/your/project/tags).

### License

This repository is licensed under [The Unlicense](LICENSE.md).

### Acknowledgements

- Stephen Grider is an excellent instructor. I highly recommend this course. It is not free, but I found the education well worth the price of admission.
- [WebUI (Dashboard)](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)
- [The Ultimate Guide to the Kubernetes Dashboard: How to Install and Integrate Metrics-server](https://www.replex.io/blog/the-ultimate-guide-to-the-kubernetes-dashboard-how-to-install-and-integrate-metrics-server)
