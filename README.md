# Kubernetes - With Mongo & Express App
Deployment of mongodb application with mongo-express for GUI access.

Installation STEPS:

Pre-requisities:
	1. Download all the files in your Kubernetes cluster.
	2. You have to specify credentials in secret.yml file . for this follow below steps:

		RUN:
   	#echo -n 'your_root_username' | base64	#(It will give you an output, paste that output in root user )
   	#echo -n 'your_root_password' | base64	#(It will give you an output, paste that output in root password )

Do the same process for Admin user.

Once you done plese run these commands sequence-wise as it is mentioned here : I am talking sequence-wise, reason is there are some dependencies on others so.

	kubectl apply -f secret.yml
 	kubectl apply -f mongodb.yml
  	kubectl apply -f internal-service.yml
  	kubectl apply -f configmap.yml
  	kubectl apply -f external-service.yml
  	kubectl apply -f mongo-express.yml


   Verify with below command: All the Pod & services should 1/1

	kubectl get all -o wide

 Now you can Open you browser, and put Ip of any node with port 30000. Login with your credentials whatever you given in secret.

	 for example: 10.0.0.1:30000

  =======Thanks=========
 	


