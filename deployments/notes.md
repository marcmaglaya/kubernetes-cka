kubectl create deployment webapp --image kodekloud/webapp-color --replicas=3


kubectl expose pod valid-pod --port=444 --name=frontend