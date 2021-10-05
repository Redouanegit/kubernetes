# kubernetes

## work with pods

```ShellSession

# list all pods in default namespace

kubectl get pods -o=jsonpath='{range .items[*]}{.metadata.name}{"\n"}{end}'

# list all pods with their start date and time in defaut namespace

kubectl get pods -o=jsonpath='{range .items[*]}{.metadata.name}{"\t"}{.status.startTime}{"\n"}{end}'

# list all the Pods deployed in a given node

kubectl get pod --all-namespaces -o jsonpath='{.items[?(@.status.hostIP=="< Node IP >")].metadata.name}'

'''

## work with nodes

```ShellSession

'''

