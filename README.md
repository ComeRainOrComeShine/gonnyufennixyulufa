# 赣语-分宜版

`gonnyufennixyulufa` 是独立维护的 Rime 赣语分宜话输入方案，用户可见名称为【赣语-分宜版】。

本仓库只包含 Rime 方案和词典，不包含 Trime Android 主框架。它以
【赣语-昌宜兼容】现行词库为底本独立出来，后续修改不会影响
“赣语-昌宜兼容”、南昌话、抚州话、宜春话等其他版本。

## 方案

- `gonnyufennixyulufa`：赣语分宜输入法主方案
- `gonnyufennixyulufa_auxiliary_pinyin`：普通话拼音反查分宜读音

## 安装

将本仓库的 YAML、TSV 和 `rime.lua` 文件复制到 Rime 用户目录，并确保已安装 Rime 的
`prelude`、`stroke`、`luna_pinyin` 和 `essay` 基础数据。

在 `default.custom.yaml` 的 `schema_list` 中加入：

```yaml
patch:
  schema_list:
    - schema: gonnyufennixyulufa
    - schema: gonnyufennixyulufa_auxiliary_pinyin
```

保存后重新部署 Rime。

## 命名约定

本仓库所有内部 ID 使用 `gonnyufennixyulufa` 前缀，避免与其他赣语地方版本同时安装时
覆盖彼此的 schema、dictionary、user dictionary、Lua filter 或注释数据。

## 版本

- `0.1.1-20260611`：同步当前昌宜兼容词库底本，显示名统一为【赣语-分宜版】
- `0.1.0-20260610`：从分宜版数据独立建库

## 许可

程序配置按 GPL-3.0-or-later 发布。第三方词频数据的许可信息保留在对应词典文件头部。
