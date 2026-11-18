# CHANGELOG.md · 版本记录

> 项目无正式版本号，按提交里程碑记录。

## 2026-11-18 · 文档维护：接入 repo-kit 机器层（link-only）

- `schema/taxonomy.json` + `schema/kit.lock.json`（kit `2.9.0` / 规范 `2.1.4`）+ `tools/repo-kit/check_repo.py`
- `.github/workflows/repo-check.yml`：md / `schema/**` / `tools/**` 变更时跑链接与锚点检查 + 锁哈希校验
- 只改文档基建，不动产品代码；验收 `REPO CHECK: PASS`（ERROR=0、WARN=0）、`KIT LOCK: PASS`
- 新增 `DEVELOPMENT.md` 并补文档基线行
- 删除 1 字节空占位文件 `20260704Final`（内容仅一个换行符，无任何引用）
- README 文件表 `vmware-install-guide.html` → 实际文件名 `index.html`

## 里程碑

- **交互式教程完成**：index.html（深色主题、卡片式翻页、30 张 WebP 截图，适合手机/电脑浏览）
- **初始版本**：VMware Workstation 虚拟机安装 Windows 图文指南

## 备注

- 无版本 tag / Release
