# Kubernates-master-configuration

# For /etc/kubernetes file you need to change apiserver file and config file.

# you need to make changes into /etc/etcd file 

#These are the setting that you need to change for master kubernates configuration.


#Commands for Autoscale:

#kubectl run myautoscale --image=latest123/apache --port 80 --labels=app=myautoscale

#kubectl get pods

#kubectl get deployment

#kubectl autoscale deployment myautoscale --min=2 --max=6 --cpu-percent=80

#autoscale deployment myautoscale --min=1 --max=6 --cpu-percent=80
#Error from server (AlreadyExists): horizontalpodautoscalers.autoscaling "myautoscale" already exists

#kubectl autoscale deployment myautoscale --min=4 --max=6 --cpu-percent=80
#Error from server (AlreadyExists): horizontalpodautoscalers.autoscaling "myautoscale" already exists

#if you face above issue then use scale.

#kubectl scale --current-replicas=2 --replicas=4 deployment/myautoscale


#you can see four instance in your Minion(nodes)
#=====================================================================================================================

# By using scale you can change your replicas by following command, previously our replicas was 4, So we will change it to 2

#kubectl scale --current-replicas=4 --replicas=2  deployment/myautoscale

