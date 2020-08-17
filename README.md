# pyquirk
A simple python program to convert graphical circuits to quantikz figures.

## Requirements
- Python 3+
- [quantikz](https://ctan.org/pkg/quantikz?lang=en): A LaTeX package for drawing quantum circuits. Here is its [manual](http://mirrors.ibiblio.org/CTAN/graphics/pgf/contrib/quantikz/quantikz.pdf).

##### How to manually install a new package on MikTeX on Windows?
- [Windows with MikTeX](https://tex.stackexchange.com/questions/2063/how-can-i-manually-install-a-package-on-miktex-windows)
- [Linux](https://tex.stackexchange.com/questions/73016/how-do-i-install-an-individual-package-on-a-linux-system)
- [Mac with TeXShop](https://tex.stackexchange.com/questions/12102/how-do-i-install-ctan-packages-on-mac-os-with-texshop)

## Usage

Copy and paste the JSON data of your circuit from [Quirk](https://algassert.com/quirk) into a `.txt` file. The output is formatted into a `.tex` file.

**For example:** `python3 pyquirk.py circuit_json.txt -o circuit.tex`

A short rundown of **quantikz** usage:
```latex
\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{quantikz}

\begin{document}
\begin{quantikz}

...circuit code goes here...

\end{quantikz}
\end{document}
```

## Future improvements
- To add more complex examples.
- Parsing from URL.
- Multiple targets for same control.