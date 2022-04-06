## 1 安装模式介绍

### 1.1 本地模式

!!! Abstract ""
    本地模式即 local 模式，DataEase 安装和运行时自带 Kettle 组件与 Doris 组件，无需自己再额外配置，1.9.0 版本之前的版本，默认安装即为 local ，local 模式下 Excel 数据集，API 数据集以及定时同步的数据默认保存的 Doris 组件中。 

### 1.2 精简模式

!!! Abstract ""
    精简模式即 simple 模式，simple 模式下不包含 Kettle 组件与 Doris 组件，用户需在【系统管理】的【系统参数】中手动配置 MySQL 引擎。

### 1.3 集群模式

!!! Abstract ""
    精简模式即 cluster 模式，cluster 模式下，Doris 组件与 Kettle 组件需自行安装；  
    Doris 安装部署可参考：http://doris.incubator.apache.org/zh-CN/ ，Kettle 安装部署可参考：http://www.kettle.org.cn/  
    Kettle 组件与 Doris 组件的添加请参考【系统管理】的【系统参数】说明。

## 2 切换安装模式

!!! Abstract ""
    若需改安装模式，修改 /opt/dataease/.env 文件中 DE_ENGINE_MODE，在安装目录下，重新执行安装脚本：
    ```shell
    /bin/bash install.sh
    ```