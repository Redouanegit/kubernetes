# kubernetes

## work with pods

```ShellSession

# list all default namespace pods

kubectl get pods -o=jsonpath='{range .items[*]}{.metadata.name}{"\n"}{end}'

# list all defaut namespace pods with their start datetime 

kubectl get pods -o=jsonpath='{range .items[*]}{.metadata.name}{"\t"}{.status.startTime}{"\n"}{end}'

# list all the Pods deployed in a given node

kubectl get pod --all-namespaces -o jsonpath='{.items[?(@.status.hostIP=="< Node IP >")].metadata.name}'




