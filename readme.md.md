
# Purpose
1. The purpose of this lab excerise is to minc the same environment setup on premise.
2. We are using an external database as the soa repository.
3. We are installing k8 from scratch. In this lab however we are not creating a HA for master node. We can refer to K8 documentation on how to set it up.
4. For lab purpose we are using 1 master and 1 worker. Deployment are done in worker node as master are not tainted to run workload.
5. Since soa on k8 require a PV/PVC, in on prem context it will either a NFS or san storage etc. In this lab we are using Oracle Cloud File System to act as the NFS.


# 1. Prereq
1. Please follow the prereq to set your environment ready.  Follow the instruction on [prereq](https://github.com/wenjian80/soak8_labs/blob/main/tutorial/prereq.md)

2. You should already have your labinfo.txt fill up on hand. We will be referencing those info in these exercise.

# 2. Version Tested
1.  [Oracle Linux 7.9 OCI Iaas Image](https://docs.cloud.oracle.com/en-us/iaas/images/)
2. [Docker version 19.03.1.ol](https://docs.docker.com/engine/release-notes/)
3. [Kubernetes 1.18.4-1](https://kubernetes.io/docs/setup/)
4. [Helm 3.4.1](https://helm.sh/)
5. [Oracle Dbaas 19.9.0.0.0](https://docs.oracle.com/en/database/oracle/oracle-database/)
6. [Weblogic Operator 3.0.1 ](https://github.com/oracle/weblogic-kubernetes-operator.git)
7. [FMW Kubernetes 20.3.3 ](https://github.com/oracle/fmw-kubernetes.git)
8. [Kube-Prometheus 0.6.0](https://github.com/prometheus-operator/kube-prometheus/tree/master)
9. [Oracle SOA 12.2.1.4 container registry ](https://container-registry.oracle.com/pls/apex/f?p=113:4:106885074376611:::4:P4_REPOSITORY,AI_REPOSITORY,AI_REPOSITORY_NAME,P4_REPOSITORY_NAME,P4_EULA_ID,P4_BUSINESS_AREA_ID:252,252,Oracle%20SOA%20Suite,Oracle%20SOA%20Suite,1,0&cs=3xzEuKbyTjyKLe-4Re2u8kpgzYt9IeGor4rR9qoIDbXZAjmMArQ6_1td_9Ms5dAmFpfbfEjpHiKmLbB9VfMsTBQ)
10. [Traefik chart 1.87.7/ App 1.7.26](https://github.com/helm/charts/blob/master/stable/traefik/Chart.yaml) 

# 3. Lab steps
TODO to explain steps

1. Excercise are running as root for lab purpose. Login to as opc, sudo su.
2. Clone this git project.
3. Create a folder call soak8_lab in both master and worker node in path /home/opc/
4. Winscp and copy the scripts folder into /home/opc/soak8_lab/scripts
5. sudo su 
6. chmod -R 777 /home/opc/soak8_lab


## Step 0: 0_InitialMachine_Config.sh
**[Run on master and worker node]**

1. This script need to run on both master and worker node.
2. We are setting up the yum repository in this script So the installation will make use the of the yum repository.

## Step 1: 1_Docker_Config.sh
**[Run on master and worker node]**

1. This script need to run on both master and worker node.
2. We are using dokcer version 19.03.1.ol
## Step 2: 2_KubeMaster_Firewall_Config.sh
**[Run on master node ONLY]**

## Step 3: 3_KubeNode_Firewall_Config.sh
**[Run on worker node ONLY]**

## Step 4: 4_KubeMaster_Kubernetes_Config.sh
**[Run on master node ONLY]**

## Step 5: 5_KubeNode_Kubernetes_Config.sh
**[Run on worker node ONLY]**

## Step 6: 6_Check_Kubedns.sh
**[Run on master node ONLY]**

## Step 7: 7_Kube_proxy.sh
**[Run on master node ONLY]**

## Step 8: 8_Git_helm.sh
**[Run on master node ONLY]**

## Step 9: 9_Operator.sh
**[Run on master node ONLY]**

## Step 10: 10_Rcu.sh
**[Run on master node ONLY]**

## Step 11: 11_Soa_secret.sh
**[Run on master node ONLY]**

## Step 12: 12_Mount_File.sh
**[Run on master and worker node]**

## Step 13: 13_Soa_pv.sh
**[Run on master node ONLY]**

## Step 14: 14_Soa_DomainJob.sh
**[Run on master node ONLY]**

## Step 15: 15_Soa_DomainConfig.sh
**[Run on master node ONLY]**

## Step 16: 16_Traefik_LB.sh
**[Run on master node ONLY]**


## Step 17: 17_Prom_Gra.sh
**[Run on master node ONLY]**

## Step 18: 18_Prom_Setting.sh
**[Run on master node ONLY]**


# Reference Links

TODO
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NDc4OTcyODAsMTI5NTU3MTM1N119
-->