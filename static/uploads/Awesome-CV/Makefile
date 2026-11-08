.PHONY: resume check clean distclean

EXAMPLES_DIR = examples
RESUME = Leo_Aparisi_de_Lannoy_resume

# latexmk tracks dependencies itself; examples/latexmkrc selects LuaLaTeX
resume:
	cd $(EXAMPLES_DIR) && latexmk $(RESUME).tex

# Fail unless the resume is one page and passes veraPDF's PDF/UA-2 profile
check: resume
	@pages=$$(pdfinfo $(EXAMPLES_DIR)/$(RESUME).pdf | awk '/^Pages:/ {print $$2}'); \
	test "$$pages" = 1 || { echo "Resume is $$pages pages, expected 1"; exit 1; }
	verapdf -f ua2 --format text $(EXAMPLES_DIR)/$(RESUME).pdf | grep -q '^PASS' \
		|| { echo "veraPDF PDF/UA-2 validation failed"; exit 1; }
	@echo "OK: 1 page, PDF/UA-2 compliant"

# Remove auxiliary files, keep the PDF (it is published on the website)
clean:
	cd $(EXAMPLES_DIR) && latexmk -c $(RESUME).tex

# Remove auxiliary files and the PDF
distclean:
	cd $(EXAMPLES_DIR) && latexmk -C $(RESUME).tex
