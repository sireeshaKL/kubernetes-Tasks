# kubernetes-Tasks
If we need to run this in docker use docker-compose.yml file and no need of app-dep-ser.yaml and db-dep-ser.yaml.

To run the compose file use command docker-compose up.

To run the same in kubenetes we dont need docker-compose.yml file.

Use app-dep-ser.yaml and db-dep-ser.yaml

In app directory build the image for app using command docker build -t imagename .

Give that image name in app-dep-ser.yaml file under container image.

In app-dep-ser.yaml give the image name that docker gives you defaultly while doing docker-compose up.

Then apply the both app-dep-ser.yaml and db-dep-ser.yaml using commands kubectl apply -f app-dep-ser.yaml and kubectl apply -f db-dep-ser.yaml

Check the pods using kubectl get pods and check the logs using kubectl logs podname

Check the services using kubectl get svc

Then in the nodeport given we can see the output.
