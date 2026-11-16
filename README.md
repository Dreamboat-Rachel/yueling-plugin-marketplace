# YueLing Plugin Marketplace

YueLing 的开源插件目录。

## 目录结构

- `registry.json`：插件目录索引
- `plugins/`：插件条目和元数据
- GitHub Releases：存放经过版本标记的插件安装包

## registry.json

目录使用固定结构：

```json
{
  "version": 1,
  "plugins": [
    {
      "id": 1,
      "type": "node",
      "identifier": "exampleNode",
      "name": "示例节点",
      "description": "插件说明",
      "version": "1.0.0",
      "author": "作者",
      "homepage": "https://github.com/作者/exampleNode",
      "downloadUrl": "https://github.com/作者/exampleNode/releases/download/v1.0.0/exampleNode.umd.js",
      "fileName": "exampleNode.umd.js",
      "sha256": "替换为安装包的 SHA-256"
    }
  ]
}
```

`id` 在目录中必须唯一，插件更新时保持不变，只递增 `version` 并更新下载地址和校验值。

每个插件条目应包含插件类型、名称、版本、下载地址和 SHA-256 校验值。YueLing 客户端将读取目录索引，校验安装包后再执行安装。

## 插件格式

支持 YueLing 插件格式：

- 节点：`.umd.js`
- 工具：`.tool.js`
- 技能：`.zip`、`.md`、`.tar`、`.tar.gz`、`.tgz`
- 扩展：`ext-*.umd.js`

