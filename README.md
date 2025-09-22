# ModelScan Demo

ModelScan is an open source project from Protect AI that scans models to determine if they contain unsafe code. It is the first model scanning tool to support multiple model formats. ModelScan currently supports: H5, Pickle, and SavedModel formats. This protects you when using PyTorch, TensorFlow, Keras, Sklearn, XGBoost, with more on the way.

**[Link to the offcial GitHub repository](https://github.com/protectai/modelscan)**

**Model Serialization Attack:** A Model Serialization Attack is where malicious code is added to the contents of a model during serialization(saving) before distribution.

**A Model Serialization Attack can be used to execute:**

* Credential Theft(Cloud credentials for writing and reading data to other systems in your environment)
* Data Theft(the request sent to the model)
* Data Poisoning(the data sent after the model has performed its task)
* Model Poisoning(altering the results of the model itself)

Read more about how ModelScan works [here](https://github.com/protectai/modelscan?tab=readme-ov-file#getting-started).

**There are 4 notebooks in this repository:**
* [keras.ipynb](keras.ipynb) 
* [tensorflow.ipynb](tensorflow.ipynb)
* [keras.ipynb](keras.ipynb)
* [xgboost.ipynb](xgboost.ipynb)

The notebooks included focus on model serialization attack on a particular ML library. We carry out a stealth mock exfiltration attack. Stealth, because the model still works as before the attack. Mock, because we don't actually carry out an exfiltration attack but show a POC where it can be carried out.

This is a clone with small modifications. The original code can be found [here](https://github.com/protectai/modelscan/tree/main/notebooks#notebooks-demonstarting-model-serialization-attacks).

### Installation and running steps:

1. Create a virtual environment (venv) using:
```
python3 -m venv venv
```
2. For Mac and Linux, activate venv:
```
source venv/bin/activate
```
3. Install all the necessary [requirements](requirements.txt) in the venv:
```
pip install -r requirements.txt
```
4. Go through the notebook one by one and observe the code in every cell and read the descriptions about it.

### Questions:
1. What is the mock exfiltration attack happening the code?
2. Think like an adversary. How this can happen in real life?
3. Think like a defender and think of how these results can be helpful. What else can be done after using this tool?