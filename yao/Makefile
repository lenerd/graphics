IMG = \
	real_ideal_model.pdf \
	millionaires_ideal.pdf \
	millionaires_smpc.pdf \
	smpc.pdf

IMG_PROTO = \
	oblivious_transfer.pdf \
	oblivious_transfer_rsa.pdf


IMG_GARBLE = \
	yao_half_adder_garble.pdf \
	yao_half_adder_eval.pdf \
	yao_and_garble.pdf \
	yao_and_eval.pdf

KEY_LOCK_IMG=Key-gold.pdf Key-black.pdf Key-white.pdf Key-black-white.pdf \
		 Lock-gold.pdf Lock-black.pdf Lock-white.pdf

.phony: all clean

all: $(IMG) $(IMG_GARBLE) ${IMG_PROTO}

key_lock: $(KEY_LOCK_IMG)

$(IMG_GARBLE): %.pdf: %.tex key_lock
	latexmk -pdf $<
	pdfcrop --margins "-1 -1 -1 -1" $@ $@

$(IMG_PROTO): %.pdf: %.tex
	latexmk -pdf $<

%.pdf: %.tex
	latexmk -pdf $^
	pdfcrop --margins "-1 -1 -1 -1" $@ $@

%.pdf: %.svg
	inkscape -A $@ $^

clean:
	latexmk -C
	rm -f *.nav *.snm *.log *.pdf
