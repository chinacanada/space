# GitHub 备份清单

- 备份时间：2026-11-21 09:23 CST（首份）；2026-11-21 10:30 用新号 chinacanada 重新拉取刷新，23 个文件字节数与首份完全一致（2,159,961 字节）
- 账号：uxuvoyiz81-edge（仓库属主）；读取账号：chinacanada（新号，公开库可读）
- 来源：Muse 的 GitHub 连接器（token 当时还活着，二步验证锁的是网页登录）；10:30 刷新时连接器已换成新号 chinacanada，旧号公开库仍可读
- 方式：连接器 get_file_contents 逐文件下载（文本 21 个）；两个二进制文件走 raw.githubusercontent.com 直链下载
- 位置：`~/workspace/github-backup/2026-11-21/`
- 共 23 个文件，2,159,961 字节（约 2.1 MB）

## 各仓库

| 仓库 | 文件 |
|---|---|
| computing0913 | README.md、index.html、privacy.html、terms.html、google875b639e53f575f2.html（Search Console 验证文件，永不删除）、edge-mail-banner.jpg、.github/workflows/deploy.yml |
| computing0913-en | README.md、index.html |
| edge-ai-studio | LICENSE、README.md、index.html、.github/workflows/pages.yml |
| edge-ai-studio-en | README.md、index.html |
| gameedge | index.html |
| canjuhe | index.html |
| Thematic-frameworkedge | .github/workflows/backup-db.yml、build-apk.yml、deploy-cloudflare.yml、deploy-pages.yml |
| edge-space-apk | README.md、EDGE-space.apk（v1.0） |

## 核验

- 全部 21 个文本文件字节数与 GitHub 清单一致，0 失败。
- 主站 index.html 的 git blob SHA 与 GitHub 一致（f60cd5c6…），md5 与本地 `~/workspace/hy4-edge-v9r1/main-site.html` 一致（0b8a05dd…），即 2026-11-02 核对过的线上版。
- 两个二进制文件大小与 GitHub 一致，file 命令确认分别为 JPEG（2736x912）与 Android APK。

## 不在这份备份里的

- 私有仓库连接器读不到（edge-bot 404）：edge-bot、freesub-private、edge-spare。
- 它们的本地副本本来就有：Bot 代码在 `~/workspace/edge-bot/server.cjs`，freesub 在 `~/workspace/freesub-backup/`，主站在 `~/workspace/hy4-edge-v9r1/main-site.html`。
- 本备份是纯文件拷贝，没有 .git，不含任何 hook，不可直接用于 git 操作；要恢复部署时按文件推回新仓库即可。
