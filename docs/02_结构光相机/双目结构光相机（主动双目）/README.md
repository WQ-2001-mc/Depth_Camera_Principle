# 主动双目资料导航

主动双目的核心判据是：两个相机观察同一场景，深度主要由左右视图的对应关系和视差计算；投影器用于给弱纹理表面增加或编码可匹配特征。

本目录按“投影纹理”分组，便于对比，不表示主动双目只有两种严格且互斥的物理类别：

- [散斑与随机纹理](散斑与随机纹理/)：伪随机点阵、散斑状图案、优化二值纹理等，通常可以单帧完成左右匹配；
- [条纹与编码纹理](条纹与编码纹理/)：单线、平行条纹、格雷码、相移正弦条纹等，通常需要唯一编码或多帧投影来消除周期歧义。

工程上还可使用网格、彩色编码、De Bruijn 图案和学习式投影图案。若系统主要解码“相机像素—投影器像素”的对应关系并以相机—投影器为三角测量基线，则更准确地归为结构光；若再融合左右视差，则属于混合系统。

## 代表资料

1. [Intel RealSense Stereoscopic Depth Cameras](散斑与随机纹理/2017_Keselman_RealSense_Stereoscopic_Depth_Cameras.pdf)：散斑状/随机红外纹理增强的量产主动双目系统；
2. [High-Accuracy Stereo Depth Maps Using Structured Light](条纹与编码纹理/2003_Scharstein_Szeliski_High_Accuracy_Stereo_Structured_Light.pdf)：格雷码与正弦条纹辅助双视图对应和视差融合的经典论文。
