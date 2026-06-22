LATEX := lualatex

name := mscs-2025
in := $(name).tex
out := $(name).pdf
aux_exts := aux log nav out snm toc

.PHONY: all clean aux-clean

all: $(out)

$(out): $(in)
	$(LATEX) "$(in)"
	$(LATEX) "$(in)"
	@$(MAKE) aux-clean

clean:
	@$(MAKE) aux-clean
	@rm -f "$(out)"

aux-clean:
	@for ext in $(aux_exts); do rm -f "$(name).$${ext}"; done
