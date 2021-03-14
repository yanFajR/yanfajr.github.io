---
published: true
layout: post
categories:
  - Kubernetes
---
Kubernetes adalah software open source untuk automation deployment, scalling, dan menanjemen container. kubernetes adalah yang paling populer saat ini untuk software yang sejenis dengannya.

Alur kerja kubernetes, yang pertama kita mendefinisikan config file yang berisi container apa saja, jumlah node, pemakaian cpu, memori, dll. lalu config dikirim ke kubernetes master untuk mengelola config file, lalu akan dikerjakan kubernetes workers.

### Faktor mempengaruhi menggunakan kubernetes
1. perubahan konsep deploy apps yang awalnya monolit menjadi microservice yang tentu memiliki tantang yang lebih bagi seorang operasional engineer.
2. perubahan tren dari awalnya menggunakan full virtualisasi ke konsep containers.

## Arsitektur

**kubernetes cluster :** 

![post-ccm-arch.png]({{site.baseurl}}/images/post-ccm-arch.png)

- **Kubernetes Master**
  - **kube-apiserver**, sebagai api untuk berinteraksi dengan kubernetes cluster
  - **etcd**, sebagai database kubernetes cluster
  - **kube-scheduller**, monitoring container berjalan dan meminta kepada node untuk menjalankan container
  - **kube-control-manager**, kontrol terhadap kubernetes cluster
  - **cloud-control-manager**, kontrol terhadap interaksi dengan cloud provider
  
- **Kubernetes Nodes**
  - **kubelet**, ada pada setiap node untuk memastikan container berjalan
  - **kube-proxy**, ada pada setiap node untuk proxy terhadap arus network dan sebagai load balancer
  - **container-manager**, contohnya docker
  
## Install

Pada windows
1. Install minikube
   - Download [https://github.com/kubernetes/minikube/releases/tag/v1.18.1](https://github.com/kubernetes/minikube/releases/tag/v1.18.1)
   - Install exe file
   - minikube start
   
     ![minikube start.PNG]({{site.baseurl}}/images/minikube start.PNG)

   - 


