helm install --namespace <NAMESPACE> gitlab-runner -f <CONFIG_VALUES_FILE> gitlab/gitlab-runner


helm upgrade gitlab-runner2 \
	--set gitlabUrl=http://192.168.4.44:8929,runnerRegistrationToken=glrt-RUFDkh9xRrbzPXpvrXZ9 \
	gitlab/gitlab-runner



### Check Role 
```sh
kubectl auth can-i create secrets --as=system:serviceaccount:default:gitlab-runner-sa -n default
```
