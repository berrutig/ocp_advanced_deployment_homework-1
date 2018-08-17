# Red Hat OpenShift - Advanced Deployment Training Homework


## Summary

**Main function**

Ansible file ocphomework.yaml is entry point for the installation configuration, which includes all operational tasks.

1. Set GUID for all hosts 
2. Check docker's status is active
3. Check NFS are shared
4. Install openshift client
5. Create inventory hosts file
6. Execute prerequisites
7. Execute deploy_cluste
8. Check OCP Cluster status
9. Post installation
10. Create PVs
11. Create 25 files for 5G and 10G PVs 
12. Create all PVs for OCP
13. Tagging recycler image
14. Smoke Test
15. CI/CD Test 
16. HPA Test
17. Multitenancy Test

    

**Provisioned Environment Hosts**

* Bastion host: bastion.$GUID.example.opentlc.com, bastion.$GUID.internal

* Load balancer: loadbalancer1.$GUID.example.opentlc.com, loadbalancer1.$GUID.internal

* 3 OpenShift master nodes: master{1,2,3}.$GUID.internal

* 2 OpenShift infrastructure nodes: infranode{1,2}.$GUID.example.opentlc.com, infranode{1,2}.$GUID.internal

* 4 OpenShift worker nodes: node{1-4}.$GUID.internal

* NFS server: support1.$GUID.internal



**Installation**

Clone all scripts from GitHub and install them.

```shell
[xxxx@bastion ~]$ sudo -i
[root@bastion ~]# git clone https://github.com/dawnsky-sina/ocp_advanced_deployment_homework.git
[root@bastion ~]# cd ocp_advanced_deployment_homework
[root@bastion ~]# ansible-playbook ./ocphomework.yaml
```


**Uninstallation**

Uninstallation your environment.

```shell
[root@bastion ~]# sh ./scripts/uninstall.sh
```

