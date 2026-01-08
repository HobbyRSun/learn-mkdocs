# 使用指南

## 📚 文档编写

### Markdown 基础语法

MkDocs 使用 Markdown 编写文档，以下是一些常用的 Markdown 语法：

#### 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
```

#### 列表

```markdown
- 无序列表项 1
- 无序列表项 2
  - 嵌套列表项

1. 有序列表项 1
2. 有序列表项 2
```

#### 链接和图片

```markdown
[链接文本](https://example.com)
![图片描述](image.jpg)
```

#### 图片管理

在 MkDocs 项目中管理图片的最佳实践：

1. **创建图片文件夹**：
   在 `docs` 目录下创建 `img` 或 `images` 文件夹，用于存放所有图片文件：
   ```
   docs/
       img/
           example.jpg
           screenshot.png
           ...
   ```

2. **引用图片**：
   使用相对路径引用图片：
   ```markdown
   ![示例图片](img/example.jpg)
   ```

3. **图片尺寸**：
   如果需要控制图片尺寸，可以使用 HTML 语法：
   ```html
   <img src="../img/example.jpg" width="500" height="300" alt="示例图片">
   ```

4. **图片说明**：
   可以为图片添加说明文字：
   ```markdown
   ![示例图片](../img/example.jpg)
   
   这是图片的说明文字
   ```

#### 代码块

```python
def hello_world():
    print("Hello, World!")
```

### MkDocs 特定功能

#### 导航链接

在文档中可以使用相对路径链接到其他页面：

```markdown
[首页](../index.md)
[关于页面](../about.md)
```

#### 提示框（Admonitions）

使用 admonition 扩展可以添加各种提示框：

```markdown
!!! note
    这是一个提示信息

!!! warning
    这是一个警告信息

!!! danger
    这是一个危险信息
```

## 🛠️ 站点配置

### 修改配置文件

配置文件 `mkdocs.yml` 包含了站点的所有配置信息：

```yaml
site_name: My MkDocs Site
theme:
  name: mkdocs
nav:
  - 首页: index.md
  - 关于: about.md
```

### 添加新页面

1. 在 `docs` 目录下创建新的 Markdown 文件
2. 在 `mkdocs.yml` 的 `nav` 部分添加导航项

## 🚀 站点构建

### 本地预览

使用以下命令启动本地服务器，实时预览站点：

```bash
mkdocs serve
```

访问 http://localhost:8000 查看效果。

### 构建站点

使用以下命令构建静态站点文件：

```bash
mkdocs build
```

构建后的文件将保存在 `site` 目录中。

### 部署站点

将 `site` 目录中的所有文件部署到您的 Web 服务器或静态站点托管服务即可。

## 💡 最佳实践

1. **保持一致的目录结构**：合理组织文档文件，便于管理和维护
2. **使用清晰的导航结构**：帮助用户快速找到所需内容
3. **添加适当的目录**：使用 `[TOC]` 或 `toc` 扩展自动生成目录
4. **使用代码高亮**：提高代码块的可读性
5. **定期更新文档**：保持文档内容的准确性和时效性

---

*更多信息请参考 [MkDocs 官方文档](https://www.mkdocs.org/)*