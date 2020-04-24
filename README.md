# quantum-bib

A clean and comprehensive bibtex-file containing the most important papers in quantum cryptography and related fields.
It is intended to be used with some modern bibstyle which displays DOI and arxiv hyperlinks (two such styles created by Marco Tomamichel are included). **The spirit is to keep the displayed information rather minimal, but provide a working hyperlink instead.**

project initiated in July 2015
by Christian Schaffner

feel free to use, [pull requests](https://help.github.com/articles/using-pull-requests/) are strongly encouraged!

## Install instructions
### Use the repository
The following assumes you have a personal github account and you are logged in.

1. [fork](https://help.github.com/articles/fork-a-repo) this github repository by clicking on `fork` (in the top right corner of your screen)
2. [clone](https://help.github.com/articles/cloning-a-repository) the repository into the directory where your .tex files are located

   ```
   ~/mypaper> git clone https://github.com/YOUR_GITHUB_USERNAME/quantum-bib.git
   ```
3. include the following in your main tex-file:

   ```
   \bibliographystyle{quantum-bib/bibtex/bst/alphaarxiv}
   \bibliography{quantum-bib/bibtex/bib/full,quantum-bib/bibtex/bib/quantum}
   ```
   if you want full journal titles or
   ```
   \bibliographystyle{quantum-bib/bibtex/bst/alphaarxiv}
   \bibliography{quantum-bib/bibtex/bib/abbr,quantum-bib/bibtex/bib/quantum}
   ```
   if you prefer abbreviated journal titles.

Congrats, you can now properly compile your .tex files as usual:
```
~/mypaper> pdflatex mypaper
~/mypaper> bibtex mypaper
~/mypaper> pdflatex mypaper
~/mypaper> pdflatex mypaper
```

### Contribute to the repository
4. add new references to `quantum-bib/bibtex/bib/quantum.bib`, using [jabref](http://jabref.sourceforge.net/) or any text editor.
5. commit your changes

  ```
  ~/mypaper> git add quantum-bib/bibtex/bib/quantum.bib
  ~/mypaper> git commit -m 'added references'
  ```
6. submit a [pull request](https://help.github.com/articles/using-pull-requests/) 

### Configure a remote for your fork
Follow [these instructions](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
```
$ git remote add upstream https://github.com/cschaffner/quantum-bib.git
```
You can now [sync](https://help.github.com/articles/syncing-a-fork/) other people's changes with your fork. 


## Repository contents:
- `/bibtex/bib/quantum.bib`  contains the bib entries
- `/bibtex/bib/full.bib`     contains full journal names
- `/bibtex/bib/abbr.bib`     contains abbreviated journal names

- `testabbr.tex` a tex file for testing all abbreviated references
- `testfull.tex` a tex file for testing all full references
- 'allrefs.tex'  a tex file containing all citation keys
- `/jabref/jabref-preferences` contains some useful [JabRef](http://jabref.sourceforge.net/) preferences

two bib-styles by Marco Tomamichel which nicely display DOI and arxiv links:
- `/bibtex/bst/alphaarxiv.bst`  based on the regular alpha style
- `/bibtex/bst/arxiv_no_month.bst`   based on the regular abbrv style

