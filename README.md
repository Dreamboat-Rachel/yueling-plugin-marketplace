# YueLing Plugin Marketplace

YueLing 的开源插件目录。

## 目录结构

- `registry.json`：插件目录索引
- `plugins/`：插件条目和元数据
- GitHub Releases：存放经过版本标记的插件安装包

每个插件条目应包含插件类型、名称、版本、下载地址和 SHA-256 校验值。YueLing 客户端将读取目录索引，校验安装包后再执行安装。

## 插件格式

支持 YueLing 插件格式：

- 节点：`.umd.js`
- 工具：`.tool.js`
- 技能：`.zip`、`.md`、`.tar`、`.tar.gz`、`.tgz`
- 扩展：`ext-*.umd.js`

