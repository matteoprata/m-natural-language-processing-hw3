# Natural Language Processing Homework 3 by Matteo Prata

**I suggest to read the project files in this order:**

1. [run.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/run.py) - It is the access point of the project, a straightforward interface to easily prepare all the input data for the Neual Architecture by leveraging external modules and to execute the Neural Architecture of choice. I would read this module first to have a clear overview of the whole project, after this, I would move to the submodules required by run.py.

2. [preprocessing_dataset.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/preprocessing_dataset.py) - It is a module containing three classes responsible for defining the structure of the parsed dataset. The three classes are the following: Dataset, Sentence and Word. Intuitively the Dataset is a set of sentences and a sentence is a sequence of words.

3. [preprocessing_parser.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/preprocessing_parser.py) - It is a module containing the functions to parse the input dataset. The access point is the function *parse_dataset*, for which given the directory of a dataset, it parses it and it produces useful dictionaries for the encoding of the dataset itself. It also disambiguates the dataset by reading the disambiguations from an input file.

4. [preprocessing_vocabularies.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/preprocessing_vocabularies.py) - It is a module containing the functions to build the lemma embeddings matrix and the sense embeddings matrix. Both functions also return dictionaries that map a key (lemma or sense) to the id of the vector in the embeddings matrix.

5. [preprocessing_embs_loader.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/preprocessing_embs_loader.py) - It is a module containing the functions to read the embeddings matricies stored on disk. 

6. [preprocessing_dataset_enc.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/preprocessing_dataset_enc.py) - It is a module containing the functions to encode the dataset according to the ids in the input dictionaries and to generate mini batches.

7. [neural_architecture.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/neural_architecture.py) - It is the module containing the class NeuralArchitecture, which is the skeleton of the three implemented models. Through this, by calling the function *execute_model* a TensorFlow graph evaluated. In particular by calling the functions *train*, *evaluation* and *test* the proper operations of the graph get executed.

8. [model1.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/model1.py) - It is a module containing the function to build the TensorFlow graph of model 1 (see report).


9. [model2.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/model2.py) - It is a module containing the function to build the TensorFlow graph of model 2 (see report).

10. [model3.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/model3.py) - It is a module containing the function to build the TensorFlow graph of model 3 (see report).

**others...** 
[utilities.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/utilities.py) and [constants.py](https://gitlab.com/matteoprata/matteo_prata_1593974_nlp18hw3/blob/master/constants.py) contain just irrelevant information to understand the system.



