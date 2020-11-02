## Train a model for task-oriented dialog datasets
We created `myTrain.py` to train models. You can run:
GLMP bAbI dialogue t1-5:
```console
❱❱❱ python3 myTrain.py -lr=0.001 -l=1 -hdd=128 -dr=0.2 -dec=GLMP -bsz=8 -ds=babi -t=1 
```
or GLMP SMD
```console
❱❱❱ python3 myTrain.py -lr=0.001 -l=1 -hdd=128 -dr=0.2 -dec=GLMP -bsz=8 -ds=kvr
```

While training, the model with the best validation is saved. If you want to reuse a model add `-path=path_name_model` to the function call. The model is evaluated by using per responce accuracy, WER, F1 and BLEU.

## Test a model for task-oriented dialog datasets
We created  `myTest.py` to train models. You can run:
GLMP bAbI t1-5:
```console
❱❱❱ python myTest.py -ds=babi -path=<path_to_saved_model> 
```
or GLMP SMD 
```console
❱❱❱ python myTest.py -ds=kvr -path=<path_to_saved_model> -rec=1
```

## Visualization Memory Access
Memory attention visualization in the SMD navigation domain. Left column is the global memory pointer G, middle column is the memory pointer without global weighting, and the right column is the final memory pointer.

<p align="center">
<img src="img/VIZ.png" width="100%" />
</p>

## Architecture
<p align="center">
<img src="img/new_enc.png" width="40%" />
<img src="img/new_dec.png" width="50%" />
</p>

## Enjoy! :)
