# Latex-Vorlage

Dies ist eine Latexvorlage (freundlicherweise zur Verfügung gestellt von [Robin Strickstrock](https://www.h-brs.de/de/emt/robin-strickstrock)), die sie benutzen können, aber nicht müssen.

 - Das Hauptdokument ist `main.tex`. Hier werden alle anderen `.tex`-files inkludiert.
 - Alle verwendeten Pakete müssen in `preamble.tex` über 
   ```latex
   \usepackage{package_name}
   ```
   eingebunden werden.
 - Solange das Hauptdokument `main.tex` heißt, wird es über Continuous Integration mit jedem *push* gebaut.

## Nützliche Links

 - Zum Arbeiten mit Latex benötigen Sie zwingend eine Latexdistribution (für Windows üblicherweise [Miktex](https://miktex.org/), für Mac [MacTeX](http://www.tug.org/mactex/) und für Linux [texlive](https://www.tug.org/texlive/)). Hilfreich ist noch ein Editor wie [Texmaker](https://www.xm1math.net/texmaker/) oder [Kile](https://kile.sourceforge.io/).
 - Unter [diesem Link](https://latex.tugraz.at/latex/warum) finden Sie empfehlenswerte, ausführliche Latexanleitungen von der TU Graz. 
 - [Latex Cheatsheet](http://www.latex4ei.de/downloads/LaTeX_CheatSheet.pdf)