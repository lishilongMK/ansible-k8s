# 原作者地址：[https://github.com/gjmzj/kubeasz](https://github.com/gjmzj/kubeasz)

## 该脚本暂时只适用于kubernetes1.9.x版本，如果装10的话可能会成功，但是需要调整好多地方


# 利用Ansible部署kubernetes集群

**注意：** 为提高集群网络插件安装的灵活性，使用`DaemonSet Pod`方式运行网络插件，目前支持`Calico` `flannel`可选

文档基于`Ubuntu 16.04/CentOS 7`，其他系统需要读者自行替换部分命令；由于使用经验有限和简化脚本考虑，已经尽量避免`ansible-playbook`的高级特性和复杂逻辑。




## 组件版本

1. kubernetes	v1.9.x
1. etcd		v3.2.13
1. docker	17.12.0-ce
1. calico/node	v2.6.5
1. flannel	v0.9.1

+ 集群用到的所有二进制文件已打包好供下载 [公司的ftp： http://ftp.km.co-mall/pf/kubernetes](http://ftp.km.co-mall/pf/kubernetes/k8s.196.tar.gz)


## 快速指南

单机快速体验k8s集群的测试、开发环境--[AllinOne部署](docs/quickStart.md)；在国内的网络环境下要比官方的minikube方便、简单很多。


1. 建议阅读 [rootsongjc-Kubernetes指南](https://github.com/rootsongjc/kubernetes-handbook) 原理和实践指南。
1. 建议阅读 [feisky-Kubernetes指南](https://github.com/feiskyer/kubernetes-handbook/blob/master/SUMMARY.md) 原理和部署章节。
1. 建议阅读 [opsnull-安装教程](https://github.com/opsnull/follow-me-install-kubernetes-cluster) 二进制手工部署。



