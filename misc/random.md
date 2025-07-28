# to be sorted later

docker run --rm -v $(pwd):/project aquasec/trivy config /project

# view current configuration, including user
kubectl config view --minify

# see what permissions I have
kubectl auth can-i --list

# see what user is in k8s
kubectl config view --minify -o jsonpath='{.users[0].name}'

# can i do an action?
kubectl auth can-i create pods
kubectl auth can-i delete clusterrolebindings

# check requirements to install flux
flux check --pre

#
