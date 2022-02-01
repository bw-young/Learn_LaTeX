[Back to Contents](../README.md)

[Setting Up a New Document >](NewArticle.md)

---

# What is LaTeX? #

LaTeX is a sort of programming language that was designed for preparing scientific and technical documents. Where Word, Open Office, Google Docs, and other apps allow you to perform word processing and insert images and tables, it can be challenging to keep the formatting consistent or work with equations. LaTeX aims to make it easy to achieve uniformity and establish consistent, rule-based formatting and layout.

The rudimentary components of every LaTeX document are:

1. Comments
2. Commands
3. The document class
4. Packages
5. Environments

---

## Comments ##

```latex
% words that are ignored by the program.
```

Comments are indicated with the % symbol. Everything that follows the % on that line is ignored when your document is compiled. There are excellent tools to make notes to yourself and to remind yourself what bits of your document are for.

---

## Commands ##

```latex
\usepackage[margin=1in]{geometry}
```

LaTeX is basically a programming language. You implement specific changes to the document using commands, which are invoked with a '\' and followed by the name of the command. Some commands take a number of arguments that are set in one or more pairs of brackets [] and/or braces {}. You will need to learn the syntax for each command you wish to invoke. Some commands operate like function calls in other programming languages, effecting the program (your document) in some way. Other commands are like other programming language's escape sequences, allowing you access to special characters, for example.

---

## The Document Class #

```latex
\documentclass{article}
```

The document class establishes the basic framework for the layout and format of your document. It sets such parameters as font size, margins, if there are multiple columns on a page, how the title page (if any) behaves, and so forth.

The most common document class you are likely to use as a scientist is 'article', though there are numerous other options (report, book, proc, etc.).

The document class is specified in the ***preamble***, which is what we call everything we use to set up the document before we add the document's contents.

---

## Packages ##

```latex
\usepackage[margin=1in]{geometry}
```

Packages are also usually used/imported/activated in the ***preamble***, after the document class has been specified. These provide access to commands that provide functionality that may not be accessible in LaTeX at its simplest level.

The 'geometry' package, for example, is useful for adjusting the general layout of your pages, including adjusting margins and allowing you to turn some pages to landscape orientation.

---

## Environments ##

```latex
\begin{document}
  This is the body text of my document.
\end{document}
```

Environments are spaces with special rules within your document. At its simplest level, these are spaces where LaTeX "knows" what to do with its contents. Everything you wish to go into your document will be in the 'document' environment. If you type words outside of your document environment, LaTeX may fail to compile your document because it doesn't know what to do with words outside of an environment!

You may create and nest other environments, such as an equation or table, within your document. Each environment begins with the ```\begin{}``` command and ends with the ```\end{}``` command.

---

[Setting Up a New Document >](NewArticle.md)
