# Conv-BN-fuse
融合Conv和BN层原理解释https://zhuanlan.zhihu.com/p/110552861
使用前需要预先准备好训练好的权重文件（如本例中skynet.weights）
在Conv_bn.py中，fuse()与fuse_g()分别为普通conv与bn的融合函数及depsewise层与bn的融合函数
在融合过程中，需要先将网络权重加载入原有网络，然后在此基础上对原有网络需要融合的层进行融合，最后保存权重即可(如本例中ConvBnFuse.weights)
