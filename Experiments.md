# System 1: stroll (graph based SRL)
The code can be found in [this repository](https://github.com/Filter-Bubble/stroll).
The labeler takes conll as input, using the features UPOS and DEPREL.

## Model 1: trained on UPOS
Trained on `gold-conllu/sonar1_train.conll`

evaluate in two ways:
 - on golden pos/deprel data (`gold-conllu`).
 - on stanfordnlp output (`stanfordnlp-conllu`).
 
## Model 2: trained on Alpino tags??
Maybe not necessary

# System 2: vua-srl
The code can be found in [this repository](https://github.com/sarnoult/vua-srl-nl) (note that this an updated fork to use python 3). It takes NAF as input, using features from the term, constituent and dependency layers (as produced by Alpino). It includes a trained model, but it's unclear on what data this model is trained.

As the system outputs NAF, we need to convert it to conll in order to evaluate.

## Model 1: the existing model 
It needs the features coming out of Alpino, so we evaluate it with the data in `alpino-naf`.

## Model 2: retrain
Train and evaluate on the output of Alpino (`alpino-naf`). We cannot train on golden data, as we don't have the golden constituents??

# System 3: BERTje
TODO: wait for the code and models released from the RUG. As it is an end-to-end system, we can train and evaluate simply on the gold conllu files.


```python

```
