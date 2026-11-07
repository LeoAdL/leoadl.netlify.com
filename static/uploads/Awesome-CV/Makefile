.PHONY: resume clean distclean

EXAMPLES_DIR = examples
RESUME = Leo_Aparisi_de_Lannoy_resume

# latexmk tracks dependencies itself; examples/latexmkrc selects LuaLaTeX
resume:
	cd $(EXAMPLES_DIR) && latexmk $(RESUME).tex

# Remove auxiliary files, keep the PDF (it is published on the website)
clean:
	cd $(EXAMPLES_DIR) && latexmk -c $(RESUME).tex

# Remove auxiliary files and the PDF
distclean:
	cd $(EXAMPLES_DIR) && latexmk -C $(RESUME).tex
