## Kubernetes example hello-app by using helm

This repository includes Kubernetes example with deployment and LoadBalancer service by using helm.
* hello-app deployed by using helm with deployment/replicas:3
	* hello-app image: gcr.io/google-samples/hello-app:2.0
* Expose the service and test it with the curl request: curl http://<ip address of exposed service>:8080
	* LoadBalancer service used
* In order to test with curl
	* curlimages/curl:7.78.0 image is used which includes curl inside
	* command `curl http://k8s-hello-app.fullname:8080` is used
	* test yaml file is in k8s-hello-app\templates directory
