 Matlab demo for our CVPR'2019 paper
# [Mapping, Localization and Path Planning for Image-based Navigation using Visual Features and Map](https://arxiv.org/pdf/1812.03795.pdf)

This code was tested in MATLAB R2017b and with [mosek 8.1.0.64](https://www.mosek.com/downloads/).

Please, run the code in 'demo.m' to view our demo.
You have to adjust the path to your mosek directory inside 'demo.m'.

This demo does the following using the concepts introduced in our paper:
1) Find landmarks in a subsequence of the Oxford Robotcar run from  2015-10-29 12:18:17
2) Match a short query sequence from 2014-11-18 13:20:12

The precalculated feature distances in this demo are based on features extracted with a _VGG-16 + NetVLAD + whitening_ network.
We use the _Off-the-shelf on Pitts30k_ model available on the [NetVLAD](https://www.di.ens.fr/willow/research/netvlad/) project page in combination with this [NetVLAD TensorFlow](https://github.com/uzh-rpg/netvlad_tf_open) implementation.   

If you do not have mosek installed, you can have a look at the saved
figures in the results folder instead.

The produced outputs are:
- Scatter plot of original reference and query sequences
- Topology of reference sequence used for finding landmarks with network flow
- Selected landmarks
- Accuracy vs. distance plot of the final matching

