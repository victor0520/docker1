https://www.qikqiak.com/post/use-kubeadm-install-kubernetes-1.15.3/
https://godleon.github.io/blog/Kubernetes/k8s-Deploy-and-Access-Dashboard/
https://kenwu0310.wordpress.com/2019/01/16/centos-7-%E5%AE%89%E8%A3%9D-kubernetes-%E4%BA%8C-%E5%AE%89%E8%A3%9D-kubernetes-dashboard/
https://www.opencli.com/linux/rhel-centos-7-install-nfs-server#respond
https://www.jianshu.com/p/ac8853927528
$ sudo systemctl enable rpcbind 
$ sudo systemctl enable nfs

https://www.cnblogs.com/wangxu01/articles/11648858.html


kubectl apply -f kubernetes-dashboard.yaml
kubectl apply -f admin-role.yaml

kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin | awk '{print $1}') | grep token: | awk -F : '{print $2}' | xargs echo

https://172.16.1.101:30310/#!/login