LATEX := pdflatex

names := cv cv_short
outs := $(addsuffix .pdf,$(names))
aux_exts := aux log out

.PHONY: all clean aux-clean

all: $(outs)

%.pdf: %.tex
	$(LATEX) "$<"
	$(LATEX) "$<"
	@$(MAKE) aux-clean

clean:
	@$(MAKE) aux-clean
	@rm -f $(outs)

aux-clean:
	@for name in $(names); do for ext in $(aux_exts); do rm -f "$${name}.$${ext}"; done; done
