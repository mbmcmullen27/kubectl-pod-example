# kubectl-pod-example
kubectl exec from a pod

```sh
# alias k=kubectl

# run blinky server
k run blinky --image=mcmull27/blinky:latest --env PORT=80
k expose pod blinky --port=80

# run alpine image and add curl (or use an image with curl available)
k run curl --image=alpine -- sleep 3000000
k exec curl -- apk add curl

# create service account and run the job
k apply -f sa-role-binding.yaml
k apply -f exec-job.yaml

# log completed job output
k logs kubectl-exec-xxxxx 
```