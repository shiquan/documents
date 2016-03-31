CACHE_DIR   := $(shell pwd)/.latex-cache
COMPILE_TEX := xelatex -output-directory=$(CACHE_DIR)
PACKAGE_SRC = $(wildcard *.tex)  

all: $(CACHE_DIR)
	$(COMPILE_TEX) $(PACKAGE_SRC)
	@mv $(CACHE_DIR)/*.pdf .

$(CACHE_DIR):
	@mkdir -p $(CACHE_DIR)

clean-cache:
	@rm -f $(CACHE_DIR)/*
	@rm -f *.log *.aux *.nav *.snm *.out

clean: clean-cache

