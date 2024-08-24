# NLP-Jokes-recognition-
LSTM, CNN, RNN with embedings, LSTM with embedings and Albert-Base-V2 fine tuned model for jokes recognition

Dataset "200K SHORT TEXTS FOR HUMOR DETECTION" downloaded from https://www.kaggle.com/datasets/deepcontractor/200k-short-texts-for-humor-detection containing 200000 unique texts labeled as humor or not. Categories are evenly distributed.

requirements.txt contain all required packages to sucessfuly run JokesRecognition.ipynb notebook.

In the notebook 5 models for jokes recogniton were tested: Bidirectional LSTM, CNN, RNN with GloVe vectors embeddings, LSTM with GloVe vectors embeddings and fine tune Albert-Base-V2.
The best performance showed fine tune Albert-Base-V2 with 98.74% accuracy
Second - RNN with GloVe embeddings with 93.15% accuracy
Third - CNN with 91.06% accuracy
Both LSTM models took very long time to train and performance was below 80%

To test the models please adjust `path`, `model_path` variables for respective models and location of your downloaded files (I used google drive for dataset and trained models storage)
When using trained models skip cells with `train` and `evaluate` functions.
To test new sentences please add them to `name` list

In Colab environment, to run succesfuly fine tuned albert model it may be nescessary to `!pip install accelerate -U` and restart sesion.
