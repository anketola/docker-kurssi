# Exercise 3.7

*Chosen alternative: a) Write a short (200-300 words) text/article on why and when to use Kubernetes. You can compare it to other similar tools.*

Kubernetes provides automation for container management. The benefits with Kubernetes and the management of multiple nodes include that it’s able to ensure application resilience by monitoring enough nodes are up in case some were to fail. Additionally, Kubernetes can aid in adjusting to increased workload. Hence, it provides automated scalability. The official Kubernetes documentation lists additional features such as automated rollouts and rollbacks and secret and configuration management.

The need to use Kubernetes, and expand from using only for instance Docker, may rise from need to scale up the application due to increasing traffic. According to an article by DZone, high traffic volume has been one of the main reasons for the adoption of Kubernetes for sites and applications such as Tinder, Reddit and Pokemon Go. That being said, there doesn’t seem to be much benefit in running an orchestration system such as Kubernetes in a small-scale setting.

However, Kubernetes doesn’t seem to be unique, and has an array of alternatives. Apparently, Kubernetes isn’t the easiest one to use, and some of the alternatives have tried to remedy the situation. Alternatives orchestration solutions include Docker Swarm, Nomad and Kontena. With Docker Swarm, one of the benefits seems to be that if one already is somewhat familiar with Docker, the learning curve shouldn’t be that steep. In comparison, it seems that Kubernetes is considered as more robust and customizable solution, whereas Docker Swarm is considered a rapid, simple way of deployment with perhaps at the cost of the same level of reliability Kubernetes could offer at peak level.


References used:

* https://kubernetes.io/
* https://containerjournal.com/2019/01/14/kubernetes-vs-docker-a-primer/
* https://dzone.com/articles/how-big-companies-are-using-kubernetes
* http://techgenix.com/kubernetes-alternatives/
* https://en.wikipedia.org/wiki/Kubernetes
* https://dev.to/totalcloudio/docker-swarm-vs-kubernetes--what-you-really-need-to-know--4kjb
