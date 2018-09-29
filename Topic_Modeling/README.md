For the first part of this assignment, you will complete the functions `doc_to_synsets` and `similarity_score` which will be  
used by `document_path_similarity` to find the path similarity between two documents.  

The following functions are provided:
* **`convert_tag:`** converts the tag given by `nltk.pos_tag` to a tag used by `wordnet.synsets`.
You will need to use this function in `doc_to_synsets`.
* **`document_path_similarity:`** computes the symmetrical path similarity between two documents by finding the synsets in each
document using `doc_to_synsets`, then computing similarities using `similarity_score`.

You will need to finish writing the following functions:
* **`doc_to_synsets:`** returns a list of synsets in document. This function should first tokenize and part of speech tag the
document using `nltk.word_tokenize` and `nltk.pos_tag`. Then it should find each tokens corresponding synset using  
`wn.synsets(token, wordnet_tag)`. The first synset match should be used. If there is no match, that token is skipped.  
* **`similarity_score:`** returns the normalized similarity score of a list of synsets (s1) onto a second list of synsets (s2).
For each synset in s1, find the synset in s2 with the largest similarity value. Sum all of the largest similarity values
together and normalize this value by dividing it by the number of largest similarity values found. Be careful with data types,
which should be floats. Missing values should be ignored.

Once `doc_to_synsets` and `similarity_score` have been completed, submit to the autograder which will run
`test_document_path_similarity` to test that these functions are running correctly. 
