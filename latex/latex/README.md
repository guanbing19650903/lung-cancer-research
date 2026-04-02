# LaTeX 编译说明

## 文件清单

- `main.tex` - 主文档（中文）
- `main_jto.tex` - JTO 期刊格式（英文）
- `references_expanded.bib` - 参考文献（60 篇）
- `supplementary.tex` - 补充材料（16 页）
- `cover_letter_jto.tex` - 投稿 Cover Letter
- `README.md` - 本说明文件

## 编译方法

### Overleaf 在线编译（推荐）

1. 访问 https://www.overleaf.com
2. 创建新项目（New Project）
3. 上传所有 `.tex` 和 `.bib` 文件
4. Menu → Compiler → XeLaTeX
5. 点击编译

### 本地编译

```bash
cd latex/

# 主文档
xelatex main.tex
bibtex main.tex
xelatex main.tex
xelatex main.tex

# 补充材料
xelatex supplementary.tex
xelatex supplementary.tex
