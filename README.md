# quantum-bib

A clean and comprehensive bibtex-file containing the most important papers in quantum cryptography and related fields.
It is intended to be used with some modern bibstyle which displays DOI and arxiv hyperlinks (two such styles created by Marco Tomamichel are included). **The spirit is to keep the displayed information rather minimal, but provide a working hyperlink instead.**

project initiated in July 2015
by Christian Schaffner and Filippos Vogiatzian

feel free to use, [pull requests](https://help.github.com/articles/using-pull-requests/) are strongly encouraged!


###Repository contents:
- `/bibtex/bib/quantum.bib`  contains the bib entries

two bib-styles by Marco Tomamichel which nicely display DOI and arxiv links:
- `/bibtex/bst/alphaarxiv.bst`  based on the regular alpha style
- `/bibtex/bst/arxiv_no_month.bst`   based on the regular abbrv style

##Formatting conventions
* The *citation-key* ("GM84" in the first example below) is the same as in the alpha style, so first letters of up to three authors, together with two digits of the publication year
* Full names of authors with proper latex spelling including special characters should be provided

See [here](https://en.wikipedia.org/wiki/BibTeX#Entry_types) for a list of possible bibtex entries.

###Example entry for @article
```
@article{GM84,
abstract = {A new probabilistic model of data encryption is introduced. For this model, under suitable complexity assumptions, it is proved that extracting any information about the cleartext from the cyphertext is hard on the average for an adversary with polynomially bounded computational resources. The proof holds for any message space with any probability distribution. The first implementation of this model is presented. The security of this implementation is proved under the intractability assumption of deciding Quadratic Residuosity modulo composite numbers whose factorization is unknown.},
author = {Goldwasser, Shafi and Micali, Silvio},
doi = {10.1016/0022-0000(84)90070-9},
isbn = {0022-0000},
issn = {00220000},
journal = {Journal of Computer and System Sciences},
month = apr,
number = {2},
pages = {270--299},
publisher = {Elsevier},
title = {{Probabilistic encryption}},
url = {http://linkinghub.elsevier.com/retrieve/pii/0022000084900709},
volume = {28},
year = {1984}
}
```

Required fields:
* author
* title
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
@inproceedings{Unr12,
author = {Unruh, Dominique},
booktitle = {Advances in Cryptology – EUROCRYPT 2012},
doi = {10.1007/978-3-642-29011-4\_10},
isbn = {9783642290107},
issn = {03029743},
pages = {135--152},
publisher = {Springer},
series = {LNCS},
title = {{Quantum Proofs of Knowledge}},
url = {http://link.springer.com/10.1007/978-3-642-29011-4\_10},
volume = {7237},
year = {2012}
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
@book{BBD09,
abstract = {Digital signatures have become a key technology for making the Internet and other IT-infrastructures secure. Digital signatures provide authenticity, integrity, and non-repudiation of data. Digital signatures are widely used in identification and authentication protocols. Therefore, the existence of secure digital signature algorithms is crucial for maintaining IT-security. The digital signature algorithms that are used in practice today are RSA [31], DSA [11], and ECDSA [15]. They are not quantum immune since their security relies on the difficulty of factoring large composite integers and computing discrete logarithms.},
address = {Berlin, Heidelberg},
author = {Buchmann, Johannes and Dahmen, Erik and Szydlo, Michael},
booktitle = {Post-Quantum Cryptography},
doi = {10.1007/978-3-540-88702-7},
editor = {Bernstein, Daniel J and Buchmann, Johannes and Dahmen, Erik},
isbn = {978-3-540-88701-0},
pages = {35--93},
publisher = {Springer Berlin Heidelberg},
title = {{Post-Quantum Cryptography}},
url = {http://link.springer.com/10.1007/978-3-540-88702-7},
year = {2009}
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
