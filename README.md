# cmpe597_final_project

#### SANER ####
* Download BERTurk from HuggingFace copy model's files to SANER\data\BERTurk
* Download ELECTRA-Turk from HuggingFace copy model's files to SANER\data\ELECTRA
* Run our_TENER.py, if you want to use another dataset, you shoul modify below parts:

```
In our_TENER.py


paths = {
        "train": "data/{}/train.txt".format(dataset),
        "test": "data/{}/test.txt".format(dataset),
        "dev": "data/{}/dev.txt".format(dataset)
}
```


```
In get_context.py

trainPath = os.path.join(data_dir_path, "train.txt")
    devPath = os.path.join(data_dir_path, "dev.txt")
    testPath = os.path.join(data_dir_path, "test.txt")
```


#### J-MULTI ####
* Run python3 main.py --command train --overwrite-mappings 1 command
* if you want to use another dataset, you shoul modify below parts:
```
In utils/__init__.py

optparser.add_option(
                "--{label}_train_file".format(label=label), default="dataset/train.txt",
                help="Train set location"
            )
            optparser.add_option(
                "--{label}_dev_file".format(label=label), default="dataset/dev_wiki.txt",
                help="Dev set location"
            )
            optparser.add_option(
                "--{label}_test_file".format(label=label), default="dataset/test_wiki.txt",
                help="Test set location"
            )
			
```

#### Jupyter Notebook ####

* All other parts in jupyer notebook and all of them can be run end-to-end to train/eval