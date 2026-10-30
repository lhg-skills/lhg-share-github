# lhg-share-github

当用户给一个 GitHub 仓库链接、想在国内分享时使用：先核许可与署名，再默认走 Gitee 组织镜像导入，验收后交付 Gitee 链接与克隆命令，不走 GitHub 组织、不冒充原创。

## 安装

```bash
npx -y skills add lhg-skills/lhg-share-github -g --all
```

## 解决什么

用户给一个 GitHub 仓库链接，想让国内用户不用 GitHub、不用 VPN 就能拿到并使用。这个 Skill 的默认解法是：先核实许可与署名，再合规导入到 Gitee 组织，对外只发 Gitee 链接。

默认不走 GitHub 组织，不把代码复制成新仓冒充原创，不改上游代码，不删 LICENSE。

## 使用

安装后，可以这样开始：

> 使用 $lhg-share-github，把 https://github.com/Renhuai123/ziwei-doushu 放到 Gitee 分享。

默认归属是 Gitee 组织 `lls-find-hub`，仓名默认用上游仓名，仓属性默认开源。用户本轮另有指定时才改。

## 默认流程

1. 核实上游许可、版权人、数据集许可、非商用部分，拆开写，不要混成一句可商用。
2. 用浏览器任务登录 Gitee，确认组织存在、账号是成员且有建仓权限；组织不存在且用户没有说先创建时先停下问。
3. 从组织页新建开源仓，用“从 URL 导入”填入 GitHub 地址导入。
4. 按模板改描述，写明镜像收藏、原作者、许可、不改代码、不声称原创。
5. 验收后交付：Gitee 地址、克隆命令、最新提交 SHA、公开与许可等验收数字。

## 主要边界

- 许可不明或明确禁止再分发时停下。
- 不要用第三方代理镜像站当正式分享链接。
- 上游没有 SKILL.md 时，不要把它当 Skill 直接提交到要求 SKILL.md 的 SkillHub。

## 运行依赖

- 支持 Agent Skills 的客户端

## 内容

本仓库只发布运行这个 Skill 所需的文件。本地评测样本、预期答案和运行记录不包含在公开包中。
