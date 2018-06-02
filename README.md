# My bachelor thesis for University of Helsinki 

Is great stuff. About Docker and Kubernetes and whatnot.

To compile this to PDF:

1) Install LaTeX distribution such as https://www.tug.org/texlive (installation takes fucking forever on at least Windows)
2) Then compile it: `pdflatex main.tex`
3) Add Bibtex references: `bibtex main`

My Texlive version was `TeX 3.14159265 (TeX Live 2018/W32TeX) kpathsea version 6.3.0` last time I compiled this thing.

https://www.cs.helsinki.fi/i/summanen/teaching/Kandidaatintutkielmat/materiaalit/mallipohja/latex/malli.pdf

## Few words about the .cls-files

Our current TeX template is absolute garbage and shame on our University for distributing it as a basis. 1) It doesn't work 2) it's ancient and 3) it looks like shit.

We had a good basis with https://github.com/UniversityHelsinkiTKTL/tktltiki2 that apparently was a remake of our old own for the previous purposes but for some stupid reason we don't use it. And now that the template has changed a little (eg. our department name went from Laitos to Osasto) we can't use it. Sad.

I did couple changes to our current ancient template like changing the encoding from latin9 to utf8. Yup, that's right. We are given a template that's encoded in latin9. There apparently was an utf8 version but I didn't have access to it (got 403). 5/5.

Also I commented out this thing: `\ref{@lastappendixpage}%` which apparently caused this whole thing blow up. Neat. https://tex.stackexchange.com/questions/371955/hyperref-error-argument-of-hysetreflink-has-an-extra

Also I changed this thing:
```
      \if \@classification
      \else
        \ccs\ \@classification
      \fi
```
to this:
```
      \if \@classification
      \else
        \vspace{2\baselineskip}
        \noindent \ccs\ \\\@classification
      \fi
```
to get the ACM classification on separate line. And maybe there was other reason, can't remember.

But whatever I've already written my thesis and this is just a backup archival and also to share my thesis to those who might want to read it.

Feel free to ping me if you have something to ask. But you're probably finnish so that's considering our culture a very tiny possibility.