# 桌宠资源库

这是一个可持续扩展的桌宠私人仓库。每只桌宠使用独立目录保存，因此可以只下载或安装其中一只，也可以继续在仓库中添加新的桌宠。

## 当前桌宠

| 目录 | 名称 | 风格 |
| --- | --- | --- |
| `xiaomo/` | 小忠岳 | 白衬衫、眼镜男生风格 |
| `xiaoli/` | 小莉 | 像素风毕业纪念女孩，带相机 |

## 目录约定

每只桌宠目录至少包含：

```text
桌宠目录/
├─ pet.json
└─ spritesheet.webp
```

以后新增桌宠时，在仓库根目录创建新的独立目录，并将该桌宠自己的 `pet.json` 和 `spritesheet.webp` 放在目录内。例如：

```text
desktop-pets/
├─ xiaomo/
├─ xiaoli/
└─ new-pet/
```

## 只下载一只桌宠

最简单的方法是下载仓库 ZIP，解压后只取需要的目录。

如果使用 Git，也可以用稀疏检出只获取指定目录：

```bash
git clone --filter=blob:none --no-checkout <仓库地址>
cd desktop-pets
git sparse-checkout set xiaomo
git checkout
```

把 `xiaomo` 或 `xiaoli` 目录中的全部文件复制到桌宠应用的资源目录，并保持 `pet.json` 与 `spritesheet.webp` 位于同一层级。

## 添加新桌宠

1. 创建新的英文目录名，例如 `zongzong/`。
2. 放入该桌宠的 `pet.json` 和 `spritesheet.webp`。
3. 为该目录添加一个简短的 `README.md`，说明名称、风格和安装方式。
4. 在本文件的“当前桌宠”表格中补充一行。
5. 提交并推送到私人仓库。

本仓库只保存可迁移的桌宠成品，不保存参考照片、生成过程文件、API 密钥或其他个人敏感材料。
