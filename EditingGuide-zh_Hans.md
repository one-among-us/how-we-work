# 编辑指南 - 那些秋叶

## 编写的原则

我们的目的是做一个小的纪念馆，而不是 wiki。因此，我们更鼓励用写作来抚慰不在世和在世的各位跨儿朋友以及我们的盟友们（allies）。无论逝者是什么性别身份，我们希望给读者看到的是，「原来，ta 们曾经是和我一样的，鲜活的生命。」因此，过于夸张或者过于冷静的描写都是需要避免的。

写作的风格比起 wiki 来说是相对自由的，但仍然需要遵守一些基本的原则，例如：

- 所写内容要尽量做到真实；
- 如果有大段的引用，需要标明出处；
- 可以使用一些社群内，或者说「圈内」的术语，但是如果愿意的话，请尽量在第一次出现的时候加上注释。

编写逝者条目应该使用第三人称。请注意使用适当的代词，尊重逝者本人的意愿。对非二元性别者、无性别者、性别不明确者等，如无本人说明，请用「ta」作为代词（目前我们没有找到更好的中文词语来替代），或者在行文中不使用代词。

在各种语文的条目中都应当使用通行规范标点。仅有一处特殊情况：如无特殊说明，无论是哪种中文版本，引号都请使用直角引号「」（外层）和『』（内层）代替 “” 和 ‘’，除非所引用内容并非中文。英文引号需要使用 “” 和 ‘’，而不是没有弯曲度的 " 或者 '。

