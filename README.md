# Trip-Advisor-based-on-Image-Recognition

-----------------------
###Team Information

Xingying Liu, Zhengrong Li, Sen Lin

EECS E6893 Big Data Analytics, Fall 2015

Columbia University 

xl2493@columbia.edu, zl2438@columbia.edu, sl3773@columbia.edu

-----------------------
###How to run:

1. Start server: in terminal, under the project directory, enter 

python app.py <port number> 


2. Go to 0.0.0.0:<port number>/upload to visit the website 

-----------------------
###Software Package description

root

|--app.py  (main program)

|--extract.py  (extract the features for all pictures in database, store the result in /file_index.csv and /pig/database.csv )

|--file_index.csv  (file_index, ImageID:Filename)

|--input  (store pictures uploaded by user)

|--lsh.so  (lsh library)

|--pig  

  |--gt*.out  (pig intermediate result [feature bag])

  |--pig.result  (pig intermediate result [vote])

  |--database.csv  (store all pictures' feature info, generated by extract.py offline)

  |--match.py  (pig latin embedded in python)

|--preprocess  

  |--rename.py (rename the pictures)

  |--squeeze.py (squeeze pictures into 200*200 pixel)

|--search.py (called by app.py, search for pictures similar to query)

|--static (picture database)

|--templates (html)

