---
title: LaTeX Notes Part I (of n)
categories: [Notes To Remember, LaTeX]
---

This is the first of what I hope to be many reminder pages, detailing the basics that I need to setup LaTeX documents. Usually these are homework assignments, so I don't do a separate title page, instead butting it at the top of the first page.

First things first, we have to have a prelude.

```latex
\documentclass[11pt]{amsart}
\usepackage{geometry}
\geometry{letterpaper}
\usepackage{graphicx}
\usepackage{amssymb}
\usepackage{epstopdf}
\usepackage{fancyhdr}
\usepackage{enumerate}
\DeclareGraphicsRule{.tif}{png}{.png}{`convert #1 `dirname #1`/`basename #1 .tif`.png}
```

The packages I include are pretty standard, and I don't end up using `fancyhdr` too much.

The big things that I always forget are mostly formatting things. First you've got your basic `$` for inline math, and `$$` for standout math. `\begin{align*}` does the same job as `$$`, but for multiple lines.

To create a matrix, I use something of the form

```latex
\left(
  \begin{array}{cc}
    1 & 2 \\
    3 & 4
  \end{array}
\right)
```

To add a graphic, I use the code

```
\adjustbox{valign=t}{
  \includegraphics[width=.8\linewidth]{Image.png}
}
```

That's all I have to write down for right now. Look out for updates to this page, or additional pages later.