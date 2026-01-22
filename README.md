# Language Science Press Guidelines for References and Citations

## Introduction

Here are guidelines about how to format citations and references in LaTeX `.tex` and BibTeX `.bib` 
files for Language Science Press books.

Language Science Press has a tool for converting plain text bibliographic entries to BibTeX 
format, <https://www.langsci-press-gug.org/doc2tex/doc2bib>, and a tool for normalizing BibTeX 
entries according to Language Science Press style, 
<https://www.langsci-press-gug.org/doc2tex/normalizebib>. 
See all Language Science Press templates and tools, <https://langsci-press.org/templatesAndTools>.

Language Science Press follows the *Generic Style Rules for Linguistics* and the 
*Unified Style Sheet for Linguistics*, with a few customizations. 
See the Language Science Press guidelines, <https://langsci-press.org/guidelines>.

## BibTeX entry

This is a BibTeX entry.

```
@type{key,
	field1 = {value1},
	field2 = {value2},
	...
}

@article{Milewski1951,
	author = {Milewski, Tadeusz},
	journal = {Lingua Posnaniensis},
	pages = {248--268},
	title = {The conception of the word in languages of {North American} natives},
	volume = {3},
	year = {1951}
}
```

The BibTeX entry type is the word after the ampersand `@`, commonly `article`, `book`, 
`incollection`, `phdthesis`, and `misc`.

The BibTeX entry key is the alphanumeric string after the opening brace `{`.
Conventionally, the key is the author surname(s) followed by the year, and maybe a suffix 
to disambiguate works in the same year or help you identify the work,
e.g. `Yu2003`, `Yu2003a`, `Yu2003thesis`, `MalingZaenen1985`, `JohnsonEtAl1989`.
Conventionally, the key does not use diacritics and is stripped to ASCII (A–Z, a–z).
The key cannot contain certain characters: space ` `; ampersand `&`; comma `,`; 
quotes `"`, `'`; backslash `\`; percent `%`; and braces and brackets `{`, `}`, `[`, `]`.

The BibTeX entry has field/value pairs. 
The fields `author`,  `title`,  and `year` are generally required for all entries.
Conventionally, values are enclosed in braces, `{...}`.
The final field/value pair can omit the separating comma after the value.

Values can be enclosed in double quote marks, and some numeric values can be unbraced, 
but Language Science Press prefers braced values.


## Full first names

Please provide full first names for authors and editors, so 

```
author = {Noam Chomsky}
*author = {N. Chomsky}
```

Middle initials do not have to be expanded

```
author  = {Larry M. Hyman}
*author  = {Larry Michael Hyman}
```

Some people use their second name as their full name. There is no need to expand the first name then. 

```
author = {D. Robert Ladd}
*author = {Dwight Robert Ladd}
```

Some authors have pen names which consist only of initials. Most notable are R. M. W. Dixon, 
N. J. Enfield, M. A. K. Halliday and A. E. Meussen. Do not use expanded names for these authors. 


## Workflow

Please deliver a BibTeX file with all your references together with your submissions.
BibTeX can be exported from all common bibliography tools. 

Use a reference manager. 
Language Science Press recommends JabRef. On Mac, you can also use BibDesk.

Each Language Science Press book has a single BibTeX file named `localbibliography.bib`.
Bibliography files of papers/chapters by contributors in an edited volumes are collated and 
reconciled by the volume editors or the Language Science Press team.

### LaTeX skeletons

When using a LaTeX template or skeleton from Language Science Press, use the file `localbibliography.bib` 
provided there. There are some dummy entries in that file. You can delete them and add your own entries instead. 

### Zotero

If using Zotero and Better BibTeX, then change these settings from their default.
Set “Export unicode as plain-text latex commands” to `no`.
Set “When an item has both a DOI and a URL, export” to `DOI`.

## LaTeX encoding

In most text contexts in LaTeX, some reserved characters must be escaped with a backslash `\`, 
but not in the context of the `doi` and `url` fields.

### Ampersand `&`

```
journal = {Natural Language \& Linguistic Theory},
publisher = {Taylor \& Francis},
volume  = {2 \& 3},

