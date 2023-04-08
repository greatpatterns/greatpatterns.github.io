---
layout: page
title: LaTeX Cheat Sheet: xy-plane
---

The following LaTeX codes will generate a 5x5 $$xy$$-plane:

```
\begin{tikzpicture}[scale=0.6]
% draw the grid
\draw[very thin,color=gray!50] (-5,-5) grid (5,5);
% draw the x-axis and y-axis
\draw[<->,thick] (-5.5,0) -- (5.5,0);
\draw[<->,thick] (0,-5.5) -- (0,5.5);
% label the ticks on the x-axis
\foreach \x in {-5,-4,...,5} {
    \draw (\x,-0.1) -- (\x,0.1);
}
% label the ticks on the y-axis
\foreach \y in {-5,-4,...,5} {
    \draw (-0.1,\y) -- (0.1,\y);
}
\end{tikzpicture}
```

Package needed: `\usepackage{tikz}`