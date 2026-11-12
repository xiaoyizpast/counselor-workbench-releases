# 辅导员工作台 · Windows 安装版

面向高校辅导员的本地优先 Windows 桌面工作台。

**维护者：交运6班**

> 本仓库只存放安装包与更新文件，源代码私有，不在本仓库公开。

## 下载安装

到 [Releases](https://github.com/xiaoyizpast/counselor-workbench-releases/releases/latest) 下载：

- `CounselorWorkbench-Setup-x.y.z.exe`：安装版，自带 .NET 运行时；
- `CounselorWorkbench-x.y.z-Portable.zip`：免安装版（可选）。

安装版默认按当前 Windows 用户安装，不需要管理员权限；安装包未签名，SmartScreen 提示“未知发布者”时选择“更多信息 → 仍要运行”。

## 功能

- 今日工作台：待办、逾期、本周到期、风险提示、固定动作；
- 待办：优先级、截止时间、关联学生/班级、CSV 导出；
- 学生：名册、标签、风险等级、CSV 导入/导出；
- 台账：心理重点、学业预警、家庭困难、违纪、谈心谈话、宿舍安全；
- 周期：每日/每周/每月/节点固定动作；
- 材料：8 类文稿模板 + 7 类回复，支持导出 Word；
- 风险：风险案件、四步处置清单、回访；
- Windows 原生定时通知；关闭窗口后驻留系统托盘；
- AI 可选：用户自填 API Key，未配置时全部功能可手动完成。

## 数据与隐私

- 数据只存本机 `%LOCALAPPDATA%\CounselorWorkbenchData`；
- SQLite + SQLCipher 加密，密钥由 Windows DPAPI 保护；
- 默认不联网、不上传、不遥测；AI 仅在用户启用并填写 Key 后请求；
- 更新只替换程序文件，不删除本机数据；
- 卸载默认保留数据，可在卸载后手动删除数据目录。

## 更新机制

应用每次启动会静默检查本仓库的 GitHub Releases：

1. 发现新版本时弹窗提示；
2. 一键下载；
3. 自动重启完成更新；
4. 不删除本地数据。

更新源文件：`releases.win.json`、`assets.win.json`、`RELEASES`、`*-full.nupkg`；由 Velopack 生成。

## 卸载

Windows 设置 → 应用 → 已安装的应用 → “辅导员工作台” → 卸载；或应用内 设置 → 更新与卸载。

## 说明

- 本工具生成的是通用模板，正式发文前请按本校文件核对；
- 涉及学生安全的问题，请按学校应急预案第一时间上报；
- 软件为私有软件，源码不公开；仅授权用于辅导员日常工作。