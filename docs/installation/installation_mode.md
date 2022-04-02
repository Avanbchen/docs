## 1 本地模式

!!! Abstract ""
    本地模式下，DataEase 安装和运行时自带 MySQL 组件、 Kettle 组件与 Doris 组件。

## 2  精简模式

!!! Abstract ""
    精简模式下，DataEase 安装和运行时自带 MySQL 组件，Excel 数据集和 API 数据集的数据存放在 MySQL 组件，若要切换 local 模式，执行：
    ```shell
    dectl uninstall
    ```
    修改安装包下 install.conf 文件中 engine_mode=local，执行：
    ```shell
    vim /opt/dataease/conf/dataease.properties
    ```
    修改 dataease.properties 文件中 engine_mode=local，执行：
    ```shell
    cd /opt/dataease
    ```
    修改 .env 文件中 engine_mode=local，在安装目录下，重新运行运行安装脚本：
    ```shell
    /bin/bash install.sh
    ```
    重新 install 以安装 Kettle 和 Doris 组件。

## 3 集群模式

!!! Abstract ""
    集群模式下，DataEase 安装和运行时包含 MySQL 组件，Doris 组件与 Kettle 组件需自行安装，Doris 安装部署可参考：http://doris.incubator.apache.org/zh-CN/ ，Kettle 安装部署可参考：http://www.kettle.org.cn/  
    Kettle 组件与 Doris 组件的添加请参考【系统管理】的【系统参数】详情。
    