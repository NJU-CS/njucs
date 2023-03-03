---
title: Contribution Guidelines
date: 2023-03-03 11:22:36
tags: [contribution]
categories: [contribution]
sticky: 9999
---

Welcome to [NJUCS · Volunteers](https://github.com/NJU-CS)! This is a crash tutorial about how to contribute to this site. If you get any problems, you can open an issue [here](https://github.com/JacyCui/njucs/issues) or you can send an email to 201220014@smail.nju.edu.cn .

<!-- more -->

### Step1: Write a post

A post is a markdown file. A markdown file is just a text file named like `XXX.md`. You can edit it using any editor you like, such as vscode, typora, etc. The entire set of [markdown grammer](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) is supported. 

HTML labels can also be used in a markdown file. 

[Latex math formulas](https://en.wikibooks.org/wiki/LaTeX/Mathematics) can be written inline between two `$`'s like `$e=mc^2$` which looks like $e=mc^2$ . Display mode latex math formulas is also supported.

```latex
$$
\int\frac{1}{\sqrt{1-x^2}}dx = \arcsin(x) + C
$$
```

The above math formula in display mode looks like

$$
\int\frac{1}{\sqrt{1-x^2}}dx = \arcsin(x) + C
$$

Among markdown, html and latex, markdown is the only necessity you have to know.

### Step2: Add the front matter

Front matter refers to the region at the top of a markdown file seperated by two `---`'s, which is written in yaml grammer. You don't have to be familar with yaml. Just follow the structure below.

```yaml
title: Your Post Title
date: YYYY-MM-DD HH:mm:ss
tags: [tag1, tag2, tag3, tag4, tag5]
categories: [category1, category2, category3]
```

|fields|type|value|
|:-:|:-:|:-:|
| `title` | string | the title of your post |
| `date` | date | the date when you create the post |
| `tags` | list of strings | **at most five** tags for a post |
| `categories` | list of strings | **at most three** categories for a post | 

A more concrete example:

```markdown
---
title: 离散数学经验分享
date: 2023-03-03 14:05:33
tags: [离散数学, 计科, 数学]
categories: [学习指南, 经验分享]
---
以下是正文部分。
```

Tags and categories are optional but highly recommended, because they help others find your post easier and faster, which means you're able to help more people through a single post.

### Step3: Publish your post

The file structure of this site is like

```bash
.
├── _config.yml
├── db.json
├── node_modules
├── package-lock.json
├── package.json
├── scaffolds
├── source
│   ├── _data
│   ├── _posts # you need to put your post here
│   ├── about
│   ├── categories
│   ├── images
│   ├── links
│   └── tags
└── themes
```

Put your markdown file in the folder `./source/_posts/` is the only thing you need to do in order to publish a post on this website. Here `.` stands for the root directory of [this repository](https://github.com/JacyCui/njucs).

If you want to publish a post but don't have access to the github repository of this website, just contact any one of us.

### Step4: Wait a few minutes

It takes some time to synchronize between github and netlify. So you need to wait a few minutes to see your post online.
