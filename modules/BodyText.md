[Back to Contents](../CONTENTS.md)

[< Setting Up a New Document](NewArticle.md) | [Equations >](Equations.md)

---

# Body Text #

Now that you have your document class set up and are in the 'document' environment, it's time to fill your document with content.

For most body text, you may simply type and what you see is what you'll get, in the font and format specified by your document class and packages. However, you may wish to *italicize* or *bold* some of your text. The ```\textit``` command lets you italicize letters, and ```\textbf``` lets you bold things. You can nest these command to combine them.

```latex
Now \textit{this} is what I'm \textbf{what} I'm talking \textbf{\textit{about}}!
```

Paragraphs are separated with a blank line between them.

 ```latex
 This is a paragraph.
 This continues that paragraph.
 
 But this is a new paragraph.
 ```

In the 'article' document class, the first line of each paragraph after the first paragraph is indented. If you don't want a paragraph to be indented, just indicate with the ```\noindent``` command at the head of the paragraph.

```latex
\noindent This is a new, un-indented paragraph.
```

or

```latex
\noindent
This is a new, un-indented paragraph.
```

I favor the latter, as I believe it is easier to identify the paragraphs without indentation. I usually use this on a paragraph following a equation, where I define variables ("where X is this and Y is that").

## Sections and Headings ##

The sections and headings hierarchy of the document is established using the ```\section{}```, ```\subsection{}```, and ```\subsubsection{}``` commands. I'm sure some document classes go into subsubsubsubsubsection, but it's probably best to simplify the structure of your document and keep it to a hierarchy that's more approachable for both journal editors and readership alike to go no deeper than 3 header levels.

```latex
\section{Methods}

This my methods section.

\subsection{Data}

These are the data I used.

\subsection{What I Did}

\subsubsection{What I Did First}

Some neat stuff.

\subsubsection{What I Did Second}

And that's why you can totally trust this research.

\section{Results}

This is what came of all that hard work.
```

---

[< Setting Up a New Document](NewArticle.md) | [Equations >](Equations.md)
