本仓库保存了 [DataEase 项目]() 的 [官方文档](https://dataease.io/docs/)，该文档使用 [MkDocs]() 文档框架下的 [Material for MkDocs]() 主题进行构建。

## 本地开发

### 克隆本仓库
```bash
git clone https://github.com/dataease/docs.git
```

### 安装依赖
```bash
cd docs
pip install -r requirements/requirements.txt
```

### 修改文档内容
本文档的文档结构定义在 `mkdocs.yml` 文件中，文档的具体内容均在 `docs` 目录中。
```yaml
..........
nav:
      - 产品介绍: index.md
      - 更新说明: changelog.md
      - 系统架构: system_arch.md
      - 安装部署:
          - Windows:
              - 离线安装: installation/offline_installation_windows.md
          - Linux:
              - 在线安装: installation/online_installation.md
              - 离线安装: installation/offline_installation.md
              - 在线升级: installation/online_upgrade.md
              - 离线升级: installation/offline_upgrade.md
              - 安装模式: installation/installation_mode.md
          - 命令行工具: installation/cli.md
      - 功能手册:
          - 通用功能: user_manual/general.md
          - 首页: user_manual/homepage.md
          - 数据源:
              - 数据源概述: user_manual/datasource_description.md
              - 配置数据库数据源: user_manual/datasource_configuration.md
              - 配置 API 数据源: user_manual/datasource_configuration_api.md
          - 数据集:
              - 数据集概述: user_manual/dataset_description.md
              - 添加数据集:
                  - 数据库数据集: user_manual/dataset_configuration/dataset_database.md
                  - SQL 数据集: user_manual/dataset_configuration/dataset_SQL.md
                  - Excel 数据集: user_manual/dataset_configuration/dataset_Excel.md
                  - 自定义数据集: user_manual/dataset_configuration/dataset_definision.md
                  - 关联数据集: user_manual/dataset_configuration/dataset_connection.md
                  - API 数据集: user_manual/dataset_configuration/dataset_api.md
              - 数据集功能设计: user_manual/dataset_design.md
          - 仪表板:
              - 仪表板概述: user_manual/dashboard_description.md
              - 创建仪表板: user_manual/dashboard_create.md
              - 仪表板基础功能: user_manual/dashboard_basicfunctions.md
              - 视图组件:
                  - 视图概述: user_manual/view_module/view_generation.md
                  - 添加视图: user_manual/view_module/view_create.md
                  - 视图功能设计: user_manual/view_module/view_design.md
                  - 视图图库: user_manual/view_module/view_gallery.md
              - 过滤组件:
                  - 时间过滤组件: user_manual/filter_module/filtertime_module.md
                  - 文本过滤组件: user_manual/filter_module/filtertext_module.md
                  - 数字过滤组件: user_manual/filter_module/filternumber_module.md
              - 其他组件:
                  - 样式组件: user_manual/other_module/style_module.md
                  - 多媒体组件: user_manual/other_module/multimedia_module.md
                  - 其他组件: user_manual/other_module/other_module.md
              - 组件基础功能: user_manual/module_basicfunctions.md
              - 仪表板使用: user_manual/dashboard_using.md
          - 系统管理:
              - 用户管理: user_manual/system_management/user.md
              - 系统参数: user_manual/system_management/param.md
              - 模版管理: user_manual/system_management/module.md
              - 站内消息: user_manual/system_management/message.md
              - 定时任务: user_manual/system_management/task.md
          - 移动端:
              - 移动端概述: user_manual/app_description.md
              - 移动端布局: user_manual/app_design.md
      - 教学视频: instructional_video.md
      - 常见问题:
          - 安装配置:
              - 安装配置相关: faq/configuration_faq/configuration.md
              - 安装启动相关: faq/configuration_faq/installation_starts.md
              - MySQL 相关: faq/configuration_faq/dataease_mysql.md
          - 备份还原: faq/backup_faq.md
          - 系统管理: faq/system_management.md
          - 功能相关:
              - 数据集: faq/dataset_faq.md
              - 仪表板: faq/panel_faq.md
          - 安全问题: faq/security_faq.md
          - 企业版: faq/enterprise_faq.md
      - 开发文档:
          - 开发环境搭建: dev_manual/dev_manual.md
          - 源码搭建（前后端分离）:
              - 工具准备: dev_manual/dev_deployment/tool.md
              - 环境准备: dev_manual/dev_deployment/enviroment.md
              - 源码准备: dev_manual/dev_deployment/code.md
              - 编译运行: dev_manual/dev_deployment/compile.md
              - 注意事项: dev_manual/dev_deployment/attention.md
          - 开发问题: faq/dev_faq.md
      - 技术咨询: https://jinshuju.net/f/e40eKK
      - 联系我们: contact.md
..........
```

文档内容使用 markdown 语法编写，若要添加新的文档，需要先在 `mkdocs.yml` 文件中的 `nav` 部分增加对应章节导航。

### 本地调试文档
```bash
mkdocs serve
```
执行上述命令后，可通过 `http://127.0.0.1:8000` 地址查看生成的文档内容，当修改文档后，页面内容会自动更新。

### 构建文档
```bash
mkdocs build
```

执行上述命令后，会在 `site` 目录下生成文档站点的静态文件，将目录中的内容复制到任意 HTTP 服务器上即可完成文档的部署。

## 帮助完善文档

### Fork 文档仓库
点击仓库右上角的 `fork` 按钮，复制本仓库到自己的 github 账号。

### 克隆 fork 后的仓库
```bash
git clone https://github.com/your-github-account/docs.git
```

### 本地修改并调试

### Push 修改内容到 GitHub 仓库

### 提交 Pull Request 到本仓库
