
# AI Synonyms generator for Taboo (157 languages supported)

## Purpose
Given a list of random words, iterate on each word and generate a list of words (up to 10) that are similar in the meaning. I used this algoritm to generate the words for my game [OpenTabu](https://github.com/rignaneseleo/OpenTabu).

## How it works
The algorithm uses an AI model to predict the meaning of a word. Then, it uses the meaning to find similar words. The model used is made by [E. Grave et al.](https://arxiv.org/abs/1802.06893) and it's available in 157 languages. In my case, I used the Italian model, but you can use any language you want.

## Logic
The logic is very simple:
1. Given a list of words, iterate on each word
2. For each word, get 10 similar words using the model
3. Clean up the list of similar words, since some of them are too simliares to the original word or are not meaningful words

## Tutorial
#### Prerequisites
1. Get the model you need from this page: https://fasttext.cc/docs/en/crawl-vectors.html and rename it to `model.bin`
2. Get a list of words and save it in a file (`words.csv`). Each word must be in a different line. No headers needed (check the example folder)
3. Install python3 (there are many tutorials online)
4. Install VS code (optional, but it's a good IDE)

#### Execution
1. Download and extract the files of this repo
2. Put the model (`model.bin`), the input file (`words.csv`) in the same folder of the extracted repo
3. Open the `main.ipynb` file with VS code (or any other IDE). In VS code you may need to install Python and Jupyter Notebook extension.
4. Run the code
5. Wait for the script to finish (it might take a while, depending on the number of words and the CPU power)
6. The script will create a file named `output.csv` with the list of similar words (each word in a new line, where the first is the original word)

## Source of words
Where can you get the list of random words to run this algorithm? There are many websites, I used the website www.palabrasaleatorias.com that allow you to get up to 10 random words from different topics.

## Example
Check out the example folder to see the input and output files.

## Errors
#### "ImportError: No module named xxx"
You need to install the missing module. Use `pip` to install it.

#### Other error
[StackOverflow](https://stackoverflow.com/) is your friend :) 
In case you can't solve it, open an issue on this repo and I will try to help you.

## References
- Thanks to [Giacomo D'Amicantonio](https://github.com/GiacomoDamicantonio) for the idea and the big help in the implementation.
- Thanks to the authors of the model: E. Grave*, P. Bojanowski*, P. Gupta, A. Joulin, T. Mikolov, "[Learning Word Vectors for 157 Languages](https://arxiv.org/abs/1802.06893)" 
