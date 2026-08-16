# 桌宠资源库

这是一个可持续扩展的桌宠私人仓库。每只桌宠使用独立目录保存，因此可以只下载或安装其中一只，也可以继续在仓库中添加新的桌宠。

## 当前桌宠

| 目录 | 名称 | 风格 |
| --- | --- | --- |
| `xiaomo/` | 小忠岳 | 白衬衫、眼镜男生风格 |
| `xiaoli/` | 小莉 | 像素风毕业纪念女孩，带相机 |

## 效果预览

<table>
  <tr>
    <td align="center">
      <a href="./xiaomo/"><img src="./assets/previews/xiaomo.png" alt="小忠岳桌宠效果图" width="192"></a><br>
      小忠岳
    </td>
    <td align="center">
      <a href="./xiaoli/"><img src="./assets/previews/xiaoli.png" alt="小莉桌宠效果图" width="192"></a><br>
      小莉
    </td>
  </tr>
</table>

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
├─ assets/             # README 效果图
├─ xiaomo/
├─ xiaoli/
└─ new-pet/
```

## 只下载一只桌宠

最简单的方法是下载仓库 ZIP，解压后只取需要的目录。

如果使用 Git，也可以用稀疏检出只获取指定目录：

```bash
git clone --filter=blob:none --no-checkout https://github.com/CheGan-xx/desktop-pets.git
cd desktop-pets
git sparse-checkout set xiaomo
git checkout
```

将整个 `xiaomo/` 或 `xiaoli/` 目录复制到桌宠目录中，并保留目录名。例如，默认位置分别是：

```text
# Windows
C:\Users\<用户名>\.codex\pets\xiaomo\

# macOS / Linux
~/.codex/pets/xiaomo/
```

如果设置了 `CODEX_HOME`，则使用 `${CODEX_HOME}/pets/xiaomo/`。安装 `xiaoli` 时将路径末尾替换为 `xiaoli`。不要把 `pet.json` 和 `spritesheet.webp` 直接平铺到 `pets/` 根目录，应用会根据子目录名加载桌宠。

## 添加新桌宠

1. 创建新的英文目录名，例如 `zongzong/`。
2. 放入该桌宠的 `pet.json` 和 `spritesheet.webp`。
3. 确保 `pet.json` 中的 `id` 与目录名一致。
4. 为该目录添加一个简短的 `README.md`，说明名称、风格和安装方式。
5. 在本文件的“当前桌宠”表格中补充一行。
6. 提交并推送到私人仓库。

本仓库只保存可迁移的桌宠成品，不保存参考照片、生成过程文件、API 密钥或其他个人敏感材料。
