# Build
operator-sdk build quay.io/saberkan/namespaceconfig:v0.0.1

# Publish
docker push quay.io/saberkan/namespaceconfig:v0.0.1

# Deploy
oc create -f deploy/crds/namespaceconfig.ei.com_namespaceconfigs_crd.yaml
oc create -f deploy/operator.yaml
