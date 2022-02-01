[Back to Contents](../README.md)

[< Body Text](BodyText.md) | [Tables >](Tables.md)

---

# Equations #

Some people prefer to use LaTeX simply because of its flexible equations framework, particularly when the 'amsmath' package is being used.

A simple equation environment will look something like this:

```latex
\begin{equation}
  y = mx + b
\end{equation}
```

As with headers, if you don't want an equation number, just include an asterisk (\*).

```latex
\begin{equation}
 A = BC + D
\end{equation}
```

## Symbols ##

There are some great look-up tables online for all of the possible symbols you might want to consider. Common ones are greek symbols, logical operators, and set operators.

| Symbol   | Command | Symbol | Command | Symbol       | Command |
| ------   | ------- | ------ | ------- | ------       | ------- |
| &alpha;  | \alpha  | <      | <       | in set       | \in     |
| &Beta;   | \Beta   | >      | >       | union        | \cup    |
| &Delta;  | \Delta  | =      | =       | intersection | \cap    |
| &gamma;  | \gamma  | &le;   | \leq    | sum          | \sum    |
| &varphi; | \phi    | &ge;   | \geq    | product      | \prod   |
| &phi;    | \varphi |        |         |              |         |
| &theta;  | \theta  |        |         |              |         |

```latex
\begin{equation}
  \Omega = \varphi \theta + \gamma
\end{equation}
```

## Fractions ##

Fractions can be stacked using the ```frac{}{}``` command, where the first {} takes arguments that go in the numerator, and the second {} takes arguments that go in the denominator.

```latex
\begin{equation}
  m = \frac{x - a}{y - b}
\end{equation}
```

## Superscripts and Subscripts ##

Superscripts are indicated with '^', subscripts with '\_'. If you must include more than one symbol in the super/subscript, enclose it with braces {}.

```latex
\begin{equation}
  E = mc^2
\end{equation}
```

## Equations in Text ##

You can include equations or mathematical symbols, operators, superscripts, etc. within the body text by enclosing it in $$.

```latex
This is some text where I refer to $\Delta$ being 10 $^\circ$C, because $R=\frac{xY}{v}$.
```

## Text in Equations ##

Sometimes, you don't want something italicized while it's in an equation context. Use the ```\text{}``` command for that.

```latex
\begin{equation}
  \text{A} = \Beta / \text{C},
\end{equation}

\noindent
where $\Beta / \text{C}$ is something meaningful.
```

## Parantheses ##

Enclose portions of equations using parantheses, brackets, or braces using exactly those symbols. However, if you include fractions or large symbols (such as the sum operator) and you want the parantheses to be large enough to enclose them, you need to use the ```\left(``` and ```\right)``` commands.

```latex
\begin{equation}
	\sigma = \frac{1}{N} \sum_{i=1}^N \left( x_i^2 \right) - \bar{x}^2,
\end{equation}

\noindent
where $\sigma$ is the standard deviation of population $x$ of $N$ elements and an average of $\bar{x}$.
```

---

[< Body Text](BodyText.md) | [Tables >](Tables.md)
