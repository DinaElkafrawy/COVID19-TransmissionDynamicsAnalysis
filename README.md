# Transmission Dynamics of the COVID-19
![covid.jpg](attachment:covid.jpg)

This notebook provides insight on COVID-19 transmission dynamics by using text mining. The notebook includes information collected from Open Research Dataset (CORD-19), after several filteration and editing. The output provides information about the following:
* Basic reproductive number
* Incubation period 
* Serial interval
* Modes of transmission
* Environmental factors

### Methodology
The steps are clearly stated and documented as you go down the notebook. 

#### A summary of the approach:
*    
     1. Dataset was prepared, sorted with most recent first and duplicates/nan/citations were removed. Only documents that reference COVID-19 in its different forms were kept.
     2. A list of relevant terms was created.
     3. Spacy Phrasematcher was used to extract the relevant terms from each document (if it had any).
     4. Term frequency for each document was calculated.
     5. A set which contained each document with its corresponding terms and their sentences was extracted.
     6. The sentences were then refined to make sure they contain relevant information (explained below). 
     7. Two graphs are plotted, one for the different incubation periods and the number of articles that agree on them and the other one is for the different modes of transmission and the number of articles that mentions them.
     8. In each document, each matched term is joined with its refined sentence.
     9. Documents are sorted according to the total number of matches, which was used as a relevance scale. The higher number of matches the more relevant they are. 
     10. For each point for the transmission dynamics mentioned above, the top 4 relevant documents are viewed, showing as much necessary information as possible. 

#### Pros of the approach:
The notebook provides a promising output, showing relevant results in a very simple way which is easily understood.
#### Cons of the approach:
More accurate results could be achieved, if a more specific rule based matcher is used.
