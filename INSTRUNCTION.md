Застосуй ресурси:
kubectl apply -f configMap.yml
kubectl apply -f secret.yml
kubectl apply -f deployment.yml
	8.	Перевір наявність ConfigMap:
kubectl get configmap python-config -o yaml
	9.	Перевір наявність Secret:
kubectl get secret app-secret -o yaml
	10.	Перевір, чи змінні присутні в контейнері:
kubectl exec -it  – printenv | grep PYTHONUNBUFFERED
kubectl exec -it  – printenv | grep SECRET_KEY
	11.	Перевір, що застосунок успішно стартує без помилок з логів:
kubectl logs 