url = {http://sas.ujc.cas.cz/archiv.php?lang=en&art=972},
```

### Underscore `_`

```
doi = {10.1001/12345_3}
```

### Number sign `#`

```
title = {``I can't believe \#{Z}iggy \#{S}tardust died''. {S}tance, fan identities and multimodality in reactions to the death of {David Bowie} on {I}nstagram},
title = {What you can cram into a single \$\&!\#* vector: {P}robing sentence embeddings for linguistic properties},
```

### Percent `%`
```
url = {https://darkwing.uoregon.edu/~dlpayne/Maa%20Lexicon/lexicon/main.htm},

title = {95\% confidence interval: {A} misunderstood statistical tool},
```

## Translation

In an English bibliography, a non-English `title` can be given in the original script
or in English transliteration, or both, or with an English translation.
Note that `title` font style depends on kind of title: a book title is italic, and 
an article title is roman.
Use the `titleaddon` field (which is always in roman) for a translation, 
and put the translation in square brackets.
Conventionally, the original script title is in parentheses after an Englsh transliteration.
That is, “Transliteration (Original script) \[Translation\]”.

The `titleaddon` is displayed immediately after after the `title`, always in roman, 
not italic, which is particularly desirable for the square brackets around a translation 
or the parentheses around the original script.
The `titleaddon` is not subject to decapitalization, so extra braces are not needed to 
protect capitals.

To avoid italic style, like for parentheses, use the `\textnormal{}` command to force roman style.

```
@book{Haga1998,
	address = {Tokyo},
	author = {Haga, Yasushi},
	publisher = {Ningen no Kagaku Sha},
	title = {Nihongo no shakai shinri},
	titleaddon = {[Social psychology in the Japanese language]},
	year = {1998}
}
	
@article{Chen2013,
	author = {Chen, Shu-chuan (陳淑娟)},
	journal = {Language and Linguistics \textnormal{(語言暨語言學)}},
	number = {2},
	pages = {371--408},
	title = {Taibei {Shezi} fangyan de yuyin bianyi yu bianhua (台北社子方言的語音變異與變化)},
	titleaddon = {[The sound variation and change of Shezi dialect in Taipei City]},
	volume = {14},
	year = {2013},
	url = {https://www.ling.sinica.edu.tw/item/en?act=journal&code=download&article_id=426},
}
```

> Haga, Yasushi. 1998. *Nihongo no shakai shinri*. \[Social psychology in the Japanese language\]. 
> Tokyo: Ningen no Kagaku Sha.
>
> Chen, Shu-chuan (陳淑娟). 2013. Taibei Shezi fangyan de yuyin bianyi yu bianhua
> (台北社子方言的語音變異與變化). \[The sound variation and change of Shezi dialect in Taipei City\]. 
> *Language and Linguistics* (語言暨語言學) 14(2). 371–408. 
> <https://www.ling.sinica.edu.tw/item/en?act=journal&code=download&article_id=426>.

## Citations

### Citation commands

The basic commands for citations are `\citep{}`, `\citet{}`, and `\citealt{}`.

| Source | Output |
| :--- | :--- |
| `\cite{Yu2003}` | Yu 2003 |
| `\citep{Yu2003}` | (Yu 2003) |
| `\citep[12]{Yu2003}` | (Yu 2003: 12) |
| `\citep{Erdal2007,Yu2003}` | (Erdal 2007, Yu 2003) |
| `\citep{MalingZaenen1985}` | (Maling & Zaenen 1985) |
| `\citep{JohnsonEtAl1989}` | (Johnson et al. 1989) |
| `\citet{Yu2003}` | Yu (2003) |
| `\citet[12]{Yu2003}` | Yu (2003: 12) |
| `\citealt{Yu2003}` | Yu 2003 |
| `\citealt[12]{Yu2003}` | Yu 2003: 12|
| `\citeauthor{Yu2003}` | Yu |
| `\citeyear{Yu2003}` | 2003 |
| `\citetitle{Yu2003}` | *Morpology Africa* |

#### Et al.

When there are three or more authors, the citation will print the first author’s name and “et al.”.
Do not write “et al.” in a BibTeX entry. 

### Citation examples

`This is claimed to be true \citep{Yu2003,MalingZaenen1985}.`  
This is claimed to be true (Yu 2003, Maling & Zaenen 1985).

`See the claim by \citet[12]{Yu2003}.`  
See the claim by Yu (2003: 12).

`See the claim in \citet[12]{MalingZaenen1985}.`  
See the claim in Maling & Zaenen (1985: 12).

#### Complex parenthetical citations

Use `\cite{}` or `\citealt{}` to build a parenthetical citation remark that is anything more complex 
than a comma-separated list of citations.

`This is a claim (see \citealt{Erdal2007} and especially \citealt[12]{Yu2003}).`  
This is a claim (see Erdal 2007 and especially Yu 2003: 12).

#### Possessive citations

Use `\citegen{}`  to build a possessive citation like 
“Smith’s (2025) claim ...”.

`\citegen{Erdal2007} claim is true.`  
Erdal’s (2007) claim is true.

`\citegen{MalingZaenen1985} claim is true.`  
Maling & Zaenen’s (1985) claim is true.

`\citegen{JohnsonEtAl1989} claim is true.`  
Johnson et al.’s (1989) claim is true.

Use \citeapo{} if you only need the apostrophe, like in "Jones' (1990) claim"


### Page citations

Use the optional argument `[]` for the page citation, which is printed after the year after a colon. 
This only works properly for one citation at a time.

`See the claim by \citet[12]{Yu2003}.`  
See the claim by Yu (2003: 12).

\*`This is claimed to be true \citep[12, 34]{Yu2003,MalingZaenen1985}.`  
This is claimed to be true (Yu 2003, Maling & Zaenen 1985: 12, 34).

`This is claimed to be true (\citealt[12]{Yu2003}, \citealt[34]{MalingZaenen1985}).`  
This is claimed to be true (Yu 2003: 12, Maling & Zaenen 1985: 34).

Do not use the abbreviations `p.` or `pp.` or `ff.` or `f.` to specify page citations. 
Always use the exact page number or range.
A page range is encoded in LaTeX with two hyphens `--`, e.g. `12--14`, 
or a literal en dash `–` (U+2013), e.g. `12–14`. 
In a page range, do not truncate the second numeral for the end of the range, e.g. \*`12--4`. 

To cite a chapter, section, table or figure, use the full (capitalized) word, not an abbreviation.
Use the section symbol `§` as appropriate.

```
\citet[Chapter 2]{Smith2025}
*\citet[ch. 2]{Smith2025}
\citet[Section 2.1]{Smith2025}
\citet[§2.1]{Smith2025}
\citet[footnote 2]{Smith2025}
\citet[fn. 2]{Smith2025}
``` 
### Parentheses

Use `\citep{}` for a list of citations in parentheses, such as at the end of a sentence.

`This is claimed to be true \citep{Yu2003,MalingZaenen1985}.`  
This is claimed to be true (Yu 2003, Maling & Zaenen 1985).

Avoid `\citep{}` within parentheses unless there are several lines between opening and closing parenthesis. 
Instead, use `\citealt{}` to build a parenthetical remark.

`This is claimed to be true (see \citealt{Yu2003} and also \citealt{MalingZaenen1985}).`  
This is claimed to be true (see Yu 2003 and also Maling & Zaenen 1985).

`\citep{}` prints a comma-separated list of citations, in one pair of parentheses.
When building a long or complex list of citations in a parenthetical remark with `\citealt{}`, 
use the same separator (a comma) in the list, unless there is a reason to switch to a 
semicolon separator.

### Quotations

Use `\citep{}` after a long quotation in an quote environment:
...

### Linguistic examples

Use `\citealt{}`, not `\citep{}`, for an (optional) citation with the `\langinfo` command
in a linguistic example.

```
\ea
\langinfo{Mising}{Sino-Tibetan}{\citealt[69]{Prasad91a}}\\
\gll azɔ́në dɔ́luŋ\\
small village\\
\glt ‘a small village’
\z
```
<p><pre>
(1)	Mising (Sino-Tibetan; Prasad 1991: 69)  
	<i>azɔ́në	dɔ́luŋ</i>
	small	village
	‘a small village’
</pre></p>
 

### Common abbreviations

Some abbreviations are commonly used with in-text citations.
Pay attention to their meanings.
Do not use italics for Latin abbreviations commonly used in English.

| Abbreviation | Meaning |
| :--- | :--- |
| i.e. | that is |
| e.g. | for example |
| a.o. | among others |
| cf. | compare |

Avoid op. cit., loc. cit. and ibid. and repeat the full citation instead.

### Personal communication

You can cite personal communication, but do not use a BibTeX entry for this.
Write the correspondent’s full name, the cue phrase “personal communication” (or its 
abbreviation “pers. comm.” or “p.c.”), and the date.
This information can be given in an in-text parenthetical remark or a footnote.

```
(Sebastian Nordhoff, personal communication, December 25, 2024)
(Nordhoff, pers. comm., 2024)
(Nordhoff, p.c., 2024)
```

### Website citations

When citing a website by name in the text, print the website URL in a parenthetical remark 
(after the website name) or a footnote (at the end of the sentence). 
A BibTeX entry is not required to cite a website, especially if the website does not have a named
author.
If the website is a resource like a database or a corpus, use a `@misc` BibTeX entry to cite 
the resource.

### Citations to this volume

In a collected volume, it is common for one paper/chapter in the volume to cite another 
paper/chapter in the same volume. The LangSci skeleton autogenerates a bib file for this. This file
contains the keys `chapters/smith`, `chapters/jones` etc, and these can be cited via `\citet{chapters/smith} 
claims ...`. This will add "[this volume]" or "this volume" after the entry, depending on the command used.


## References

### Quick guide for references

Most works can be referenced with the `@article`, `@book`, `@incollection`, `@phdthesis`,
and `@misc` BibTeX entry types.

```
@article{Milewski1951,
	author = {Milewski, Tadeusz},
	journal = {Lingua Posnaniensis},
	pages = {248--268},
	title = {The conception of the word in languages of {North American} natives},
	volume = {3},
	year = {1951}
}
```
> Milewski, Tadeusz. 1951. The conception of the word in languages of North American natives. 
> *Lingua Posnaniensis* 3. 248–268.

```
@book{Lightfoot2002,
	address = {Oxford},
	editor = {Lightfoot, David W.},
	publisher = {Oxford University Press},
	title = {Syntactic effects of morphological change},
	year = {2002},
	doi = {10.1093/acprof:oso/9780199250691.001.0001},
}
```
> Lightfoot, David W. (ed.). 2002. *Syntactic effects of morphological change*. 
> Oxford: Oxford University Press. DOI: 
> [10.1093/acprof:oso/9780199250691.001.0001](https://doi.org/10.1093/acprof:oso/9780199250691.001.0001).

```
@incollection{Rissanen1999,
	address = {Cambridge},
	author = {Rissanen, Matti},
	maintitle = {The {Cambridge} history of the {English} language},
	booktitle = {1476--1776},
	editor = {Lass, Roger},
	pages = {187--331},
	publisher = {Cambridge University Press},
	title = {Syntax},
	volume = {3},
	year = {1999},
	doi = {10.1017/CHOL9780521264761.005},
}
```
> Rissanen, Matti. 1999. Syntax. In Roger Lass (ed.), 
> *The Cambridge history of the English language*. Vol. 3: *1476–1776*, 187–331. 
> Cambridge: Cambridge University Press. DOI: 
> [10.1017/CHOL9780521264761.005](https://doi.org/10.1017/CHOL9780521264761.005).

```
@phdthesis{Yu2003,
	address = {Berkeley},
	author = {Yu, Alan Chi Lun},
	school = {University of California},
	title = {The morphology and phonology of infixation},
	year = {2003},
	url = {https://escholarship.org/uc/item/4ds6q618},
}
```
> Yu, Alan Chi Lun. 2003. *The morphology and phonology of infixation*. 
> Berkeley: University of California. (Doctoral dissertation). 
> <https://escholarship.org/uc/item/4ds6q618>.

```
@misc{Filppula2013,
	author = {Filppula, Markku},
	howpublished = {Paper presented at the conference of the Societas Linguistica Europaea, Split, 18–21 September},
	title = {Areal and typological distributions of features as evidence for language contacts in {Western Europe},
	year = {2013}
}
```
> Filppula, Markku. 2013. 
> *Areal and typological distributions of features as evidence for language 
> contacts in Western Europe*. 
> Paper presented at the conference of the Societas Linguistica Europaea, Split, 18–21 September.

##  BibTeX entry types

The Language Science Press bibliography style supports the following major BibTeX entry types: 
`@article`, `@book`, `@incollection`, `@phdthesis`,`@mastersthesis`, `@thesis`, `@techreport`,  and
`@misc`.

Avoid `@manual`, `@online`, `@unpublished`, `@inproceedings`,  `@inbook`.
 
Do not use these legacy/deprecated BibTeX entry types: 
`@proceedings`, `@conference`, `@report`, and `@booklet`. 


### Article

Use the `@article` entry type for an article in a journal.
Some conference proceedings and working paper series are considered serialized journals by 
their publisher.
Do not use `@article` for an article-length unpublished manuscript or preprint, especially if 
there is no serialized journal.

```
@article{Lastname2025,
	author = {Lastname, Firstname},
	journal = {Journal Title in Title Case},
	pages = {123--145},
	title = {Article title in sentence case: {A} subtitle},
	volume = {56},
	number = {4},
	year = {2025},
	doi = {10.1234/1234567},
	url = {https://www.jstor.org/stable/12345678},
	note = {Some essential information in sentence case},
}
```

#### Article ID

If the article has an article ID instead of sequential pagination, then use the `pages` field 
for the article ID itself, without adding e.g. “Article ID” or “Paper number”. 
In this case, do not use the `pages` field to show the total number of pages in the article, 
e.g.,  `pages = {1--12}`.
```
pages = {9120},
* pages = {Article ID 9120},
```

#### Special issue

If the article is in a special issue, with an issue title and editors that are worth mentioning, 
then use the `note` field for this information.
The conventional format for special issue information is 
“Special issue: Title of special issue in sentence case. Alex Smith, Pat Jones & Sam Lee (eds.)”.
By using the `note` field, this information is displayed after the `volume` (and `number`) and 
before the `pages`.

If the article is in a special issue, with an issue title and editors that are worth mentioning, 
then use the fields `issuetitle` and `editor` for this information.
The `issuetitle` field is title-like, so use braces to protect any capitalization.
Contact Language Science Press to enable support for the `issuetitle` and `editor` fields for 
`@article`, because these are disabled by default.
(Add `\PassOptionsToPackage{issueandeditor=true}{biblatex}` to `langscibook.cls` before 
`\usepackage[...]{biblatex}`.)

```
@article{Andeson2003,
	author = {Anderson, Gregory D. S.},
	journal = {STUF - Language Typology and Universals},
	number = {1--2},
	pages = {12--39},
	title = {Yeniseic languages from a {Siberian} areal perspective},
	volume = {56},
	year = {2003},
	doi = {10.1524/stuf.2003.56.12.12},
	note = {Special issue: Studia Yeniseica: In honor of Heinrich Werner. Edward J. Vajda \& Gregory D. S. Anderson (eds.)},
}

@article{Andeson2003alt,
	author = {Anderson, Gregory D. S.},
	journal = {STUF - Language Typology and Universals},
	number = {1--2},
	pages = {12--39},
	title = {Yeniseic languages from a {Siberian} areal perspective},
	volume = {56},
	year = {2003},
	doi = {10.1524/stuf.2003.56.12.12},
	issuetitle = {{S}tudia {Y}eniseica: {I}n honor of {Heinrich Werner}}. 
	editor = {Vajda, Edward J. and Anderson, Gregory D. S.},
}

```
> Anderson, Gregory D. S. 2003. Yeniseic languages from a Siberian areal perspective. 
> *STUF - Language Typology and Universals* 56(1–2). 
> Special issue: Studia Yeniseica: In honor of Heinrich Werner. 
> Edward J. Vajda \& Gregory D. S. Anderson (eds.). 12–39. 
> DOI: [10.1524/stuf.2003.56.12.12](https://doi.org/10.1524/stuf.2003.56.12.12)
> 
> Anderson, Gregory D. S. 2003b. Yeniseic languages from a Siberian areal perspective. 
> *STUF - Language Typology and Universals* 56(1–2): 
> *Studia Yeniseica: In honor of Heinrich Werner*. 
> Edward J. Vajda & Gregory D. S. Anderson (eds.). 12–39. 
> DOI: [10.1524/stuf.2003.56.12.12](https://doi.org/10.1524/stuf.2003.56.12.12)

 

### Book

```
@book{Lastname2024,
	author = {Lastname, Firstname},
	title = {Book title in sentence case: {A} subtitle},
	volume = {3},
	edition = {2},
	series = {Series Title in Title Case},
	number = {12},
	publisher = {Publisher},
	address = {City},
	year = {2024},
	note = {Some essential information in sentence case},
}
@book{Lastname2023,
	editor = {Lastname, Firstname},
	maintitle = {Main title of multi-volume work},
	title = {Title of book in multi-volume work},
	volume = {3},
	publisher = {Publisher},
	address = {City},
	year = {2023},
}
```

A `@book` entry requires an `author` or `editor` field, but not both. 
The fields `title`, `year`, `publisher`, and `address` are required. 
Use the fields `edition`, `volume`, and `series` and `number` if needed.

For a book, do not use the `pages` field.
Do not use the `note` field for the ISBN or to show the total number of pages the book has.

#### Booklet

Do not use the `@booklet` BibTeX entry type.
Use `@book` or `@misc` instead.

#### Proceedings

Do not use the `@proceedings` BibTeX entry type.
Use `@book` instead.

### In collection

```
@incollection{incollection1,
	address = {City},
	author = {Author, Firstname},
	title = {Title of article/chapter in collection: {A} subtitle},
	booktitle = {Title of collection},
	editor = {Editor, Firstname},
	pages = {123--145},
	publisher = {Publisher},
	year = {2025},
	doi = {10.1234/1234567},
	note = {Some essential information in sentence case},	
}
@inproceedings{inproceedings1,
	author = {Author, Firstname},
	title = {Title of paper in proceedings: {A} subtitle},
	booktitle = {Title of proceedings},
	editor = {Editor, Firstname},
	pages = {123--145},
	publisher = {Publisher},
	year = {2025},
	note = {Some essential information in sentence case},	
}	
@inproceedings{inproceedings2,
	author = {Author, Firstname},
	title = {Title of paper in proceedings: {A} subtitle},
	year = {2025},
	booktitle = {Proceedings of {Linguistics Conference}, {B}erlin, {J}uly 1--4},
	doi = {10.1234/1234567},
}	
@inbook{inbook1,
	address = {City},
	author = {Contributor, Firstname},
	title = {Foreword or similar contribution},
	booktitle = {Title of book},
	bookauthor = {Bookauthor, Firstname},
	pages = {v--xii},
	publisher = {Publisher},
	year = {2025},
}
```

Use `@incollection` for an article/chapter in an edited book. Use this for proceedings, too.
Use `@inbook` for a part of a book, such as a foreword, written by a contributor different 
than the author of the book.
The fields `author`, `title`, and `pages` are required to identify the article/chapter/paper, 
and the fields `booktitle` and `year` are required to identify the book. 
With `@incollection`, the fields `editor`, `publisher`, and `address` for the book are 
required. 
For a proceedings paper, the fields `editor`, `publisher`, `address`, and 
`pages` should be given if available, and `publisher` and `address` can be interpreted as the 
organizer and location, respectively, of the conference. 
For a contribution in a book, use `bookauthor` to identify the author of the book, 
and `author` to identify the author of the contribution.

For these entry types, use the fields `edition`, `volume`, `series` and `number` as appropriate 
for the book.

#### Conference

Do not use the `@conference` entry type. 
The `@conference` entry type is deprecated, once intended for a conference contribution, 
and now a conference paper is better formatted as an `@incollection` entry.

### Theses

Use `@phdthesis`, `@mastersthesis`, and `@thesis` for a dissertation, thesis, or paper submitted 
to a school as a requirement for granting a degree.

See [Thesis type](#thesis-type), [School](#school), and [Address](#address).

```
@phdthesis{Ashby2016,
	author = {Ashby, Michael George},
	school = {University of Oxford},
	address = {Oxford},
	title = {Experimental phonetics in {Britain}, 1890--1940},
	year = {2016},
	url = {https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1},
}
```

> Ashby, Michael George. 2016. *Experimental phonetics in Britain, 1890–1940*. 
> Oxford: University of Oxford. (Doctoral dissertation).
> <https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1>.
 
 
  

#### Eprint

The Language Science Press bibliography style does not support the `eprint` and `eprinttype` 
fields for eprints, which other bibliography styles do support. 
Do not use the `eprinttype` field or its unsupported values
`arxiv`, `jstor`, `pubmed`, `hdl`, `googlebooks`, `lingbuzz`, or `roa`.
Instead, use the `url` field for the full URL of the eprint and the `note` field to describe the 
eprint.

```
@unpublished{Conrod2021unpublished,
	author = {Conrod, Kirby},
	year = {2021},
	note = {Preprint. lingbuzz/006452}
	title = {Variation in {English} gendered pronouns: {A}nalysis and recommendations for ethics in linguistics},
	urldate = {2021-08},
	url = {https://ling.auf.net/lingbuzz/006452},
}
@misc{Conrod2021misc,
	author = {Conrod, Kirby},
	year = {2021},
	note = {Preprint. lingbuzz/006452}
	title = {Variation in {English} gendered pronouns: {A}nalysis and recommendations for ethics in linguistics},
	urldate = {2021-08},
	url = {https://ling.auf.net/lingbuzz/006452},
}

* @unpublished{Conrod2021unsupported,
	author = {Conrod, Kirby},
	date = {2021-08},
	eprint = {006452},
	eprinttype = {lingbuzz},
	title = {Variation in {English} gendered pronouns: {A}nalysis and recommendations for ethics in linguistics},
}
```
> Conrod, Kirby. 2021. *Variation in English gendered pronouns: Analysis and recommendations for ethics in linguistics*.
> Preprint. lingbuzz/006452. <https://ling.auf.net/lingbuzz/006452> (August 2021).  
>
> Conrod, Kirby. 2021. Variation in English gendered pronouns: Analysis and recommendations for 
> ethics in linguistics. Preprint. lingbuzz/006452. 
> <https://ling.auf.net/lingbuzz/006452> (August 2021).  
>
> Conrod, Kirby. 2021. Variation in English gendered pronouns: Analysis and recommendations 
> for ethics in linguistics.  

### Miscellaneous

Use `@misc` for conference presentations (not in a proceedings volume), preprints, unpublished 
manuscripts, software, websites, and any anything else that is not better classified by 
another BibTeX entry type.

Note that the title of a `@misc` reference is formatted according to the Language Science Press 
style in italic like a book title, not in roman like an article title.

Use the `note` field, or the `howpublished` field, to describe the `@misc` reference.

Use the `organization` and `address` fields if the `@misc` reference has an identifiable 
organization, sponsor, institute or publisher with a location.
Do not use the `institute`, `publisher`, and `location` fields with `@misc`.

```
@misc{LGR2015,
	author = {Comrie, Bernard and Haspelmath, Martin and Bickel, Balthasar},
	organization = {{Max Planck Institute for Evolutionary Anthropology, Department of Linguistics} and {University of Leipzig, Department of Linguistics}},
	title = {{The Leipzig Glossing Rules}: {Conventions} for interlinear morpheme-by-morpheme glosses},
	url = {https://www.eva.mpg.de/lingua/resources/glossing-rules.php},
	address = {Leipzig},
	urldate = {2015-05-31},
	year = {2015},
}

@misc{Vaux2022,
	author = {Vaux, Bert},
	note = {Manuscript. lingbuzz/007166},
	title = {The {Armenian} dialect of {Salmast}},
	url = {https://lingbuzz.net/lingbuzz/007166},
	year = {2022},
}

````
> Comrie, Bernard, Martin Haspelmath & Balthasar Bickel. 2015. 
> *The Leipzig Glossing Rules: Conventions for interlinear morpheme-by-morpheme glosses*. 
> Leipzig: Max Planck Institute for Evolutionary Anthropology, Department of Linguistics & 
> University of Leipzig, Department of Linguistics. 
> <https://www.eva.mpg.de/lingua/resources/glossing-rules.php> (31 May, 2015).
>
> Vaux, Bert. 2022. *The Armenian dialect of Salmast*. Manuscript. lingbuzz/007166.
> <https://lingbuzz.net/lingbuzz/007166>.

#### Software

```
@misc{Kay2024,
	title = {{tidybayes}: {T}idy data and geoms for {Bayesian} models},
	author = {Kay, Matthew},
	year = {2024},
	note = {R package version 3.0.7},
	doi = {10.5281/zenodo.1308151},
}

@misc{Burkner2025,
	title = {{brms}: {Bayesian} regression models using `{Stan}'},
	author = {Bürkner, Paul-Christian},
	year = {2024},
	note = {R package version 2.23.0},
	doi = {10.32614/CRAN.package.brms},
}
@article{Burkner2021,
	title = {Bayesian item response modeling in {R} with {brms} and {Stan}},
	author = {Bürkner, Paul-Christian},
	journal = {Journal of Statistical Software},
	year = {2021},
	volume = {100},
	number = {5},
	pages = {1--54},
	doi = {10.18637/jss.v100.i05},
}
```
> Kay, Matthew. 2024. *tidybayes: Tidy data and geoms for Bayesian models*. 
> R package version 3.0.7. DOI: [10.5281/zenodo.1308151](https://doi.org/10.5281/zenodo.1308151).

## BibTeX fields

```
title booktitle maintitle subtitle author editor year edition series
journal volume number pages address publisher doi url urldate school
type note
```

### Names

In the BibTeX file, list each name in the form “Surname, Givenname”, or more
generally “prefix/particle Surname(s), suffix, Givenname(s)”. 
Separate names of different authors/editors with the word “and”.

```
author = {Van Valin, Jr., Robert D.},
author = {Chelliah, Shobhana L. and de Reuse, Willem J.},
```

A name with a prefix or particle (e.g. van, van der, Van, von, Da, de, De) should
include that prefix/particle in the surname in the BibTeX file, with the intended
capitalization, without extra braces or LaTeX spacing ties `~`. 
The Language Science Press bibliography style will correctly alphabetize such names.

A name suffix (e.g. Sr, Sr. Jr, Jr., III) can be given after the surname after a comma.
Such a suffixed name will be processed correctly by the Language Science Press bibliography style.

Give the full names of authors and editors as in the publication of the referenced work.
Do not initialize given names unless that is the person’s preference.
Some persons style their name with initials only, like R. M. W. Dixon, or with a first initial, 
like W. Tecumseh Fitch. Middle initials are common, like Michael T. Putnam.

Give names of all authors and editors.
Do not use “et al.” in the author or editor field.

For a group or institutional name, or a person’s name that cannot be inverted around a comma 
in the English bibliographic style, use a second pair of curly braces around the entire name.

A name in a second script can be given in parentheses, but take care to put it after the surname 
or given name in the BibTeX file so that it is displayed after the name in the displayed reference. 
You can control how the name appears in the text via `shortauthor={}`

Do not omit space between initials. 
Do not add LaTeX spacing commands such as `~` or `\` after a period.
 

```
author = {Pérez Hernández, Lorena and Ruiz de Mendoza, Francisco José},

author = {{R Core Team}},

author = {Dixon, R. M. W.},

author = {É. Kiss, Katalin},

editor = {van Riemsdijk, Henk},

editor = {Hamilton, Rev. William},

author = {Chen, Shu-chuan (陳淑娟)},
shortauthor = {Chen},

author = {{Ngũgĩ wa Thiong’o}},
``` 

### Title

Write the `title` of the reference in sentence case. Capitalize the first letter in
the title and the first letter in any subtitle (after punctuation like a semicolon, en dash, comma 
or period that separates the title into parts).
Proper nouns and intentionally capitalized words and letters must be protected
with curly braces `{...}` so that they are not decapitalized when compiled. 
Language Science Press provides a Bibtex normalizer that detects proper nouns and the like
and adds braces as necessary (<https://www.langsci-press-gug.org/doc2tex/normalizebib>). 
Decapitalization only applies to title-like fields –
`title`, `booktitle`, `maintitle`, `subtitle` – not other fields such as 
`author`, `journal`, `series`, `address`, `publisher`, `note`, `howpublished`, and `type`.
These title-like fields also automatically capitalize the first letter of the title.
If the title starts with a word styled in lowercase, then protect it from initial caaitalization 
with braces.
```
title = {Vocabulary in {Native American} languages: {Salish} words},
title = {Tone in {Y}ongning {N}a: {L}exical tones and morphotonology},
title = {{tidybayes}: {T}idy data and geoms for {Bayesian} models},
booktitle = {Proceedings of the 22nd {Amsterdam} Colloquium}},
booktitle = {The structure of phonological representations, {P}art {II}},
```

There is a preference to put braces around the full word for proper nouns, which are always capitalized 
like `A grammar of {Turkish}`, and to only capitalize the first letter where capitalization depends on context, 
like ``Syntax and morphology: {W}here the two meet`

### Year

The `year` is required for all references.

Use a range of years for a cited work when that is most appropriate.

As a numeral, the year value can be unbraced, but Language Science Press prefers braced field 
values.

Do not use a year with a month and day. Instead, use the `urldate` field.

```
year = {2025},
year = {1949--1950},
```

For an `@incollection` entry, the `year` field is the date of publication of the proceedings 
volume, which may not be the same as the date of the conference. 
Do not use the `year` field to specify the days of the conference; instead put the conference 
location and date in the `booktitle` if desired.

#### No date

If the reference has no known date of publication, but is published, then set `year = {n.d.},`. 
By doing this, the citation or reference is printed with “n.d.”, the preferred no-date cue 
in Language Science Press style.

```
\citep{Smithodate}

@book{Smithnodate,
	author = {Smith, Alex},
	title = {Title of book},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {n.d.},
}
```
> Smith (n.d.)
> 
> Smith, Alex. n.d. *Title of book*. Berlin: Language Science Press.

#### Original date of publication

Do not use the `origdate` field to provide a different date of publication.
The `origdate` value is not printed in the reference if the `year` is already set.
 

#### Publication status

Do not use any phrase such as “In press”, “Submitted”, “In review”, “Accepted”, “In prepration”, 
“Unpublished”, or “Forthcoming” as the value of the `year` field for an unpublished work.
Instead, leave the `year` field empty and set the `pubstate` field to  `forthcoming`. Do not use "in press" or any other value. 

\citep{Smithinreview}

@book{Smithinreview,
	author = {Smith, Alex},
	title = {Title of book},
	publisher = {Language Science Press},
	address = {Berlin},
	pubstate = {forthcoming},
} 

### Series and number

Use the `series` and `number` fields to show such information of a reference. 
Do not use the `volume` field for the series number. 

The `series` name is capitalized in title case (capitalize all lexical words) in English. 
Do not use braces to protect capitals in the `series` name; this is not necessary.
A non-English `series` name can be written with that language’s conventional capitalization 
and punctuation even with Latin script.

Do not use initials for series, but write down the full name of the series in Title Case.

Provide a `series` name without a `number` value if that is not known or set by the publisher, 
but do try to determine the `number`.
  

Avoid mentioning the series editor (*Reihenherausgeber*). 
Do not try to use the `serieseditor` field.

```
@book{Clyne1991,
	address = {Berlin},
	editor = {Clyne, Michael},
	publisher = {Mouton de Gruyter},
	series = {Contributions to the Sociology of Language},
	number = {62},
	title = {Pluricentric languages: {Different} norms in different nations},
	year = {1991},
	doi = {10.1515/9783110888140},
}
```

> Michael Clyne (ed.). 1991. *Pluricentric languages: Different norms in different nations*
> (Contributions to the Sociology of Language 62). Berlin: Mouton de Gruyter.
> DOI: [10.1515/9783110888140](https://doi.org/10.1515/9783110888140).

### Journal

The `journal` name is capitalized in Title Case (capitalize all lexical words) in English. 
Do not use braces to protect capitals in the `journal` name; this is not necessary. 
A non-English `journal` name can be written with that language’s conventional capitalization and 
punctuation even in Latin script.

### Volume and number

The journal `volume` and `number` are numerals, conventionally.
The `number` is the issue number within a `volume`.
The `volume` is an arabic numeral, conventionally, but some journals use capital roman numerals 
for the `volume`.
Joint volumes or issues are common. 
Use the journal’s style of punctuation mark, e.g. `&` or `/` or en dash `--`, for a joint 
`volume` or `number`.

If the journal does not organize itself into volumes and instead has sequentially numbered issues, 
often called numbers, maybe more than one per year or not every year, then use the `volume` field
for this numbering, even if the journal calls it a number. 
By using the `volume` field, this number will not be printed in parentheses in the reference.

For a `@journal` entry , use the `number` field only if the `volume` field is used first.

### Book volumes

#### Book in multi-volume collection

A book volume in a multi-volume collection is conventionally written as e.g.
“*Main title of multi-volume collection*. Vol. 3: *Title of volume in multi-volume collection*”.
Sometimes this is writen as e.g. “*Title of multi-volume collection: A subtitle*, vol. 4”.
Use the `volume` field to ensure that the volume cue, “Vol.” or “vol.”, is in roman, not italic, 
while the rest of the title is italic.
Use the `maintitle` field to separate the title into parts separated by the volume 
cue, “Vol. or “vol.”.
Here are BibTeX examples for a book volume in a multi-volume collection, avoiding 
“Vol.” or “vol.” in the `title` or `booktitle` field.

```
@book{Smith2000,
	editor = {Smith, Alex},
	maintitle = {Main title of multi-volume collection},
	title = {Title of volume in multi-volume collection},
	volume = {3},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {2000},
}
@book{Smith2001,
	editor = {Smith, Alex},
	title = {Title of multi-volume collection: {A} subtitle},
	volume = {4},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {2001},
}
@incollection{Jones2000,
	author = {Jones, Pat},
	title = {Title of chapter},
	pages = {12--34},
	editor = {Smith, Alex},
	maintitle = {Main title of multi-volume collection},
	booktitle = {Title of volume in multi-volume collection},
	volume = {3},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {2000},
}
@incollection{Jones2001,
	author = {Jones, Pat},
	title = {Title of chapter},
	pages = {12--34},
	editor = {Smith, Alex},
	booktitle = {Title of multi-volume collection: A subtitle},
	volume = {4},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {2001},
}
```
> Smith, Alex (ed.). 2000. *Main title of multi-volume collection*. Vol. 3: *Title of volume in multi-volume collection*. Berlin: Language Science Press.
>
> Smith, Alex (ed.). 2001. *Title of multi-volume collection: A subtitle*, vol. 4. 
Berlin: Language Science Press.
>
> Jones, Pat. 2000. Title of chapter. In Alex Smith (ed.), 
*Main title of multi-volume collection*. Vol. 3: *Title of volume in multi-volume collection*, 
12–34. Berlin: Language Science Press.
>
> Jones, Pat. 2001. Title of chapter. In Alex Smith (ed.), 
*Title of multi-volume collection: A subtitle*, vol. 4, 12–34. Berlin: Language Science Press.

### Multi-volume work

To indicate that cited book is a multi-volume work but only identify the (main) title, 
use the `note` field, e.g. `note = {4 volumes}`, so that this will be displayed in roman, 
not italic as part of the title itself.
```
@book{Smith2002,
	editor = {Smith, Alex},
	maintitle = {Main title of multi-volume collection},
	note = {4 volumes},
	publisher = {Language Science Press},
	address = {Berlin},
	year = {2002},
}
```
> Smith, Alex (ed.). 2002. *Main title of multi-volume collection*. 4 volumes. 
> Berlin: Language Science Press.

### Publisher

### School

Identify the degree-granting `school` for a `@phdthesis`, `@mastersthesis`, or `@thesis`.

If applicable, put the department after the school, e.g. 
`school = {Carnegie Mellon University, Laboratory for Computational Linguistics},` 

### Address

Use `address` for the city, without indication of state, province, or country.
If a publisher is associated with several cities, give only the first city.
 
Please provide some `address` for any BibTeX entry with a `publisher`  field, even if the city is already evident in that field.

```
publisher = {Mouton de Gruyter},
address = {Berlin},

publisher = {John Benjamins},
address = {Amsterdam},

publisher = {Oxford University Press},
address = {Oxford},
```

#### Location

Do not use the `location` field.
Use `address` instead. 
For a conference paper, (re)write the `booktitle` field to include the conference venue (and dates),
or use the `address` field for the conference venue.

The Association for Computational Linguistics (ACL) and the European Language Resources 
Association (ELRA) use the `address` field for the conference location.

```
* @inproceedings{borstell-2022-introducing,
    title = "Introducing the signgloss{R} Package",
    author = {B{\"o}rstell, Carl},
    editor = "Efthimiou, Eleni  and
      Fotinea, Stavroula-Evita  and
      Hanke, Thomas  and
      Hochgesang, Julie A.  and
      Kristoffersen, Jette  and
      Mesch, Johanna  and
      Schulder, Marc",
    booktitle = "Proceedings of the LREC2022 10th Workshop on the Representation and Processing of Sign Languages: Multilingual Sign Language Resources",
    month = jun,
    year = "2022",
    address = "Marseille, France",
    publisher = "European Language Resources Association",
    url = "https://aclanthology.org/2022.signlang-1.3/",
    pages = "16--23",
    abstract = "The signglossR package is a library written in the programming language R, intended as an easy-to-use resource for those who work with signed language data and are familiar with R. The package contains a variety of functions designed specifically towards signed language research, facilitating a single-pipeline workflow with R when accessing public language resources remotely (online) or a user{'}s own files and data. The package specifically targets processing of image and video files, but also features some interaction with software commonly used by researchers working on signed language and gesture, such as ELAN and OpenPose. The signglossR package combines features and functionality from many other libraries and tools in order to simplify and collect existing resources in one place, as well as adding some new functionality, and adapt everything to the needs of researchers working with visual language data. In this paper, the main features of this package are introduced."
}

@inproceedings{borstell-2022-langsci,
	title = {Introducing the signgloss{R} package},
	author = {Börstell, Carl},
	editor = {Efthimiou, Eleni and Fotinea, Stavroula-Evita and Hanke, Thomas and Hochgesang, Julie A. and Kristoffersen, Jette and Mesch, Johanna and Schulder, Marc},
	booktitle = {Proceedings of the {LREC2022 10th Workshop on the Representation and Processing of Sign Languages}: {M}ultilingual Sign Language Resources, {M}arseille, {F}rance, 20-25 {J}une},
	year = {2022},
	address = {Paris},
	publisher = {European Language Resources Association},
	url = {https://aclanthology.org/2022.signlang-1.3/},
	pages = {16--23},
	series = {SingLang},
}
```
> \*Börstell, Carl. 2022. Introducing the signglossR package. In Eleni Efthimiou, Stavroula-Evita 
> Fotinea, Thomas Hanke, Julie A. Hochgesang, Jette Kristoffersen, Johanna Mesch & Marc Schulder 
> (eds.), *Proceedings of the lrec2022 10th workshop on the representation and processing of sign languages: Multilingual sign language resources*, 
> 16–23. Marseille, France: European Language Resources Association. 
> <https://aclanthology.org/2022.signlang-1.3/>.
>
> Börstell, Carl. 2022. Introducing the signglossR package. In Eleni Efthimiou, Stavroula-Evita 
> Fotinea, Thomas Hanke, Julie A. Hochgesang, Jette Kristoffersen, Johanna Mesch & Marc Schulder 
> (eds.), *Proceedings of the LREC2022 10th Workshop on the Representation and Processing of Sign Languages:  Multilingual sign language resources, Marseille, France, 20-25 June* (SingLang), 
> 16–23. Paris: European Language Resources Association. 
> <https://aclanthology.org/2022.signlang-1.3/>.

### Edition

To provide the edition number for a book, set `edition` to a numeral. 
Or provide more information as text.
If the `edition` value is a numeral, e.g. `edition = {2},`, then an ordinal version of that number 
is printed in the reference with the cue “edn.”, e.g. “2nd edn.”.
If the `edition` value is any other text, then that text is printed in the reference after the 
title.

Do not use the `title`, `booktitle`, or `note` fields for edition information.

```
@book{Croft2023,
	address = {Cambridge},
	author = {Croft, William},
	edition = {2},
	series = {Cambridge Textbooks in Linguistics},
	publisher = {Cambridge University Press},
	title = {Typology and universals},
	year = {2003},
	doi = {10.1017/CBO9780511840579},
}
@book{Ong2012,
	address = {New York},
	author = {Ong, Walter J.},
	edition = {30th anniversary edition},
	publisher = {Routledge},
	title = {Orality and literacy: {T}he technologizing of the word},
	year = {2012}
}
```
> William Croft. 2003. *Typology and universals*. 2nd edn. (Cambridge Textbooks
> in Linguistics). Cambridge: Cambridge University Press. DOI: 
> [10.1017/CBO9780511840579](https://doi.org/10.1017/CBO9780511840579).
> 
> Walter J. Ong. 2012. *Orality and literacy: The technologizing of the word*. 
> 30th anniversary edition. New York: Routledge.

### DOI

Provide a DOI in the `doi` field whenever a DOI is available for the referenced work.
Provide only the DOI itself, e.g. `10.0001/1234567`, not an address like 
`https://doi.org/10.0001/1234567`.

```
doi = {10.0001/1234567},
* doi = {doi: 10.0001/1234567},
* doi = {https://doi.org/10.0001/1234567},
* doi = {https://dx.doi.org/10.0001/1234567},
```

Use the `url` feld for a handle, even though the doi resolver sometimes works with a handle.
```
url = {http://hdl.handle.net/10045/53587},
* doi = {10045/53587}
```

### URL and urldate

Provide an URL in the `url` field when the referenced work is available at that URL address.
A DOI is strongly preferred over an URL; do not provide an URL if a DOI is available.
Use a complete URL, with the prefix `https://` or `http://`, not just a domain.

Provide an `urldate`  for all URLs.

For any `urldate`, use the numeric format `yyyy-mm-dd`, e.g. `urldate = {2024-12-25}` 
in the BibTeX entry. 
In the reference list, the `urldate` is displayed by the Language Science Press bibliography style 
as e.g. “(25 December, 2024)” at the end of the reference.

Do not use the `note` field to provide information that could be provided in the 
`url` and `uldate` fields.
 
Please trim the `url` value to its clean, stable form. 
Remove any inessential parts after  `?`, `&`, or `#` such as search terms, tracking codes, 
or text highlights.

### Type

The `type` field is used with thesis entries (`@thesis`, `@phdthesis` or `@mastersthesis`) 
or a `@techreport` entry to specify or override the default label or cue to describe the 
type of work it is within that entry.

#### Thesis type

Use the `type` field to specify a custom thesis type with `@thesis`, or with `@phdthesis` or `@mastersthesis` to override the default thesis cue.
This is useful for theses and dissertations from non-U.S. schools, as well as 
undergraduate theses and papers.
Do not qualify a thesis or dissertation as “unpublished” just because it is not publicly 
archived or indexed (this is APA style).
```
type = {Doktorarbeit},
type = {Dissertação de doutorado},
type = {Mémoire de maîtrise},
type = {BA thesis},
```

```
@thesis{Ashby2016,
	author = {Ashby, Michael George},
	school = {University of Oxford},
	address = {Oxford},
	title = {Experimental phonetics in {Britain}, 1890--1940},
	year = {2016},
	type = {DPhil thesis},
	url = {https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1},
}
```
> Ashby, Michael George. 2016. *Experimental phonetics in Britain, 1890–1940*. 
> Oxford, University of Oxford. (DPhil thesis).
> <https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1>.

Without specifying a `type` of thesis, the default cues are 
“Doctoral dissertation” for `@phdthesis` and “MA thesis” for `@mastersthesis`.

```
@phdthesis{Ashby2016,
	author = {Ashby, Michael George},
	school = {University of Oxford},
	address = {Oxford},
	title = {Experimental phonetics in {Britain}, 1890--1940},
	year = {2016},
	url = {https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1},
}
@mastersthesis,{Smith2007,
	author = {Smith, Rebecca Dow},
	title = {The noun class system of {U̱t-Ma'in}: {A} {West Kainji} language of {Nigeria}},
	address = {Grand Forks},
	school = {University of North Dakota},
	year = {2007},
	url = {https://commons.und.edu/theses/4476/},
```

> Ashby, Michael George. 2016. *Experimental phonetics in Britain, 1890–1940*. 
> Oxford: University of Oxford. (Doctoral dissertation).
> <https://ora.ox.ac.uk/objects/uuid:d8bbffae-8a4e-478e-ba65-0f5a5bbd66e1>.
>
> Smith, Rebecca Dow. 2007. *The noun class system of U̱t-Ma’in: A West Kainji language of Nigeria*. 
> Grand Forks: University of North Dakota. (MA thesis). 
> <https://commons.und.edu/theses/4476/>.


#### Technical report type

Use the `type` field to specify a custom type of a `@techreport` entry, to override the 
default “Tech. rep.”.

## Sample BibTeX file

```
%Encoding: utf-8

@article{MalingZaenen1985,
	author = {Maling, Joan and Zaenen, Annie},
	year = {1985},
	title = {Preposition-stranding and passive},
	journal = {Nordic Journal of Linguistics},
	volume = {8},
	number = {2},
	pages = {197--209},
	doi = {10.1017/S0332586500001335},
}

@phdthesis{Yu2003,
	address = {Berkeley},
	author = {Yu, Alan Chi Lun},
	school = {University of California},
	title = {The morphology and phonology of infixation},
	shorttitle = {Morpology Africa},
	year = {2003},
	url = {https://escholarship.org/uc/item/4ds6q618},
}
...	
```
