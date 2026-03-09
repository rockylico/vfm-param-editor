# VFM-E2E 参数雷达图编辑器

🎯 **可视化拖动调整参数，一键更新到飞书**

## 功能特性

- ✅ **雷达图可视化** - 9个大专题权重对比
- ✅ **拖动交互** - 直接拖动雷达图或- ✅ **滑块调整** - 精确控制每个参数
- ✅ **一键更新** - 生成PowerShell命令更新飞书表格
- ✅ **UTF-8支持** - 完美处理中文字符

## 快速开始

1. 打开 `index.html`
2. 选择配置类型（得分权重/优化上限阈值/等）
3. 拖动雷达图或调整滑块
4. 点击 **"🔧 生成 PowerShell 命令"**
5. 在PowerShell中粘贴运行

## 技术栈

- **Plotly.js** - 交互式雷达图
- **Feishu API** - 数据存储
- **PowerShell** - 数据更新

## 部署

本项目部署在GitHub Pages，- 访问地址：`https://[username].github.io/vfm-param-editor/`
- 免费托管
- HTTPS支持
- 全球CDN加速

## 数据源

飞书多维表格：
- App Token: `P342bep6baOcMGsFw4pc4tNDn0c`
- Table ID: `tblwbP7XRDnBIFwy`
- 数据自动同步

## 更新参数

### 方式1：PowerShell命令（推荐）

```powershell
# 1. 保存JSON到文件
$json = @'
{参数数据}
'@
$json | Out-File -FilePath "vfm_update.json" -Encoding UTF8

# 2. 用curl发送
curl -X POST "https://zyt.feishu.cn/base/automation/webhook/event/IVR5aXAKlwwx3phIzSvczyiVnAg" -H "Content-Type: application/json; charset=utf-8" --data-binary "@vfm_update.json"
```

### 方式2：AI助手

需要更新数据时，联系AI助手获取最新的HTML文件

## 许可证

MIT License

## 作者

VFM-E2E Team
