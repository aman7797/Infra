OpenShift Commands:
 
5.  oc new-app . --strategy=docker  --name mysample
6.  oc start-build java --from-dir .
7.  oc get svc/docker-registry -o yaml | grep clusterIP:
8.  oc delete all --selector app=centos
9.  oc adm policy add-scc-to-user anyuid -z default -n project-name
10. oc login -u system:admin
11. oc create -f nfs-pv.yaml
12. oc create -f nfs-claim.yaml
13. oc expose svc/centos --hostname centos.apps.10.20.14.183.xip.io