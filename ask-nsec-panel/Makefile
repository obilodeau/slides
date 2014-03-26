#
# Makefile to serve more as self-serving documentation than anything else
#

default: cuecards slides

cuecards: ask-nsec-panel.html

ask-nsec-panel.html: ask-nsec-panel.adoc
	asciidoc -b cuecards ask-nsec-panel.adoc

slides: ask-nsec-slides.html

ask-nsec-slides.html: ask-nsec-slides.adoc
	asciidoc ask-nsec-slides.adoc

prepare:
	asciidoc --backend build cuecards.zip cuecards/
	asciidoc --backend install cuecards.zip

clean:
	asciidoc --backend remove cuecards
	rm -f *.html

