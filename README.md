## nanoGPT training and inference in Dutch language - Trained from scratch

Simple GPT model training for several Dutch books. The nanoGPT model used in this project refers to Andrej Karpathy's nanoGPT video lecture [code](https://github.com/karpathy/ng-video-lecture).

### Training Data

Following open-source plain text books were obtained from [Project Gutenberg](https://gutenberg.org/) website

* [Aan de Zuidpool by Roald Amundsen](https://gutenberg.org/ebooks/14269)
* [Onder Moeders Vleugels by Louisa May Alcott](https://gutenberg.org/ebooks/17337)
* [Columbus: De ontdekker van Amerika by John S. C. Abbott](https://gutenberg.org/ebooks/18066)
* [In Griekenland by A. Adossidès](https://gutenberg.org/ebooks/28085)
* [Prometheus Geboeid by Aeschylus](https://gutenberg.org/ebooks/57697)

### Preprocessing

Before feeding to GPT model, data was preprocessed in following ways:

* Uppercase to lowercase - it is better to keep same words in exactly same shape. Multiple variants of the same word can confuse the model.
* Removing punctuation, special characters, numbers, brackets - anything more than actual words themselves will not be necessary for the model training.
* Removing whitespaces in cases when there are more than one consecutive repetition.
* Normalizing accents - the dutch language is characterized by the use of accents on vowels. These accents are harder to interpret for the model, thus will be normalized - replaced by their normal counterparts.


### Training

Training code is same as provided by [nanoGPT video lecture](https://github.com/karpathy/ng-video-lecture) and can be viewed in the jupyter notebook provided in this repo.

*Note : Since the model is simple, it is possible to run the training process on personal CPU as well as free Colab or Kaggle account. In this case, model was trained on personal CPU with 16GB RAM, 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz CPU*

*Note : This project is intended for self-educational purpose. Credit is given where it is due.*
