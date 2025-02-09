# Imagepull back off issue resovle 


If the image we are storing in private registroy then we need to give the cred to pull the image 

````


kubectl create secret generic regcred \
    --from-file=.dockerconfigjson=config.json \
    --type=kubernetes.io/dockerconfigjson

````