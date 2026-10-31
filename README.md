# qq-bridge-releases

**这是 qq-bridge 的公开发布仓库，只存放安装包与自动更新清单；不放源代码。**

- 源码仓库保持私有，授权查看请向作者申请。
- 本仓库的 Release 附件仅供授权用户本人安装与更新，**请勿转发给未授权的人**。

## 安装

1. 安装并登录 **DeepSeek Harness 桌面版**（只需一次）
2. 下载最新 Release 中的 `qq-bridge-<版本>.zip`，解压到任意目录（路径尽量不含空格）
3. 双击 **`安装.cmd`**（自动装依赖、生成配置、安装 DSH 预设/MCP、创建桌面快捷方式）
4. 双击桌面 **「启动QQ桥接」**

> 安装完成后建议重启一次 DSH，让预设/MCP 生效。

## 自动更新

- 启动桥接后打开控制台，顶部会提示新版本；点 **更新** 即可
- 更新流程：自动备份 → 替换代码 → 恢复用户文件（config/state/roles 等）→ 数据迁移 → 重启 → 健康检查；失败会自动回滚
- 更新源就是本仓库的 `latest.json`（Release 附件）

## 校验

下载后可用 Release 说明里的 sha256 校验：

```bat
certutil -hashfile qq-bridge-<版本>.zip SHA256
```

## 许可证

本项目采用**专有授权许可**（非开源）：授权用户可免费个人使用、接收官方更新；禁止转发/再发布/商用/用于训练模型。完整条款见安装包内 `LICENSE`。
历史版本（≤ v0.2.1-r1）仍按 MIT 许可。

## 链接

- 最新版清单：`https://github.com/rhodehubman-lang/qq-bridge-releases/releases/latest/download/latest.json`
