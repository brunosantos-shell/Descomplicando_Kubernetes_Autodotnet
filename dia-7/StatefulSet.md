kubectl exec -ti nginx-0 -- bash
curl nginx-0.ngix.default.svc.cluster.local

hs 

permite a comunicação do pods
servir os statefulset

``` bash 
$ kubectl exec -ti nginx-1 -- bash
root@nginx-1:/# curl nginx-0.nginx.default.svc.cluster.local
giropops-0
root@nginx-1:/# curl nginx-2.nginx.default.svc.cluster.local
<html>
<head><title>403 Forbidden</title></head>
<body>
<center><h1>403 Forbidden</h1></center>
<hr><center>nginx/1.29.4</center>
</body>
</html>

```


k expose deployment nginx

k expose deployment nginx --type NodePort

Simular com o busybox

# Expor um service - usado para tshoot

kubectl expose service --name opa nginx-test --type NodePort
kubectl config set-context --current --namespace=servicos-lab