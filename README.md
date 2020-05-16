# Code for "Word Embeddings as Tuples of Feature Probabilities"

### Authors

Siddharth Bhat, Alok Debnath, Souvik Bannerjee, and Manish
Shrivastava

Kohli Center on Intelligent Systems,
International Institute of Information Technology, Hyderabad

{siddharth.bhat, alok.debnath, souvik.bannerjee}@research.iiit.ac.in

m.shrivastava@iiit.ac.in

## Requirements

Please download the `text8` corpus for creating word embeddings if you
would like to use those made using the `word2vec` source code. You can
also use other pretrained word embeddings for this task.

To replicate similarity measurements, please use the `SimLex-999` corpus.

## Instructions

```
cd word2vec
make all
./word2vec -train <input file name> -output <output file name> -size 200 -window 5 -sample 1e-4 -negative 5 -hs 0 -binary 0 -cbow 1 -iter 3
```

To perform analogy, simply change the model path name in `1-eval.sh` and
run it as `./1-eval.sh`

To perform similarity, simply change the model path name and simlex corpus
path name in `1-paper-numbers.sh` and run it as `./1-eval.sh`

To use the command line interface for fuzzy embeddings, run:
```
make cli
./cli
```
and follow the instructions.
