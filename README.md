# ReMatch
K-Cap 2017 Project 
## Capturing Knowledge in Semantically-typed Relational Patterns to Enhance Relation Linking
Note: The evaluation results for K-Cap 2017 paper is in "Evaluation results" Folder.

## For Installation and Running
> Please read the entire README file before doing anything

### Python Version
Python 2.7 :thumbsup:

### Required packages
* numpy
* glove_python
* sklearn
* practnlptool
* textrazor
* cPickle
* distance
* nltk
* SocketServer
* urllib
* json
* re

### Required data files
* glove precomputed data files
  - download from (http://nlp.stanford.edu/data/glove.6B.zip) the default file used by the code is (glove.6B.50d.txt)
* patty data files (included <not big>)

### Required Data
* text-razor API key

## Code explanation:
PS. File names are self explanatory

1. Tagger: POS tagger
1. Splitter: split the question into combinations
1. Embedder: glove wrapper to convert question into vectors
1. Reader: PATTY data reader
1. Backend: the complete process of reading PATTY data and create embeddings, with the cosine similarity code
1. Frontend: the complete process of reading a question and processing it
1. Textrazor_Api: the API wrapper for the textrazor service
1. main: where the magic happens
1. api: for the web UI interface
1. webService: for calling the system as a web service locally

## Running local web service
Running the service via **./webService.py [port]**


and calling it is simple i.e. (http://localhost/question_url_encoded)
  - Response will look like this:
  ```
  {
   "results":[
      "result 1",
      "result 2", ...
   ],
   "parts":[
      "part 1",
      "part 2", ...
   ],
   "pos":[
      [
         "word",
         "pos tag"
      ], ...
   ],
   "relation 1": "dbpedia relation lable",
   "relation 2": "dbpedia relation lable",
   ...
   "relation N": "dbpedia relation lable",
   "gen_question":"generalized question here",
   "question":"the input question"
}
  ```

## Fast run
please run the code once using the main file to create the *.dat files that will be just loaded other times which will reduce processing time because not extra processing is done.

running main file is straightforward **./main.py** 

## Any other issues while running the code:
Please email :email: to Yaser (yaser.jaradeh@gmail.com) or Kuldeep (kskuldeepvit@gmail.com) if you face any problem.

