---
layout: publication
sitemap: false
title: "SEMICON: A Learning-to-hash Solution for Large-scale Fine-grained Image Retrieval"
authors: Yang Shen, Xuhao Sun, Xiu-Shen Wei, Qing-Yuan Jiang, Jian Yang
pdf: ECCV2022_SEMICON
image: ECCV2022_SEMICON.jpg
display: Proceedings of the European Conference on Computer Vision
display_short: ECCV
year: 2022
github: 
learning2hash: true
fine_grained_retrieval: true
abstract: "In this paper, we propose Suppression-EnhancingMask based attention and Interactive Channel transformatiON (SEMICON) to learn binary hash codes for dealing with large-scale fine-grained image retrieval tasks. In SEMICON, we first develop a suppression-enhancing mask (SEM) based attention to dynamically localize discriminative image regions. More importantly, different from existing attention mechanism simply erasing previous discriminative regions, our SEM is developed to restrain such regions and then discover other complementary regions by considering the relation between activated regions in a stage-by-stage fashion. In each stage, the interactive channel transformation (ICON) module is afterwards designed to exploit correlations across channels of attended activation tensors. Since channels could generally correspond to the parts of finegrained objects, the part correlation can be also modeled accordingly, which further improves fine-grained retrieval accuracy. Moreover, to be computational economy, ICON is realized by an efficient two-step process. Finally, the hash learning of our SEMICON consists of both globaland local-level branches for better representing fine-grained objects and then generating binary hash codes explicitly corresponding to multiple levels. Experiments on five benchmark fine-grained datasets show our superiority over competing methods. Codes are available at https://github.com/NJUST-VIPGroup/SEMICON."
---
