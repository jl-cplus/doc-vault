# MyDebit DR Exercise Guide
This note is intended solely for APSB to perform the MyDebit DR exercise.  
  
> [!CAUTION]
> Ensure you are using the correct Kubernetes context.  
  
## Log Monitoring Command
```
$ kubectl -n mydebit logs -f --tail=500 host-api-0
```
> Note: The log output contains `RC: 00`, which indicates that the system is functioning as BAU.  
  
## Scale ReplicaSet Command
  
#### To scale down the StatefulSet host-api to zero replicas
```
$ kubectl -n mydebit scale --replicas=0 sts/host-api  
```
  
#### To scale up the StatefulSet host-api back to one replica
```
$ kubectl -n mydebit scale --replicas=1 sts/host-api
```
  