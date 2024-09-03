---
layout: publication
sitemap: false
title: "ExchNet: A Unified Hashing Network for Large-Scale Fine-Grained Image Retrieval"
authors: Quan Cui, Qing-Yuan Jiang*, Xiu-Shen Wei, Wu-Jun Li, Osamu Yoshie
pdf: ECCV2020_ExchNet
image: ECCV2020_ExchNet.jpg
display: Proceedings of the European Conference on Computer Vision
display_short: ECCV
year: 2020
github: 
learning2hash: true
fine_grained_retrieval: true
abstract: "Retrieving content relevant images from a large-scale fine-grained dataset could suffer from intolerably slow query speed and highly redundant storage cost, due to high-dimensional real-valued embeddings which aim to distinguish subtle visual differences of fine-grained objects. In this paper, we study the novel fine-grained hashing topic to generate compact binary codes for fine-grained images, leveraging the search and storage effciency of hash learning to alleviate the aforementioned problems. Specifically, we propose a unified end-to-end trainable network, termed as ExchNet. Based on attention mechanisms and proposed attention constraints, ExchNet can firstly obtain both local and global features to represent object parts and the whole fine-grained objects, respectively. Furthermore, to ensure the discriminative ability and semantic meaning's consistency of these part-level features across images, we design a local feature alignment approach by performing a feature exchanging operation. Later, an alternating learning algorithm is employed to optimize the whole ExchNet and then generate the final binary hash codes. Validated by extensive experiments, our ExchNet consistently outperforms state-of-the-art generic hashing methods on five fine-grained datasets. Moreover, compared with other approximate nearest neighbor methods, ExchNet achieves the best speed-up and storage reduction, revealing its efficiency and practicality."
---
