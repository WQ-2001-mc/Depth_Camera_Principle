# ToF 深度相机资料

ToF（Time of Flight）通过主动发光并测量往返传播时间获得距离。这里按时间估计方式分成 dToF 和 iToF；“扫描式/Flash 面阵式”是另一条独立的系统形态分类轴。

| 项目 | dToF | iToF |
|---|---|---|
| 直接观测量 | 脉冲到达时间、时间戳或直方图 | 调制光与回波的相关值/相位差 |
| 基本关系 | $R=c\Delta t/2$ | $R=c\phi/(4\pi f_m)$ |
| 常见像素/读出 | SPAD/APD + TDC/TCSPC | 锁相/解调像素，多相相关采样 |
| 典型问题 | 光子散粒噪声、pile-up、死时间、背景光 | 相位缠绕、MPI、多相运动伪影、环境光 |
| 典型形态 | 扫描 LiDAR、Flash LiDAR、稀疏点阵 | 面阵 ToF 相机、AMCW 深度传感器 |

## 子目录

- [dToF](dToF/)：脉冲 ToF 和 SPAD Flash LiDAR 的代表资料；
- [iToF](iToF/)：锁相/相关式 iToF 的代表综述。

正文原理、公式和系统瓶颈见 [深度相机原理介绍](../../深度相机原理介绍.md#4-tof-相机)。
