[Back to Contents](../README.md)

[< Figures](Figures.md)

---

# Bibliography #

The 'natbib' package is a popular choice for utilizing BibTex to manage references, and is included in the preamble:

```latex
\usepackage{natbib}
\bibliographystyle{apalike}
```

You then invoke the Reference section in your article, before ending the 'document' environment, with the ```\bibliography{}``` command. This command takes the bibliography file as a reference. Bibliography files are usually given the \*.bib extension, but it is not necessary to specify the extension when calling ```\bibliography{}```.

```
\begin{document}
...

\bibligraphy{refs}

\end{document}
```

---

## Citations ##

All citations have a tag or label given them in the bibliography file. Conventions change between people, and you may want to change them to your own style if downloading a \*.bib reference from the internet. However, once you have the tag, you invoke it using the ```\citep{}``` or ```\citet{}``` commands.

```\citep{}``` is a paranthetical citation (Mortimer et al., 2015).

```\citet{}``` is an in-text citation, such as Mortimer et al. (2015).

Multiple references can be cited with one command, separating their tags with a comma.

```latex
We found the results of \citet{mort.et.2015} to be most intuitive to addressing the challenge of squids in our flumes \citep{gran.1988, octo.fran.2011}.
```

It is sometimes useful to include notes within an paranthetical reference, include "e.g.," "i.e.," and "and so forth." In this case ```\citep[][]{}``` takes two additional arguments. The first [] is the prefix, and second [] is the postfix. There is a space between each of the prefix, the citations, and the postfix. You *must* use both [], even if one is empty, otherwise it assumes only the postfix.

```latex
Other researchers, however, have discovered more fundamental, if less intuitive, causal linkages between squids and flumes \citep[e.g.,][]{cosa.et.2001}.
```

---

## The Bibliography File ##

The bibliography generally follows rules similar to LaTeX proper. The general syntax for a bibliography entry in the bibliography file is:

```bibtex
@documenttype{tag,
  author = {first1 middle1 last1 and last2, first2 middle2},
  title = {Publication title},
  other_fields = {},
 }
```

Authors are separated by the word 'and'. You can specify that two words must go together, or must use the capitalization you specify, by using brackets {}. For example, Vincent Van Goh should be referenced as "Van Gogh, Vincent" and not as "Gogh, Vincent Van." You specify this as ```author = {{Van Gogh}, Vincent}```.

Accents and special characters can also be specified using commands and brackets {}. An example is given below.

The most common document types encountered in the physical sciences are likely to be 'article,' 'incollection,' and 'book.' Here are some examples of each:

```bibtex
@article{bait.et.2014,
    author  = {Baitis, Elke and Kocurek, Gary and Smith, Virginia and Mohrig, David and Ewing, Ryan C. and Peyret, A.-P.B.},
    title   = {Definition and origin of the dune-field pattern at White Sands, New Mexico},
    journal = {Aeolian Research},
    year    = {2014},
    volume  = {15},
    pages   = {269--287},
    doi     = {10.1016/j.aeolia.2014.06.004},
}

@incollection{bohn.anto.2009,
	author    = {B{\"{o}}hner, J. and Antoni{\'{c}}, O.},
	title     = {Land-surface parameters specific to topo-climatology},
	booktitle = {Geomorphometry: Concepts, software, applications},
	editor    = {Hengl, Tomislav and Reuter, Hannes I.},
	series    = {Developments in Soil Science},
	year      = {2009},
	volume    = {33},
	pages     = {195--226},
	publisher = {Elsevier},
	address   = {New York, NY, USA},
	doi       = {10.1016/S0166-2481(08)00008-1},
}

@book{beer.et.2006,
	author    = {Beer, F. P. and Johnston, E. R. and De Wolf, J. T.},
	title     = {Mechanics of Materials: Fourth Edition in SI Units},
	year      = {2006},
	publisher = {McGraw-Hill},
	address   = {New York, NY, USA},
}
```

Note that you can use quotations "" instead of brackets {}, but I found the brackets to be the most inuitive for communicating the record hierarchy, and sometimes it seems quotations aren't required but not in a way that I've been able to reliably predict.

```bibtex
@article{bait.et.2014,
    author  = "Baitis, Elke and Kocurek, Gary and Smith, Virginia and Mohrig, David and Ewing, Ryan C. and Peyret, A.-P.B.",
    title   = "Definition and origin of the dune-field pattern at White Sands, New Mexico",
    journal = "Aeolian Research",
    year    = 2014,
    volume  = "15",
    pages   = "269--287",
    doi     = "10.1016/j.aeolia.2014.06.004",
}
```
