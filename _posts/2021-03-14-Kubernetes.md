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


