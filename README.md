# 1. Introduction

Scripts to compute ToxHabits evaluation metrics.

Written in Python 3.7


# 2. Requirements

Python version: ```Python 3.7```

To install Requirements: 
```
pip install -r requirements.txt
```


# 3. Execution

```
cd src  
python main.py -g ..\ground_truth\gs.tsv -p ..\dummy_submission\test_submission.tsv -s ner
```


# 4. Other interesting stuff:

### Metrics

The evaluation metrics are precision, recall and f1-score. The latter will be used to decide the award winners.

### Script Arguments
+ ```-g/--gs_path```: path to Gold Standard TSV file with the annotations
+ ```-p/--pred_path```: path to predictions TSV file with the annotations
+ ```-c/--valid_codes_path```: path to TSV file with valid codes (provided here).
+ ```-s/--subtask```: subtask name (```ner```).

### Examples: 

```
$ cd src
$ python main.py -g ..\ground_truth\gs.tsv -p ..\dummy_submission\test_submission.tsv -s ner


-----------------------------------------------------
Clinical case name                      Precision
-----------------------------------------------------
es-S0210-48062010000100019-3            1.0
-----------------------------------------------------
es-S0210-56912007000900007-3            1.0
-----------------------------------------------------

-----------------------------------------------------
Clinical case name                      Recall
-----------------------------------------------------
es-S0210-48062010000100019-3            1.0
-----------------------------------------------------
es-S0210-56912007000900007-3            1.0
-----------------------------------------------------

-----------------------------------------------------
Clinical case name                      F-score
-----------------------------------------------------
es-S0210-48062010000100019-3            1.0
-----------------------------------------------------
es-S0210-56912007000900007-3            1.0
-----------------------------------------------------

-----------------------------------------------------
Micro-average metrics
-----------------------------------------------------

Micro-average precision = 1.0


Micro-average recall = 1.0


Micro-average F-score = 1.0

```


### Citation
Please, cite us: 

Miranda-Escalada, A., Gascó, L., Lima-López, S., Farré-Maduell, E., Estrada, D., Nentidis, A., Krithara, A., Katsimpras, G., Paliouras, G., & Krallinger, M. (2022). Overview of DisTEMIST at BioASQ: Automatic detection and normalization of diseases from clinical texts: results, methods, evaluation and multilingual resources. Working Notes of Conference and Labs of the Evaluation (CLEF) Forum. CEUR Workshop Proceedings

@article{miranda2022overview,
title={Overview of DisTEMIST at BioASQ: Automatic detection and normalization of diseases from clinical texts: results, methods, evaluation and multilingual resources},
author={Miranda-Escalada, Antonio and Gascó, Luis and Lima-López, Salvador and 
Farré-Maduell, Eulàlia and Estrada, Darryl and Nentidis, Anastasios and Krithara, Anastasia and 
Katsimpras, Georgios and Paliouras, Georgios and Krallinger, Martin},
booktitle={Working Notes of Conference and Labs of the Evaluation (CLEF) Forum. CEUR Workshop Proceedings},
year={2022}
}

