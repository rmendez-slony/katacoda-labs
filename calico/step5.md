# Test Calico Network

Lets remove the taint on the master so it can run pods.
`k taint node master node-role.kubernetes.io/master-`{{execute}}

And deploy a simple nginx deployment 
`k run http --image=nginx --replicas=2`{{execute}}

Take a quick look at the Ip's on the pods on node01 and master
`k get pods -o wide`

Lets pull a couple of troubleshooting images
`docker pull busybox`{{execute}}
`docker pull nicolaka/netshoot`{{execute}}
ON BOTH TERMINALSS



docker run -it --net host nicolaka/netshoot



install the calico ctl  I THINK I'LL REMOVE THIS, 
  
     https://docs.projectcalico.org/v3.9/getting-started/calicoctl/install 
  download calicoctl
  chmod
  path

We'll connect to the k8s in the next step
   https://docs.projectcalico.org/v3.9/getting-started/calicoctl/configure/kdd
   
RESOURCES:
https://schoolofdevops.github.io/zero-to-docker/troubleshooting-toolkit/
https://github.com/nicolaka/netshoot
   