---
layout: post
title: "Markdown 基本語法測試"
description: "測試 Markdown 基本語法測試"
date: 2018-08-02 13:43:00+0800
categories: [markdown]
tags:
  - markdown
author: kisaku
image:
  path: /img/2018-08-02-Markdown-Syntax-Test/md_logo.jpg
  width: 1280
  height: 777
comments: true
---

###  1. # 用法

  # 有幾個，代表 Hn，例如：# 代表 H1，## 代表 H2，以此類推，##### 代表 H5。


語法：

```vim

#       H1 標題 
##      H2 標題 
###     H3 標題 
####    H4 標題 
#####   H5 標題 
######  H6 標題 

```
輸出：

<div markdown="1"  class="d-block bg-info"> 
#       H1 標題 
##      H2 標題 
###     H3 標題 
####    H4 標題 
#####   H5 標題 
######  H6 標題 
</div>

***

###  2. - 和 = 

語法：

```vim

# 三個 - 或 = 

減號標題為 H2
---

等號標題為 H1
===

```

輸出：

<div markdown="1"  class="d-block bg-info"> 
減號標題為 H2
---

等號標題為 H1
===
</div>

***

### 3. 分隔線

```vim

* * *

***

*****

- - -

---------------------------------------

```

輸出：

<div markdown="1"  class="d-block bg-info"> 

* * *

***

*****

- - -

---------------------------------------

</div> 

<br/>

***

