CACHE_DIR   := $(shell pwd)/.latex-cache
COMPILE_TEX := pdflatex -output-directory=$(CACHE_DIR)
PACKAGE_SRC := $(wildcard *.tex)

all:
	@mkdir -p $(CACHE_DIR)
	$(foreach var,$(PACKAGE_SRC),$(COMPILE_TEX) $(var);)
	@mv $(CACHE_DIR)/*.pdf .

clean-cache:
	@rm -f $(CACHE_DIR)/*
	@rm -f *.log *.aux

clean: clean-cache

