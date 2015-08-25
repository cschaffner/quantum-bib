# quantum-bib

A clean and comprehensive bibtex-file containing the most important papers in quantum cryptography and related fields.
It is intended to be used with some modern bibstyle which displays DOI and arxiv hyperlinks (two such styles created by Marco Tomamichel are included). **The spirit is to keep the displayed information rather minimal, but provide a working hyperlink instead.**

project initiated in July 2015
by Christian Schaffner

feel free to use, [pull requests](https://help.github.com/articles/using-pull-requests/) are strongly encouraged!

##Install instructions
####Use the repository
The following assumes you have a personal github account and you are logged in.

1. [fork](https://help.github.com/articles/fork-a-repo) this github repository by clicking on `fork` (in the top right corner of your screen)
2. [clone](https://help.github.com/articles/cloning-a-repository) the repository into the directory where your .tex files are located

   ```
   ~/mypaper> git clone https://github.com/YOUR_GITHUB_USERNAME/quantum-bib.git
   ```
3. include the following in your main tex-file:

   ```
   \bibliographystyle{quantum-bib/bibtex/bst/alphaarxiv}
   \bibliography{quantum-bib/bibtex/bib/quantum}
   ```

Congrats, you can now properly compile your .tex files as usual:
```
~/mypaper> pdflatex mypaper
~/mypaper> bibtex mypaper
~/mypaper> pdflatex mypaper
~/mypaper> pdflatex mypaper
```

####Contribute to the repository
4. add new references to `quantum-bib/bibtex/bib/quantum.bib`, using [jabref](http://jabref.sourceforge.net/) or any text editor.
5. commit your changes

  ```
  ~/mypaper> git add quantum-bib/bibtex/bib/quantum.bib
  ~/mypaper> git commit -m 'added references'
  ```
6. submit a [pull request](https://help.github.com/articles/using-pull-requests/) 

####Configure a remote for your fork
Follow [these instructions](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
```
$ git remote add upstream https://github.com/cschaffner/quantum-bib.git
```
You can now [sync](https://help.github.com/articles/syncing-a-fork/) other people's changes with your fork. 


##Repository contents:
- `/bibtex/bib/quantum.bib`  contains the bib entries

- `test.tex` a tex file for testing all references
- `/jabref/jabref-preferences` contains some useful [JabRef](http://jabref.sourceforge.net/) preferences

two bib-styles by Marco Tomamichel which nicely display DOI and arxiv links:
- `/bibtex/bst/alphaarxiv.bst`  based on the regular alpha style
- `/bibtex/bst/arxiv_no_month.bst`   based on the regular abbrv style

##Formatting conventions
* The *citation-key* ("GM84" in the first example below) is the same as in the alpha style, so first letters of up to four authors, together with two digits of the publication year. In [JabRef](http://jabref.sourceforge.net/), this corresponds to the `[authorsAlpha][shortyear]` setting.
* Full names of authors with proper latex spelling including special characters should be provided

See [here](https://en.wikipedia.org/wiki/BibTeX#Entry_types) for a list of possible bibtex entries.

###Example entry for @article
```
@Article{GM84,
  Title                    = {{Probabilistic encryption}},
  Author                   = {Goldwasser, Shafi and Micali, Silvio},
  Journal                  = {Journal of Computer and System Sciences},
  Year                     = {1984},

  Month                    = apr,
  Number                   = {2},
  Pages                    = {270--299},
  Volume                   = {28},

  Abstract                 = {A new probabilistic model of data encryption is introduced. For this model, under suitable complexity assumptions, it is proved that extracting any information about the cleartext from the cyphertext is hard on the average for an adversary with polynomially bounded computational resources. The proof holds for any message space with any probability distribution. The first implementation of this model is presented. The security of this implementation is proved under the intractability assumption of deciding Quadratic Residuosity modulo composite numbers whose factorization is unknown.},
  Doi                      = {10.1016/0022-0000(84)90070-9},
  ISBN                     = {0022-0000},
  ISSN                     = {00220000},
  Publisher                = {Elsevier},
  Url                      = {http://linkinghub.elsevier.com/retrieve/pii/0022000084900709}
}
```

Required fields:
* title
* author
* journal
* number
* pages
* year
* DOI

Ignored fields: (if they are included, they should be correct)
* archivePrefix
* archiveId
* eprint
* month
* url
* isbn
* issn
* abstract

###Example entry for @inproceedings
```
@InProceedings{Unr12,
  Title                    = {{Quantum Proofs of Knowledge}},
  Author                   = {Unruh, Dominique},
  Booktitle                = {Advances in Cryptology – EUROCRYPT 2012},
  Year                     = {2012},
  Pages                    = {135--152},
  Publisher                = {Springer},
  Series                   = {LNCS},
  Volume                   = {7237},

  Doi                      = {10.1007/978-3-642-29011-4\_10},
  ISBN                     = {9783642290107},
  ISSN                     = {03029743},
  Url                      = {http://link.springer.com/10.1007/978-3-642-29011-4\_10}
}
```

Required fields:
* author
* booktitle
* pages
* series
* year
* volume
* DOI

Ignored fields: (if they are included, they should be correct)
* archivePrefix
* archiveId
* eprint
* month
* editor
* publisher
* url
* abstract


###Example entry for @book
```
@Book{BBD09,
  Title                    = {{Post-Quantum Cryptography}},
  Editor                   = {Bernstein, Daniel J and Buchmann, Johannes and Dahmen, Erik},
  Publisher                = {Springer},
  Year                     = {2009},
  Series                   = {LNCS},

  Abstract                 = {Digital signatures have become a key technology for making the Internet and other IT-infrastructures secure. Digital signatures provide authenticity, integrity, and non-repudiation of data. Digital signatures are widely used in identification and authentication protocols. Therefore, the existence of secure digital signature algorithms is crucial for maintaining IT-security. The digital signature algorithms that are used in practice today are RSA [31], DSA [11], and ECDSA [15]. They are not quantum immune since their security relies on the difficulty of factoring large composite integers and computing discrete logarithms.},
  Booktitle                = {Post-Quantum Cryptography},
  Doi                      = {10.1007/978-3-540-88702-7},
  ISBN                     = {978-3-540-88701-0},
  Pages                    = {35--93},
  Url                      = {http://link.springer.com/10.1007/978-3-540-88702-7}
}
```

Required fields:
* editor/author
* booktitle
* publisher
* year
* DOI / ISBN (not all publishers (e.g. Cambridge University Press) seem to provide a DOI, provide ISBN instead.)

Ignored fields: (if they are included, they should be correct)
* archivePrefix
* archiveId
* eprint
* month
* url
* abstract
