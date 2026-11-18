# AGENTS.md · 项目规则

> 给 AI / 未来的你：只记文档里看不出的关键信息。
> 📌 **文档基线**：2026-11-18（commit `__SHA__`）接入 repo-kit 机器层（link-only / 规范 2.1.4）

## 项目是什么

VMware Workstation 虚拟机安装 Windows 图文教程（交互式 HTML 幻灯片，30 张 WebP 截图），手把手从零到安装成功。

## 关键坑（装机实战经验）

1. **下载渠道**：网盘（VMware-Workstation-Lite-setup.7z）或 Broadcom 官网注册后下载**个人免费版**（用于个人非商业用途）
2. **创建虚拟机**：ISO 选 windows 系统镜像；安装位置最好放**固态盘**（速度快）；Win11 安全要求需设密码（本地使用 123456 那些都行）
3. **资源配置**：磁盘文件初始很小随使用增长；内存不超过系统内存 **1/2**（越大越好）；CPU 数字改大，过大系统会提示
4. **安装系统**：看到 "Press any key" 点击任意键进入；基本都是下一步
5. **进系统前先断网**：Windows 联网更新机制会引导走微软账户——先断开虚拟机网络连接再进系统，避免强制登录微软账户
6. **硬件可后调**：不修改直接完成也行，进系统后随时可调

## 文档

- [README.md](README.md)：内容概要 + 文件说明
- [DEVELOPMENT.md](DEVELOPMENT.md)：长卷幻灯片架构、断网/内存/截图体积三个坑
- 文件：`index.html`（交互式教程）+ `images/`（30 张截图）

## 机器层（repo-kit · link-only）

- `schema/taxonomy.json` + `schema/kit.lock.json`（kit `2.9.0` / 规范 `2.1.4` / `link-only`）+ `tools/repo-kit/check_repo.py`
- 校验：`python tools/repo-kit/check_repo.py --root .`；锁哈希：`pwsh tools/update-repo-kit.ps1 -Check`
- 只查**链接与锚点**：全仓 md 豁免 frontmatter（本仓没有 frontmatter 契约）
- `schema/kit.lock.json` **不要手改**，升级只能跑 `tools/update-repo-kit.ps1`
