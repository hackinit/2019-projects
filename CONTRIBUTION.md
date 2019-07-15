# 如何将我的项目加入本列表

为了将你在 [THE Hack 2019](https://thehack.org.cn) 完成或是提出想法的项目加入本列表，你将需要通过 Pull Request 提交你的请求。

### Fork repo

你需要首先点击 GitHub 右上角的 Fork 按钮，建立你自己的分支。在 fork 完成后，你将会被自动重定向到你自己的 Fork repo 内。

### 编辑 [`README.md`](/README.md) 并加入项目简介

请在 README.md 文件中以**二级标题**的形式加入你自己的项目名称。你还可以在项目名称后自由地添加任何徽章（比如：编译状态、版本号、star数量等）。

在项目名称以及徽章（如果你添加了的话）后，你可以加入你们队伍的名称、成员、ID、个人网站/社交网站链接，以及你们的项目官方网站链接、demo链接、代码库链接等。

之后，你可以附上一段**不超过500字**的项目简介，你也可以在你的项目简介内添加1张图片。

以下提供一段范例代码：

```markdown
## Ruff Over-heating Detector
[![Dependency Status](https://david-dm.org/hackinit/ruff-overheating-detector.svg)](https://david-dm.org/hackinit/ruff-overheating-detector.svg)

*THE Hack 2019 Staff - Tech Dept.*  
成员： @yechs（[GitHub](https://github.com/yechs) | [知乎](https://example.org) | [个人网站](https://example.org)） @neyctech（[GitHub](https://github.com/neyctech)） et al.

[项目网址](https://example.org) | [Demo 链接](https://example.org) | [GitHub repo](https://github.com/hackinit/ruff-overheating-detector)

一个基于Ruff物联网开发套件开发的用于防止导线过热的检测器。该产品会通过温度传感器读入导线温度，并显示在连接的显示屏上。你也可以通过接入 Ruff 开发板的 Wi-Fi 网络以对数据进行远程监视。此外，当导线温度超过40摄氏度时，蜂鸣器会立即进行示警。
```

### 通过 git submodule 的方式添加你的代码（可选）

如果你乐意将你的代码开源的话，你也可以通过 git submodule 的方式将你的代码链接放在本 repo 内。在 Windows 上，你将可以通过 Git Bash 运行以下代码。

以下代码以 [hackinit/ruff-overheating-detector](https://github.com/hackinit/ruff-overheating-detector) 为例，在 Windows 上通过 git bash 添加代码：

```console
$ git clone https://github.com/[你的用户名]/2019-projects # 注意这里需要 clone 你 fork 之后的 repo
$ cd 2019-projects

$ # 注意这一条命令中，需要将 Git 地址与目录名称替换成你自己的项目。
$ # 你可以在 GitHub 页面上点击 "Clone or download" 获取自己项目的 Git 链接
$ git submodule add https://github.com/hackinit/ruff-overheating-detector.git ruff-overheating-detector 
Cloning into 'D:/THE-Hack/2019-projects/ruff-overheating-detector'...
remote: Enumerating objects: 127, done.
remote: Counting objects: 100% (127/127), done.
remote: Compressing objects: 100% (76/76), done.
Receiving objects:  remote: Total 127 (delta 29), reused 115 (delta 26), pack-reused 0
Receiving objects: 100% (127/127), 176.92 KiB | 751.00 KiB/s, done.
Resolving deltas: 100% (29/29), done.
```

通过 `git status`，你会发现 git submodule 已经生成了两个文件，并自动将他们添加到了 Git index 中。你可以直接 commit 了

```console
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   .gitmodules
        new file:   ruff-overheating-detector
        
$ git commit -m "Add ruff-overheating-detector" # 这里可以将 -m 之后引号内的信息替换成任何你想要的 commit message
[master 154d9ec] Add ruff-overheating-detector
 2 files changed, 4 insertions(+)
 create mode 100644 .gitmodules
 create mode 160000 ruff-overheating-detector
```

随后，你就可以将你的编辑通过 `git push` push 到你自己的 repo 了

### 提交 Pull Request

在一切就绪之后，你只需要回到你 fork 的 repo 首页，点击 "New Pull Request"，并确定 base-repository 为 "hackinit/2019-projects"，且 base 为 "master"，然后你就可以提交你的 Pull Request了。

提交 PR 后，我们会尽快 merge，merge 后你的项目就将被显示在本 repo 的首页上。
