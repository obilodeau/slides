# Makefile for asciidoc based presentation
# Olivier Bilodeau <bilodeau@eset.com>

MAIN_DOCUMENT=derbycon
ASCIIDOCTOR_BACKENDS=/home/olivier/src/asciidoctor-backends/slim/revealjs

default: $(MAIN_DOCUMENT).html

$(MAIN_DOCUMENT).html: *.ad 
	asciidoctor -T $(ASCIIDOCTOR_BACKENDS) -b revealjs $(MAIN_DOCUMENT).ad

open: $(MAIN_DOCUMENT).html
	"$(shell which xdg-open || which open || which x-www-browser)" $(MAIN_DOCUMENT).html
	
clean:
	rm -f *.html

serve:
	"$(shell which xdg-open || which open || which x-www-browser)" \
		http://localhost:8000/$(MAIN_DOCUMENT).html
	python -m SimpleHTTPServer 8000
