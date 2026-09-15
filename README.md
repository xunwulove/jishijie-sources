# jishijie-sources

极视界（Jishijie）影视源订阅列表与编写规则。

## 订阅地址

软件「设置 → 影视源 → 源导入导出 → 同步订阅」填入：

```
https://raw.githubusercontent.com/xunwulove/jishijie-sources/main/jishijie-sources.json
```

## 文件说明

| 文件 | 说明 |
|------|------|
| `jishijie-sources.json` | 订阅主文件（42 个源：type=1 CMS × 23、type=3 drpy2 × 19） |
| `type1影视源.json` | type=1 标准 CMS 源（拆分版，与主文件一致） |
| `type3影视源.json` | type=3 drpy2 爬虫源（拆分版，与主文件一致） |
| `type4影视源.json` | type=4 XPath 规则源（当前为空占位） |
| `影视源编写规则文档.md` | 影视源编写/修改完整规则（AI 执行版，含 type=1/3/4 三种格式） |

## 约定

- 修改源后同步更新 `jishijie-sources.json` 与对应拆分文件，保持三者一致
- 源字段结构：`key / name / type / api / ext / jar / searchable / quickSearch / filterable / timeout / playerApi / categories`
- type=3 源 `ext` 为内联 drpy2 JS 规则；type=1 源 `api` 为标准 MacCMS 采集接口