如果要引用外部来源，请使用网络档案馆链接服务，比如 [Internet Archive](https://archive.org) 和 [archive.today](https://archive.ph) 等 (参见 [data/#141](https://github.com/one-among-us/data/issues/141) 的讨论）。

为了保护我们的读者，如果逝者是自杀离去的，请尽量淡化具体的方式。如果是采取药物的方式，不可以写出具体的药品名称或剂量。

### 逝者条目命名规范

#### 网页路由与data仓库内的目录名

`data` 仓库内 `people` 目录下的目录名直接被用于网页路由的生成，例如：

[https://www.one-among.us/profile/noname](https://www.one-among.us/profile/noname) 页面对应 `github:one-among-us/data/people/noname` 目录

贡献者在创建新条目时，建议参考如下原则对目录进行命名：

- 请贡献者在不引起混淆的情况下尽可能使用确认为逝者**个人持有**的，最具有**公共性**的线上身份标识作为目录名称或命名参考。一般而言，我们认为这一标识应当按照如下顺序选取：
  - 逝者最广为人知的身份标识，尽可能只包含字母/数字/下划线，尽可能不包含 slash `/` 空格 `␣` 及其他需要转义的字符
  - twitter/X **username**
  - telegram **username**
  - fediverse **username**
  - 其他类似性质论坛/IM/社交网络中用于标识用户的**唯一ID**，包括但不限于 discord/IRC/个人网站/wechat
- 请尽可能以 twitter/X username [字符限制](https://help.twitter.com/en/managing-your-account/change-x-handle)作为目录命名参照：
  - 目录名长度在4～15个字符之间
  - 仅使用字母，数字与下划线`_`
- 考虑到现实世界的不确定性，无法通过简单的命名规则完全规避重名的可能。贡献者需一定程度上自行保障目录名称和逝者之间的对应并避免歧义。出现冲突时，请优先考虑避让先前已录入的条目并发邮件到 [info@one-among.us](mailto:info@one-among.us) 加以确认。

## 收录的标准

我们纪念两类逝者：

- 跨性别者、跨**性**别者、非二元性别人士、非常规性别者（transgender, transsexual, non-binary, and gender non-conforming people, 总称 TGD）。只要确认其 TGD 身份，就可以收录。不应该因为 TGD 人士的品行问题而选择拒绝收录和纪念，但可以以后人的视角在介绍中作公正的评判；
- 对 TGD 社群有感情的友跨人士（allies）。这里的标准比较宽松。

我们维护了一份只有 One Among Us 在任志愿者能看到的「不愿被收录人士的名单」，一旦发现 Pull Requests 或者 Issues 中有名单内提到的人，我们会手动关闭。这份名单我们认为不应该公开查阅，但是如果有确认名单或者希望自己不被收录的需求，请发邮件到 [info@one-among.us](mailto:info@one-among.us) 联系我们。

## 用 GitHub 来修改和提交

如果想要继续，你首先需要以下知识：

- `git` 的基本使用：克隆仓库、commit、rebase 到主分支、在上游和本地间同步；
- GitHub 的基本使用：复刻源码、创建 PR、与其他 GitHub 用户合作；
- YAML 基本语法：缩进规则、横线、空格与引号的使用、处理特殊字符；
- Markdown 基本语法。

或者你也可以直接把想要修改或增加的部分发邮件到 [info@one-among.us](mailto:info@one-among.us)。我们的工作人员会把它们转成恰当格式上传。我们并不需要贡献者有任何技术知识，你完全可以以你喜欢的方式工作。任何形式的贡献都同样会被认可。

## 支持的 Features

### 注释块

除去 markdown 所支持的 HTML 注释块 `<!--` 和 `-->` 外, 额外支持 JSX 的注释块 `{/*` 和 `*/}`. 例如:

``` HTML
<!-- 这是注释, 将不会在文章中显示 -->
```

``` JSX
{/* 这也是注释, 将不会在文章中显示 */}
```

### 嵌入文章中的图标

支持类似于 `[!Note]` 的内嵌图标. 直到本文编写时 (Apr.7, 2024), 受支持的标识如下表所示:

|标识|图标|
|:-:|:-:|
|`[!Caution]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: rgb(209, 36, 47); margin-right: 10px;" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="M4.47.22A.749.749 0 0 1 5 0h6c.199 0 .389.079.53.22l4.25 4.25c.141.14.22.331.22.53v6a.749.749 0 0 1-.22.53l-4.25 4.25A.749.749 0 0 1 11 16H5a.749.749 0 0 1-.53-.22L.22 11.53A.749.749 0 0 1 0 11V5c0-.199.079-.389.22-.53Zm.84 1.28L1.5 5.31v5.38l3.81 3.81h5.38l3.81-3.81V5.31L10.69 1.5ZM8 4a.75.75 0 0 1 .75.75v3.5a.75.75 0 0 1-1.5 0v-3.5A.75.75 0 0 1 8 4Zm0 8a1 1 0 1 1 0-2 1 1 0 0 1 0 2Z"></path></svg>|
|`[!Warning]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: rgb(154, 103, 0); margin-right: 10px;" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="M6.457 1.047c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0 1 14.082 15H1.918a1.75 1.75 0 0 1-1.543-2.575Zm1.763.707a.25.25 0 0 0-.44 0L1.698 13.132a.25.25 0 0 0 .22.368h12.164a.25.25 0 0 0 .22-.368Zm.53 3.996v2.5a.75.75 0 0 1-1.5 0v-2.5a.75.75 0 0 1 1.5 0ZM9 11a1 1 0 1 1-2 0 1 1 0 0 1 2 0Z"></path></svg>|
|`[!Important]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: rgb(130, 80, 223); margin-right: 10px;" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="M0 1.75C0 .784.784 0 1.75 0h12.5C15.216 0 16 .784 16 1.75v9.5A1.75 1.75 0 0 1 14.25 13H8.06l-2.573 2.573A1.458 1.458 0 0 1 3 14.543V13H1.75A1.75 1.75 0 0 1 0 11.25Zm1.75-.25a.25.25 0 0 0-.25.25v9.5c0 .138.112.25.25.25h2a.75.75 0 0 1 .75.75v2.19l2.72-2.72a.749.749 0 0 1 .53-.22h6.5a.25.25 0 0 0 .25-.25v-9.5a.25.25 0 0 0-.25-.25Zm7 2.25v2.5a.75.75 0 0 1-1.5 0v-2.5a.75.75 0 0 1 1.5 0ZM9 9a1 1 0 1 1-2 0 1 1 0 0 1 2 0Z"></path></svg>|
|`[!Tip]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: rgb(26, 127, 55); margin-right: 10px;" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="M8 1.5c-2.363 0-4 1.69-4 3.75 0 .984.424 1.625.984 2.304l.214.253c.223.264.47.556.673.848.284.411.537.896.621 1.49a.75.75 0 0 1-1.484.211c-.04-.282-.163-.547-.37-.847a8.456 8.456 0 0 0-.542-.68c-.084-.1-.173-.205-.268-.32C3.201 7.75 2.5 6.766 2.5 5.25 2.5 2.31 4.863 0 8 0s5.5 2.31 5.5 5.25c0 1.516-.701 2.5-1.328 3.259-.095.115-.184.22-.268.319-.207.245-.383.453-.541.681-.208.3-.33.565-.37.847a.751.751 0 0 1-1.485-.212c.084-.593.337-1.078.621-1.489.203-.292.45-.584.673-.848.075-.088.147-.173.213-.253.561-.679.985-1.32.985-2.304 0-2.06-1.637-3.75-4-3.75ZM5.75 12h4.5a.75.75 0 0 1 0 1.5h-4.5a.75.75 0 0 1 0-1.5ZM6 15.25a.75.75 0 0 1 .75-.75h2.5a.75.75 0 0 1 0 1.5h-2.5a.75.75 0 0 1-.75-.75Z"></path></svg>|
|`[!Note]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: rgb(9, 105, 218); margin-right: 10px;" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8Zm8-6.5a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13ZM6.5 7.75A.75.75 0 0 1 7.25 7h1a.75.75 0 0 1 .75.75v2.75h.25a.75.75 0 0 1 0 1.5h-2a.75.75 0 0 1 0-1.5h.25v-2h-.25a.75.75 0 0 1-.75-.75ZM8 6a1 1 0 1 1 0-2 1 1 0 0 1 0 2Z"></path></svg>|
|`[!Alert]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: #ff7800; margin-right: 10px;" viewBox="0 0 20 20" version="1.1" width="16" height="16" aria-hidden="true"><path d="M12 2c-.5 0-1 .19-1.41.59l-8 8c-.79.78-.79 2.04 0 2.82l8 8c.78.79 2.04.79 2.82 0l8-8c.79-.78.79-2.04 0-2.82l-8-8C13 2.19 12.5 2 12 2m0 2l8 8l-8 8l-8-8m7-5v6h2V7m-2 8v2h2v-2Z"/></svg>|
|`[!Annotation]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; fill: #865e3c; margin-right: 10px;" viewBox="0 0 20 20" version="1.1" width="16" height="16" aria-hidden="true"><path d="M12 15c.81 0 1.5-.3 2.11-.89c.59-.61.89-1.3.89-2.11c0-.81-.3-1.5-.89-2.11C13.5 9.3 12.81 9 12 9c-.81 0-1.5.3-2.11.89C9.3 10.5 9 11.19 9 12c0 .81.3 1.5.89 2.11c.61.59 1.3.89 2.11.89m0-13c2.75 0 5.1 1 7.05 2.95C21 6.9 22 9.25 22 12v1.45c0 1-.35 1.85-1 2.55c-.7.67-1.5 1-2.5 1c-1.2 0-2.19-.5-2.94-1.5c-1 1-2.18 1.5-3.56 1.5c-1.37 0-2.55-.5-3.54-1.46C7.5 14.55 7 13.38 7 12c0-1.37.5-2.55 1.46-3.54C9.45 7.5 10.63 7 12 7c1.38 0 2.55.5 3.54 1.46C16.5 9.45 17 10.63 17 12v1.45c0 .41.16.77.46 1.08c.3.31.65.47 1.04.47c.42 0 .77-.16 1.07-.47c.3-.31.43-.67.43-1.08V12c0-2.19-.77-4.07-2.35-5.65S14.19 4 12 4c-2.19 0-4.07.77-5.65 2.35S4 9.81 4 12c0 2.19.77 4.07 2.35 5.65S9.81 20 12 20h5v2h-5c-2.75 0-5.1-1-7.05-2.95C3 17.1 2 14.75 2 12s1-5.1 2.95-7.05C6.9 3 9.25 2 12 2"/></svg>|
|`[!TransFlag]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; margin-right: 10px;" viewBox="0 0 32 32" width="16" height="16" aria-hidden="true"><path fill="#5BCEFA" d="M0 27c0 2.209 1.791 4 4 4h28c2.209 0 4-1.791 4-4v-1.3H0V27z"/><path fill="#F5A9B8" d="M.026 20.5L0 25.8h36v-5.3z"/><path fill="#EEE" d="M0 15.3h36v5.3H0z"/><path fill="#F5A9B8" d="M0 9.902h36V15.4H0z"/><path fill="#5BCEFA" d="M36 9c0-2.209-1.791-4-4-4H4C1.791 5 0 6.791 0 9v1.2h36V9z"/></svg>|
|`[!Pride]`|<svg style="display: inline-block; overflow: visible !important; vertical-align: sub; margin-right: 10px;" viewBox="0 0 32 32" width="16" height="16" aria-hidden="true"><path fill="#880082" d="M0 27a4 4 0 0 0 4 4h28a4 4 0 0 0 4-4v-.5H0v.5z"/><path fill="#3558A0" d="M0 22.07h36v4.6H0z"/><path fill="#138F3E" d="M0 17.83h36v4.5H0z"/><path fill="#FAD220" d="M0 13.5h36V18H0z"/><path fill="#FF7300" d="M0 9.17h36v4.5H0z"/><path fill="#FF000E" d="M32 5H4a4 4 0 0 0-4 4v.33h36V9a4 4 0 0 0-4-4z"/></svg>|

*Under construction*
