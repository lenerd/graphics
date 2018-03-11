IMG = \
  	universal_circuit.pdf \
	private_function_evaluation.pdf \
	timeline.pdf \
	edge-embedding.pdf \
	edge-universal_graph.pdf \
	graph_half_adder_embedding.pdf \
	graph_other_embedding.pdf \
	half_adder.pdf \
	towards_universal_circuit.pdf \
	2-way_4-way_construction.tex \
	embedding_algorithm.pdf \
	hybrid_construction.pdf \
	pfe_toolchain.pdf

.phony: all clean

all: $(IMG)

%.pdf: %.tex
	latexmk -pdf $^
	pdfcrop --margins "-1 -1 -1 -1" $@ $@

clean:
	latexmk -C
	rm -f *.nav *.snm *.log *.bbl *.run.xml *.pdf
