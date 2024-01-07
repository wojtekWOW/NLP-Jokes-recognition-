# NLP-Jokes-recognition-
LSTM, CNN, RNN with embedings, LSTM with embedings and Albert-Base-V2 fine tuned model for jokes recognition

# NLP-Rozpoznawanie-żartów-
LSTM, CNN, RNN z osadzeniem, LSTM z osadzeniem i precyzyjnie dostrojony model Albert-Base-V2 do rozpoznawania żartów

Zbiór danych „200 000 KRÓTKICH TEKSTU DO WYKRYWANIA HUMORU” pobrany ze strony https://www.kaggle.com/datasets/deepcontractor/200k-short-texts-for-humor-detection zawierający 200 000 unikalnych tekstów oznaczonych jako humorystyczne lub nie. Kategorie są równomiernie rozłożone.

plik requirements.txt zawiera wszystkie pakiety wymagane do pomyślnego uruchomienia notatnika JokesRecognition.ipynb.

W notatniku przetestowano 5 modeli rozpoznawania żartów: Bidirectional LSTM, CNN, RNN with GloVe vectors embeddings, LSTM with GloVe vectors embeddings i fine tune Albert-Base-V2.
Najlepszy wynik wykazał Albert-Base-V2 z dokładnością 98,74%.
Drugi – RNN z GloVe z dokładnością 93,15%.
Trzeci – CNN z dokładnością 91,06%.
Trening obu modeli LSTM trwał bardzo długo, a wydajność była poniżej 80%

Aby przetestować modele, dostosuj zmienne `path`, `model_path` dla odpowiednich modeli i lokalizacji pobranych plików (użyłem dysku Google do przechowywania zbioru danych i wytrenowanych modeli)
Podczas korzystania z wytrenowanych modeli pomiń komórki z funkcjami `train` i `evaluate`.
Aby przetestować nowe teksty, dodaj je do listy `name`

W środowisku Colab, aby pomyślnie uruchomić dostrojony model Alberta, może być konieczne wykonanie polecenia `!pip install accelerate  -U` i ponowne uruchomienie sesji. Bez tego kroku `Trainer` i `TrainingAgruments` z pakietu `transformers` nie zadziałałyby.

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

In Colab environment, to run succesfuly fine tuned albert model it may be nescessary to `!pip install accelerate -U` and restart sesion. Without this step `Trainer` and `TrainingAgruments` from `transformers` package didn't work.
