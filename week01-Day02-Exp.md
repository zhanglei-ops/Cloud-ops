- - # 实验步骤

    ##     实验目标

    - [ ] **安装两台CNA**：CNA01&CNA02

      ​    CNA 初始化：

    ​	登录CNA01&02
    ​	用户名和密码是之前安装设置的
    ​	EulerOS默认做了安全加固`centos可以`，不允许root`管理员用户`用户远程登录。`可在Fusioncompute产品手册查询`

    - [ ] **进入CNA系统**

      执行

      ```
      #cnalnit
      ```

      初始化`注意：l为大写i`
      系统会自动创建名为gandalf 并设置密码的普通用户

    - [ ] **安装VRM到CNA**

      `可以使用ISO文件使用命令提示符安装但过于复杂`

    1. 选择使用**MobaXterme工具**`win传文件到Linux工具` 将fusioncompute LinuxInstall `版本号都要相同` 传输到CNA01/02系统`Linux系统,只需传输至其中一个`

    2. 使用gandalf用户传输，传输完成使用root用户进行解压等操作

    浏览器地址栏输入`https://主机ip:8080`打开工具界面。输入用户名和密码之后，单击“登录”
    	初始帐号信息:`admin`
    	初始密码:`laaS@PORTAL-CLOUD8!`
    	`第一次登录需要修改默认密码，当前仅支持单用户登录。`

