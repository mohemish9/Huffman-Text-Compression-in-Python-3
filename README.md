# Huffman Text Compression in Python 3 

### Description
The idea is to use “variable-length encoding”. We can exploit the fact that some characters occur more frequently than others in a text to design an algorithm that can represent the same piece of text using lesser number of bits. In vari- able-length encoding, we assign a variable number of bits to characters depending upon their frequen- cy in the given text. So, some characters might end up taking a single bit, some might end up taking two bits, some will be encoded using three bits, and so on. The problem with variable-length encoding lies in its decoding.

Each node of the tree are represented with a byte symbol and the frequency of that byte on the data. The creation of the Huffman tree have the following steps:
Scan the data and calculate the frequency of occurrence of each byte;
* Insert those nodes into a reverse priority queue based on the frequencies(a lowest frequency is given highest priority);
* Start a loop until the queue is empty;
* Remove two nodes from the queue and combine them into a internal node with the frequency equal to the sum of the two nodes frequencies;
* Insert the two nodes removed from the queue as children of the created internal node;
* Insert the created internal node into the queue;
* The last node remaining on the queue is the root of the tree.

![alt text](https://www.techiedelight.com/wp-content/uploads/2016/11/Huffman-Coding-6.png)

### Prerequisites
Python 3.7+ 

### Usage
##### To compress 
```
python3 text_compress.py
```
Then enter the name of the text file you wish to compress.
##### To uncompress
```
python3 Text_uncompress.py
```
Then enter the name of the huffman file you wish to uncompress, while making sure the huffman.key file is in the same folder.

Only works for txt files.
