# 🌐 HandRaw Static (静态分发中心与云端热更新源)

本项目是 **[HandRaw Style](https://github.com/yang0/handraw-style)** 的云端静态资源分发与客户端动态热更新源。

---

## 📁 目录结构

- **`manifest.json`**：客户端启动时探测的清单文件，记录最新画风库版本号、画风总数、更新时间、数据文件与图片 CDN 地址；
- **`data/`**：
  - `styles.json`：全量手绘风格数据
  - `layouts.json`：166 款排版图型数据
  - `colors.json`：36 款经典单色数据
  - `tones.json`：16 款影调数据
  - `partners.json`：中转商推荐与专属返佣/福利链接
- **`images/`**：
  - `individual/`：手绘风格 WebP 高清预览缩略图
  - `layouts/`：排版图型示意图
  - `colors/`：色卡图片
  - `tones/`：影调示例图

---

## 🔄 自动化同步与发布

在 `handraw-style` 主仓库执行以下命令即可全自动增量同步并推送到本仓库：

```bash
# 仅本地同步
python scripts/sync_to_static.py

# 同步并自动提交 Git 推送到 GitHub 远端
python scripts/sync_to_static.py --git

# 同步并一键部署到 tencent-vm 云服务器
python scripts/sync_to_static.py --deploy
```
