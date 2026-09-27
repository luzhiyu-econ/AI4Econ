# How to use this book

AI can help turn unstructured material into research data. The useful output is a documented measurement process, not a polished answer from a model.

This edition follows one example: identify whether a policy sentence contains a concrete fiscal support commitment. Work through the chapters in order, then replace the example with your own question.

## Before you begin

You need a small collection of source documents, stable document IDs, and permission to use those documents with your chosen tools. Keep the original text and the source location for every excerpt.

Make a hand-reviewed sample before running a model on the full corpus. Include ordinary cases, borderline cases, and examples that should be excluded. The sample is your reference for both prompt design and evaluation.

## Reading path

1. [Define the task](chapters/01-define-task.md): decide what one row means and what counts as a positive case.
2. [Build an annotation protocol](chapters/02-annotation.md): specify labels, evidence, and review rules.
3. [Evaluate the output](chapters/03-evaluation.md): test the protocol on data it did not see during development.
4. [Use AI evidence in an economics paper](chapters/04-inference.md): connect the measured variable to a defensible estimand.

## Working rule

Keep five things together: source text, source ID, protocol version, model response, and review decision. If any one is missing, later readers may be unable to reproduce a label or understand a disagreement.
