# FusionCompute安装前置准备

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
# 常识

**X86架构和ARM架构是什么区别?**

- 8086指令集
  IBM:4004升级8086指令集，8:寻址长度
  IBM将8086指令集卖给Intel

- 复杂型指令集`X86指令集`

  英特尔+微软
  不停突破摩尔定理`18个月芯片的能力提升1倍`

- 精简型指令集`包括手机操作系统` `赶超方向突破生态`

  - ARM架构`Advance Reduce Machinee`

    1. 华为鲲鹏处理器 `泰山TaiShan服务器` 

  - BM POWER架构IBMAIX小型机
# Fusioncompute安装部署
**远程管理卡**
<img width="689" height="296" alt="0a4516c3e43589f7b32ee16bba231874" src="https://github.com/user-attachments/assets/3a652908-7880-46b6-a884-6ce2a6dac327" />
 
 `内置mini-os系统，只要服务器通电，即便未按启动电源键，mini-os.依然可以正常访问`

mini-os使用Intel IPMI协议 开源 `Intelligent Platform Management Interface(能平合管理接口)`

 - IBM:RSA远程管理卡

 - HP: ILO2e

 - DELL:DRACe

 - **华为:BMC/IBMC**` (Baseboard Management Controller)e`

   - 所有服务器出厂远程管理口都有一个默认的IP地址，用户名和密码:
   - 默认IP:192.168.2.100

   ​        255.255.255.0

   ​       用户名: Administratore

   ​       密码:Admin@9000

   - **例：**我的笔记本电脑，配置192.168.2.200IP地址，ping通192.168.2.100~通过浏览器访问https://192.168.2.100远程管理这台服务器
   
