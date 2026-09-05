> **本仓库已迁移并归档 / This repository has moved and is archived.**
>
> 当前源码与后续维护位于 [MSIME-Engine 的 `dictionary/custom/`](https://github.com/metasequoiaime/MSIME-Engine/tree/main/dictionary/custom)。
> 请在 [MSIME-Engine](https://github.com/metasequoiaime/MSIME-Engine) 提交 Issue 和 Pull Request。
> 完整提交历史已保留在 Engine 中；本仓库保留历史代码、标签与已有 Release，供旧版本追溯和下载。
> 迁移来源见 [consolidation-sources.json](https://github.com/metasequoiaime/MSIME-Engine/blob/main/docs/consolidation-sources.json)。
>
> 以下为归档前的历史说明，当前构建与使用方式请以 Engine 中的文档为准。

# 水杉输入法自定义词库

这个仓库保存无法从通用词典稳定取得的人工维护条目。根目录保留现有自定义数据，其中
`translations.txt` 会被 MetasequoiaImeDict 构建流程用作候选窗翻译覆盖；`packs/` 下是用户按需导入的专业词库。

## 专业词库

- [`packs/unreal_houdini`](packs/unreal_houdini)：Unreal Engine、Houdini 和 Houdini Engine for Unreal

专业词库不会自动加入所有用户的候选列表。用户选择导入后，新增内容会作为用户词条保存，
因此既能满足垂直领域输入，也不会用 `SOP`、`TOP`、`PCG` 等短缩写干扰普通用户。

运行以下命令可以检查所有专业词库的字段格式、拼音、重复项和翻译覆盖率：

```powershell
python tools/validate_packs.py
```
