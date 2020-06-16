# kubernetes-ingress
Codebunk URl :https://codebunk.com/b/5751100113469/
Why ingress is used :
Suppose Lets consider we have 4 application that running so for these 4 application we require 4 SVC(services) and that services are talking to the number of nodes present hence we require that much of IP Addresses (for example 4 nodes 5 services 4*5=20 ip required).
hence nodeport doesn't feasible like there is lot's of trafiic and we can't depend on Nodeport.

Now suppose why we use Services :
1) Avoid failure
2) To access applicatoin outside the cluster
3) Virtual IP (If my pod gets down and then new pod is created by deploment and that created pod has different ip hence through service we assigned only one ip)

        I Attached Both the scenarios that are feasible to differentiate between Nodeport and Ingress 
        In Ingress We doesn't require lot's of IP address infact the end user access the applications only using one port and doesn't require different Ip's for different application as end user only talk with INgress Controller and Ingress contraoller talk to the Service and service to pod(pod is similar to container we just say pod instead of container)
        
        Bookish Details :
                            Ingress exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. Traffic routing is controlled by rules defined on the Ingress resource.An Ingress may be configured to give Services externally-reachable URLs, load balance traffic, terminate SSL / TLS, and offer name based virtual hosting. An Ingress controller is responsible for fulfilling the Ingress, usually with a load balancer, though it may also configure your edge router or additional frontends to help handle the traffic.  An Ingress does not expose arbitrary ports or protocols. Exposing services other than HTTP and HTTPS to the internet typically uses a service of type Service.Type=NodePort or Service.Type=LoadBalancer.


I Attache the Commands in Command file :)

