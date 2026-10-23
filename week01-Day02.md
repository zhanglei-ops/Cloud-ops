# FusionCompute安装和管理

## 	部署方式建议

- 如果管理的CNA主机超过**50台**，则建议VRM使用物理服务器来部署。
  如果管理的CNA主机不超过50台，为了节省服务器，则VRM可以使用虚拟机来部署。

  `CNA就是一台安装好的Linux欧拉系统，centos，并且部署好的开源的KVM虚拟化 CNA.ISO安装完，KVM也已经自动部署完成。`

## 	部署介质

- 物理服务器部署VRM方式:
  `FusionCompute_VRM-8.5.0.SPC200-X86_64.iso`

- 虚拟化部署流程：
  `FusionCompute_VRM-8.5.0.SPC200-X86_64.zip`

  - 物理部署VRMISO文件 需要LINUX命令行操作

  - 模版文件虚拟化部署VRM模版文件，导入到CNA中，成为一台虚拟机。

    1. 先安装 CNA, 然后在 CNA 中安装`fusioncompute LinuxInstall` 工具

    2. 工具安装完成后，通过web界面将VRM模版导入到CNA中，在CNA中就能运行一台VRM 虚拟机。

       `因为没连共享存储此时VRM部署在CNA本地不能做热迁移`
