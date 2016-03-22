CACHE_DIR   := $(shell pwd)/.latex-cache
COMPILE_TEX := pdflatex -output-directory=$(CACHE_DIR)
PACKAGE_SRC := $(wildcard *.tex)

all:
	$(foreach var,$(PACKAGE_SRC),$(COMPILE_TEX) $(var);)
	@mv $(CACHE_DIR)/*.pdf .

$(CACHE_DIR):
	@mkdir -p $(CACHE_DIR)

clean-cache:
	@rm -f $(CACHE_DIR)/*
	@rm -f *.log *.aux

clean: clean-cache

