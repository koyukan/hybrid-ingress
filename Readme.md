Using Ingress Group, load balance accross namespaces.
Single Ingress instance routing to both Fargate Pods with target-type: ip and Regular Pods with target-type: instance

App 1: Deployed on Default Namespace using Nodeport Service
    alb.ingress.kubernetes.io/target-type: instance
App 2: Deployed on Fargate Namespace using ClusterIP Service
    alb.ingress.kubernetes.io/target-type: ip
    namespace: fp-ns-app1  
App 3: Deployed on Fargate Namesapce using ClusterIP Service
    alb.ingress.kubernetes.io/target-type: ip 
    namespace: fp-ns-app1  