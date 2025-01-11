---
layout: post
title: "A tutorial on finding minimum point correspondences between two point sets"
date: 2024-07-24
description: "3D point cloud registration with a focus on minimum point correspondences theoretically"
---



This is a general tutorial for 3D point cloud registration using SVD based closed form approaches with known correspondences.

- The main blog post providing theoretical/geometric justification can be found here: [A tutorial on finding minimum point correspondences between two point sets](https://saishubodh.notion.site/Minimum-point-correspondences-b-w-two-point-clouds-to-solve-for-transformation-between-them-f0d972001496410493a1613b9aada2d3?pvs=4).  
- Code supplements the blog post by providing ipython notebook to play around with: [3D_point-set-registration](https://github.com/Shubodh/3D_point-set-registration)

We also investigate what the minimum number of corresponding points needed is to register two point sets. This problem seems deceptively simple but I couldn't find a clear answer in standard computer vision/robotics texts. Therefore, this post offers a concise answer from multiple perspectives: theoretical, algorithmic and from geometric intuition by going through the original papers from the 1960s.



