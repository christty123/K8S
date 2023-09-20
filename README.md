# K8S
k8s
部署环境的两种方式，目前生产部署Kubernetes集群主要有两种方式
1、kubeadm 
 Kubeadm是一个K8s部署工具，提供kubeadm init和kubeadm join，用于快速部署Kubernetes集群
2、二进制包 
 从github下载发行版的二进制包，手动部署每个组件，组成Kubernetes集群
本方案采用第1种方式搭建
1.1 前期环境准备
服务器要求：
⦁	建议最小硬件配置：2核CPU、2G内存、20G硬盘
⦁	服务器最好可以访问外网，会有从网上拉取镜像需求，如果服务器不能上网，需要提前下载对应镜像并导入节点

软件环境：
软件	版本
操作系统	CentOS7.9_x64 （mini）
Docker	20-ce
Kubernetes	1.26
服务器规划：
角色	IP
k8s-master	192.168.x.71
k8s-node1	192.168.x.72
k8s-node2	192.168.x.73
