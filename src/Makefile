PKG =  GPlotFun

$(PKG).gfn: $(PKG).inp $(PKG).spec $(PKG)_sample.inp
	gretlcli --makepkg $(PKG).inp

#$(PKG).pdf: $(PKG).tex
#	pdflatex $<
#	bibtex $(PKG)
#	pdflatex $<
#	pdflatex $<

$(PKG).zip: $(PKG).gfn $(PKG).pdf
	echo makepkg $(PKG).zip | gretlcli -b -

# Only if the manual is a pdf file or you provide an external dataset
install: $(PKG).zip
	echo pkg install $(PKG).zip --local | gretlcli -b -

# Only for zip-file
clean:
	rm -f $(PKG).zip $(PKG).gfn
