# How We Work: 文档与贡献指南

## 关于我们

One Among Us 是一家旨在提高跨性别权利，呼吁对跨性别者的关注，并且为跨性别者提供社群支持的非营利组织。目前我们的主要工作是运营 [那些秋叶 One-Among.Us](https://one-among.us) 网站，纪念那些已经逝去的跨性别者或友跨伙伴（allies）。

## 那些秋叶

那些秋叶 One-Among.Us 是开源网站。文章和源代码均储存于 GitHub，由三个仓库组成：[`data`](https://github.com/one-among-us/data) 主要存放文章和评论，[`web`](https://github.com/one-among-us/web) 主要存放前端代码，[`backend`](https://github.com/one-among-us/backend) 存放后端代码。如果想要做内容的更新，只需要关注 `data` 仓库的结构就好。 

### 贡献内容

评论是机器人自动同步上去的，只需要在网站上填写。如果想要贡献信息和正文，可以参照下列文章：

- 我们的 [编辑指南](EditingGuide-zh_Hans.md)。
- 如果涉及和自杀相关的报道，还请参照世界卫生组织的 [媒体工作者预防自杀指南](https://apps.who.int/iris/handle/10665/258814)（可以从链接下载中文版）。

### 贡献代码

#### Commit Messages 的写法

自 2023 年 2 月 20 日起，One Among Us 所有代码仓库的 commit messages 均采用以下格式：

> [*] Do something

整条 message 以英文写作。以方括号内的标记符开头，方括号后加一个空格，再以大写 **动词** 起始描述基本的更改点，句末不加标点符号。如果有在一行之内写不下或认为不必写在标题的内容，请在之后以更加具体的 commit message 作为补充。每行不超过 72 英文字符。

**标记符**

> [+] 添加
>
> [-] 移除
>
> [U] 更新 (Update)
>
> [O] 优化 (Optimization)
>
> [F] 修复 (Fix)
>
> [S] 样式 (Style)
>
> [M] 移动 (Move)
>
> [T] 测试 (Test)
>
> [D] 文档 (Documentation)
>
> [B] 备份（Backup）
>
> [PR] Merge commit of pull request

**例子**

> [+] Add entry for sauricat

添加 sauricat 的条目。

> [U] Update photos for sauricat

更新 sauricat 的照片。

> [F] Fix punctuation

修改标点符号。

*Under Construction...*
