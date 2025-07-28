az account show
az account show --query id -o tsv
az ad sp create-for-rbac \
  --name "badclick-tf" \
  --role="Contributor" \
  --scopes="" \
  --sdk-auth

az aks get-credentials \
  --resource-group badclick-infrastructure-rg \
  --name badclick-org-aks \
  --file kubeconfig-badclick