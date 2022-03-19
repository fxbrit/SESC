# SESC
SESC (search engine for smart contracts) is an extension of my [ContractCrawler](https://github.com/fabritrv/ContractCrawler) project that allows you to search through the contracts you previously crawled, and more.


**HOW TO USE**:
1. Enter the directory that contains all of the source code of the contracts that you previously got using ContractCrawler.
2. Enter 'txt' if you files are saved as .txt or 'sol' if they have .sol extension.
3. Select one of the _available options_.
4. Create the cache and run the parser. (optional but suggested)

The _available options_ are:

0. Create graph -> See v.5.x notes.
1. Create cache -> Enter 20 keyword and search them all at once to create the cache. This will speed up your next searches.
2. Search by keyword -> Enter a keyword and the number of results you want to see. If you already parsed the contracts you'll be able to get even more details.
3. Search by sentence -> See v.3.x notes.
4. Delete cache.
5. Parse each contract present in the directory you specified when launching SESC.
6. Parse a single contract -> Just enter its address and get its functions and variables.
7. Exit.


I highly reccomed reading the rest of the notes before using SESC.
The results for options number 0, 2 and 3 can be displayed in a cooler way, more details below.


**DISPLAY BETTER RESULTS**:

SESC can show results in a better and more intuitive way. When you run one of the functionalities a JSON will be produced, in particular:
1. Graph -> generates a JSON that can create a dendrogram
2. Search by sentence -> generates a JSON that can create a circle packing
3. Search by keyword -> generates a JSON that can create an indented tree
by using and adapting [D3's founder Mike Bostock work](https://observablehq.com/@mbostock). You can find full details on what I edited, links to Mike original work as well as a thank you message to him and a couple other brief details in the localh directory.

To display the results, run then function and wait for the completion as usual, then cd to localh and enter 
```python
python3 -m http.server
```
then open your browser and go to localhost:8000. A small menu will appear, you just have to select what you want to visualize. Credits, notes and details are available in the menu as well.

**NOTE**:
If you got your source codes through a different source it should still work as long as the source code of the smart contracts is formatted in a standard way.
