# 二进制资料本地上传步骤

当前仓库已经提交了文字整理、变量表、开车 SFC 笔记和资料清单。PDF/JPG/PNG 原始文件建议用本地 git 或 GitHub 网页补传。

## 方式一：GitHub 网页上传

1. 打开仓库：`https://github.com/linkstwo/ximenzi`
2. 进入 `materials/pdfs/`，点击 `Add file -> Upload files`。
3. 将 5 个 PDF 拖进去，提交信息写：`上传 PDF 原始资料`。
4. 进入 `materials/images/`，点击 `Add file -> Upload files`。
5. 将图片资料拖进去，提交信息写：`上传图片原始资料`。

## 方式二：本地 git 上传

在电脑上解压本次对话生成的资料包后，执行：

```bash
git clone https://github.com/linkstwo/ximenzi.git
cd ximenzi

mkdir -p materials/pdfs materials/images

# 把 PDF 复制到 materials/pdfs/
# 把 JPG/PNG 复制到 materials/images/

git add materials/pdfs materials/images
git commit -m "上传原始 PDF 和图片资料"
git push origin main
```

## 传完后核对

核对 `materials/source_manifest.md` 中的文件大小和 SHA256，确保没有传错、损坏或漏传。

Windows PowerShell 下计算 SHA256：

```powershell
Get-FileHash .\materials\pdfs\文件名.pdf -Algorithm SHA256
```
