# Towards Integrated AI-Assisted Legal Reasoning

This repository contains the LaTeX source code for a comprehensive survey paper: **"Towards Integrated AI-Assisted Legal Reasoning: A Survey of Indian Legal NLP Across Five Capability Axes."** 

The paper is formatted as an IEEE two-column conference paper and reviews the state of Indian Legal AI across five key dimensions:
1. Precedent Search
2. Case Fact Structuring
3. Argument Graph Construction
4. Judicial Outcome Simulation
5. What-If Analysis

## Project Structure

The paper is modularised into five separate "bundles" to manage the content more effectively:
- `bundle1.tex`: Title block, Abstract, Introduction, and Background.
- `bundle2.tex`: Precedent Search, Case Fact Structuring, and Argument Graph Construction.
- `bundle3.tex`: Judicial Outcome Simulation and What-If Analysis.
- `bundle4.tex`: Datasets and Evaluation Metrics.
- `bundle5.tex`: Gaps and Contribution, Ethical Considerations, and Bibliography setup.
- `survey_references.bib`: The BibTeX database containing all citations.

## How to Build the PDF

To compile the modular bundles into the final complete PDF (`survey_main.pdf`), run the following commands in your terminal from this directory:

```bash
# 1. Combine all bundles into a single main file
cat bundle1.tex bundle2.tex bundle3.tex bundle4.tex bundle5.tex > survey_main.tex

# 2. Run pdflatex (first pass to generate auxiliary files)
pdflatex survey_main.tex

# 3. Run BibTeX (to process citations - do not add the .tex extension)
bibtex survey_main

# 4. Run pdflatex (second pass to insert bibliography)
pdflatex survey_main.tex

# 5. Run pdflatex (third pass to resolve all cross-references)
pdflatex survey_main.tex
```

After running these commands, the compiled, print-ready document will be available as `survey_main.pdf`.
