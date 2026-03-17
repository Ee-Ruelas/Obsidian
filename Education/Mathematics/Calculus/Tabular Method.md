The tabular method is a sub-method within the scope of [[Integration by Parts]] (IBP), and is often used to speed the calculation process when doing IBP multiple times.

It consist of creating a table and then following a set of steps to solve quickly.
Lets say that our integral is: $\int x^2xdx$
We can do it regularly by multiplying them but for sake of example we will use the tabular method:
```tikz
\usetikzlibrary{matrix}
\begin{document}
\tikzset{ 
    table/.style={
        matrix of nodes,
        row sep=-\pgflinewidth,
        column sep=-\pgflinewidth,
        nodes={
            rectangle,
            draw=gray,
            align=center
        },
        minimum height=1.5em,
        text depth=0.5ex,
        text height=2ex,
        nodes in empty cells,
%%
        every row/.style={
            nodes={fill=gray!20}
        },
        column 1/.style={
            nodes={text width=2em,font=\bfseries}
        },
        row 1/.style={
            nodes={
                fill=black,
                text=white,
                font=\bfseries
            }
        }
    }
}
  \begin{tikzpicture}

\matrix (m) [table,text width=6em]
{
$u$&$dv$\\
 $x$&$x^2$   \\
 $1$& $\frac{x^3}{3}$  \\
 $0$& $\frac{x^4}{12}$  \\
};
\draw[->,red] (m-2-1.center) -- (m-3-2.center);
\end{tikzpicture}
\end{document}
```





