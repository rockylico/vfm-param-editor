# 部署VFM参数编辑器到GitHub Pages

## 📋 准备工作

1. GitHub账号（你已有 ✅）
2. Git工具（如果没有，下载：https://git-scm.com/downloads）

---

## 🚀 快速部署（5分钟）

### 步骤1：创建GitHub仓库

1. 打开 https://github.com/new
2. 填写信息：
   - Repository name: `vfm-param-editor`
   - Description: `VFM-E2E参数编辑器`
   - 选择 **Public**
   - ✅ 勾选 "Add a README file"
3. 点击 **Create repository**

---

### 步骤2：上传文件

**方法A：网页上传（最简单）**

1. 在仓库页面，点击 **"Add file"** → **"Upload files"**
2. 拖拽以下文件：
   - `index.html`（将vfm_radar_editor.html重命名为index.html）
   - `vfm_params_latest.json`
3. 点击 **Commit changes**

**方法B：Git命令行**

```bash
# 1. 克隆仓库
git clone https://github.com/YOUR_USERNAME/vfm-param-editor.git
cd vfm-param-editor

# 2. 复制文件到仓库
cp /path/to/vfm_radar_editor.html index.html
cp /path/to/vfm_params_latest.json .

# 3. 提交并推送
git add .
git commit -m "Add VFM param editor"
git push
```

---

### 步骤3：启用GitHub Pages

1. 在仓库页面，点击 **Settings**
2. 左侧菜单找到 **Pages**
3. Source选择：
   - Branch: `main`
   - Folder: `/ (root)`
4. 点击 **Save**

---

### 步骤4：访问你的编辑器

等待1-2分钟，然后访问：
```
https://YOUR_USERNAME.github.io/vfm-param-editor/
```

---

## 🎯 在飞书中使用

### 方法1：文档中嵌入

1. 打开飞书文档
2. 点击 **"+"** → **"网页"**
3. 粘贴URL：
   ```
   https://YOUR_USERNAME.github.io/vfm-param-editor/
   ```
4. 调整大小，完成！

### 方法2：添加快捷方式

1. 在飞书文档中，输入 `/` 命令
2. 选择 **"链接"**
3. 添加标题：`VFM参数编辑器`
4. 粘贴URL

---

## 🔄 更新数据

当飞书表格参数更新后：

1. 从飞书获取最新JSON
2. 在GitHub仓库中更新 `vfm_params_latest.json`
3. GitHub Pages会自动更新（1-2分钟）

---

## 📝 文件清单

确保上传这些文件：

1. ✅ `index.html` - 主编辑器（从vfm_radar_editor.html重命名）
2. ✅ `vfm_params_latest.json` - 参数数据
3. ✅ `README.md` - 说明文档（可选）

---

## 🔧 高级配置（可选）

### 自定义域名

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 内容：`your-domain.com`
3. 在域名服务商配置DNS

### 添加访问统计

在HTML中添加：
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_ID"></script>
```

---

## 🆘 常见问题

### Q: 页面显示404？
A: 等待1-2分钟，GitHub Pages需要时间部署

### Q: 更新后没有变化？
A: 清除浏览器缓存，或使用隐私模式

### Q: 需要API更新功能？
A: 联系我，我可以修改HTML支持直接API调用

---

## 📞 需要帮助？

遇到任何问题，随时联系我！

我可以：
- ✅ 帮你检查部署是否成功
- ✅ 修改HTML支持新功能
- ✅ 优化用户体验
