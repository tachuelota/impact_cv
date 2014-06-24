# ImpactStory curriculum

Web version available here: [www.guillaumelobet.be/impact](http://www.guillaumelobet.be/impact)

## Overview

The aim of the porject is to automaticlly generate a curriculum using LaTeX and the information contained on an ImpactStory profile (altmetrics).

## Web version

The web version is composed of 3 php scripts to convert the ImpactStory profile to one of these formats:

- BibTex
- PDF
- Markdown
- HTML

Web version available here: [www.guillaumelobet.be/impact](http://www.guillaumelobet.be/impact)


## LaTeX version

for the LaTeX afficionados.

So far, there are three main files to generate the curriculum:

- Perl
	- parse_impactstory_bib.pl
- LaTeX
	- friggeri-cv.cls
	- curriculum.tex
	
To generate the curriculum, run the Perl file, then run the LaTeX one.


### Perl script

To run the Perl file, you need to installt he following packages:

- JSON qw( decode_json )
- IO::All
- Try::Tiny
- XML::Simple

To install them, run in the terminal:

	cpan JSON qw( decode_json )
	cpan IO::All
	cpan Try::Tiny
	cpan XML::Simple
	
Before running the Perl file, do not forget to edit you profile link (line 17). 

The Perl script create a bib file (impactbib.bib), used by LaTeX to generate the CV.


### LaTeX script

The LaTeX script is based on the CV template from Adrien Friggeri (adrien@friggeri.net), https://github.com/afriggeri/CV.

You need to used XeLaTeX and biber to make it run smoothly.

## Disclaimer

This is only the second time I use Perl. So the code is certainly unefficient, badly written and full of mistakes. But it works. So feel free to improve it!


