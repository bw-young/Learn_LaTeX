[Back to Contents](../CONTENTS.md)

[< Introduction](Introduction.md) | [Body Text >](BodyText.md)

---

# Setting Up a New Document #

Setting a new document is pretty straight-forward, and can usually be done by copying-and-pasting preambles from other documents you've created, if you're not given another template to work with.

## Preamble ##

First, we must establish the preamble by selecting a document class and identifying which packages we wish to use.

Common packages include geometry, amsmath, graphicx, and natbib. These help with page layout, formatting equations, setting graphics and figures, and managing/interpreting the bibliography, respectively.

```latex
\documentclass{article}

\usepackage[utf8]{inputenc}
\usepackage[margin=1in]{geometry}
\usepackage{array} % for extending the array and tabular environments
\usepackage{amsmath} % for math
\usepackage{graphicx} % for figures and graphics

\usepackage{natbib} % for references/citations
\bibliographystyle{apalike}
```

Title-page information is often established in the preamble as well.

```latex
\title{My Title}
\author{Myself I. Me \and You R. Awesome}
```

## The Document Environment ##

Following the preamble, it's time to begin the document.

```latex
\begin{document}
	\titlepage
  
  \abstract{This document is about stuff. You should read it.}
\end{document}
```

Although the title and authors were specified in the preamble, they are sorted into a neat title using the ```\titlepage``` command. You'll note that creating the abstract is a command, rather than just regular text with a header above it. You *could* have your abstract be a section with a header, but journals will generally know better how to manage your abstract if you pass it as an argument to the ```\abstract``` command.

---

[< Introduction](Introduction.md) | [Body Text >](BodyText.md)
