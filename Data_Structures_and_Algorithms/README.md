The assignment pdf is listed within the repository but here is a quick summary. 

An example of an input that will insert a term into the tree would be: "i STRING".

To count how many currently stored terms that are lexicographically between STRING1 and STRING2: "r STRING1 STRING2".

# Usage

./wordrange input_file output_file

Example:

./wordrange Tests/allwords-more-range.txt output.txt

You can change the input file to any of the input files listed in the Tests folder.

In a linux environment, you can compare the actual and expected ouputs with:

diff ouput.txt Tests/allwords-more-range-output.txt



