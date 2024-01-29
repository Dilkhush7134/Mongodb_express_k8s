# Kubernetes - With Mongo & Express App
Deployment of mongodb application with mongo-express for GUI access 

Create a MongoDB Deployment:
		mongodb.yml

	#In the mongodb.yml, we have specified "mongo" as an image, so it will fetch the latest mongo image from the docker hub.
	#Here we need two ENVIRONMENT Variable. 
MONGO_INITDB_ROOT_USERNAME & MONGO_INITDB_ROOT_PASSWORD
To get these values we will create a Secret from where we will reference that value.

secretKeyRef.name : specifies the name of the secret (which we have defined in Step 2)

secretKeyRef.key : specifies the key name which we have declared under the data section in Step 2.

Please note: Secret must be created before the deployment because this deployment step has dependency over the Secret step.

