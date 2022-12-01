# gui-text-input-generator

## Dependencies

To satisfy prerequisite, run below commands on the project root:

```bash
> pip install -r requirements.txt 
> wget https://www.dropbox.com/s/l24p9l9q13unz0j/cc.en.300.bin # or download directly from https://www.dropbox.com/s/l24p9l9q13unz0j/cc.en.300.bin?raw=1

```

## How to run

To predict category of a textfield and possible input texts in it, we provide the script `predict_string.py` which accepts JSON files of Android screen states and produce rankings of matching categories & text input values.

```bash 
> python predict_string.py -i data/samsung_internal -o result/text_input_pred_samsung.json --predict-value --sample-value-file data/value_pool.json
```

The above script collects Android screen state files (with filenames like `state_*.json`) contained in the `data/samsung_internal` directory, and predict text input categories & values for the contained textfields in the screen. The result is saved into `result/text_input_pred_samsung.json`.
