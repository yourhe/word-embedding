# Word Embedding in Golang

[![Build Status](https://travis-ci.org/ynqa/word-embedding.svg?branch=master)](https://travis-ci.org/ynqa/word-embedding)
[![GoDoc](https://godoc.org/github.com/ynqa/word-embedding?status.svg)](https://godoc.org/github.com/ynqa/word-embedding)
[![Go Report Card](https://goreportcard.com/badge/github.com/ynqa/word-embedding)](https://goreportcard.com/report/github.com/ynqa/word-embedding)

This is the implementation of word embedding (a.k.a word representation) models in Golang.

## Word Embedding

Word embedding makes word's meaning, structure, and concept mapping into vector space with low dimension. For representative instance:

```
Vector("King") - Vector("Man") + Vector("Woman") = Vector("Queen")
```

Like this example, the models generate the vectors that could calculate word meaning by arithmetic operations for other vectors.

## Models
- [x] Word2Vec
  - Distributed Representations of Words and Phrases
and their Compositionality [[pdf]](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)
- [x] GloVe
  - GloVe: Global Vectors for Word Representation [[pdf]](http://nlp.stanford.edu/pubs/glove.pdf)

and more...

## Installation

```
$ go get -u github.com/ynqa/word-embedding
$ bin/word-embedding -h
```

## Usage

```
tools for embedding words into vector space

Usage:
  word-embedding [flags]
  word-embedding [command]

Available Commands:
  distance    Estimate the distance between words
  glove       GloVe: Global Vectors for Word Representation
  help        Help about any command
  word2vec    Word2Vec: Continuous Bag-of-Words and Skip-gram model

Flags:
  -h, --help   help for word-embedding

Use "word-embedding [command] --help" for more information about a command.
```

For more information about each sub-command, see below:
- [distance](./distance/README.md)
- [word2vec](./model/README.md)
  - In code-based, refer to the [example](./example/example.go).
- [glove](./model/README.md)

## Demo

Downloading [text8](http://mattmahoney.net/dc/textdata) corpus, and training by Skip-Gram with negative sampling.

```
$ sh demo.sh
```

## Output
Output a file is subject to the following format:

```
<word> <value1> <value2> ...
```

## References
- Just see it for more deep comprehension:
  - Improving Distributional Similarity
with Lessons Learned from Word Embeddings [[pdf]](http://www.aclweb.org/anthology/Q15-1016)
  - Don’t count, predict! A systematic comparison of
context-counting vs. context-predicting semantic vectors [[pdf]](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.648.8023&rep=rep1&type=pdf)
