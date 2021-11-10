# Hello World!

Here is a little description of this cool ebay scraper program. Running this code, you can download the content of a specified number of Ebay pages on a search term into a JSON or .csv file for further analysis. The basic steps it follows are:

* generates an Ebay URL from your chosen search term
* downloads the specified number of results pages (default is 10)
* extracts important bits of information from each item's listing: price, items sold, free returns or not, shipping price
* compiles a JSON file containing these pieces

Also, for reference, here are the [project instructions](https://github.com/mikeizbicki/cmc-csci040/tree/2021fall/hw_03)

# How to Use

Open `ebay-dl.py` in VSCode and insert terminal commands in the following format:

For standard searches scraping 10 pages of results and one word search terms, run
```
python3 ebay-dl.py searchterm
```
in the command line. 

To scrape anything other than 10 pages, or search items with 2+ word search terms, run
```
python3 ebay-dl "search term" --num_pages=x
```

If you're intrested in reproducing the JSON files I've generated, you can run the commands
```
python3 ebay-dl.py sweatshirt
```
for the sweatshirt.json file, 
```
python3 ebay-dl.py doritos
```
for the doritos.json file, and 
```
python3 ebay-dl.py "apple product"
```
for the apple+product.json file

# Making CSV files

If you're also looking to generate .csv instead of JSON files with your data, you can do that too!

To specify .csv file generation in the command line, add a `--csv` flag in your command, making it look like:
```
python3 ebay-dl --csv searchterm
```
To generate the same .csv files I've generated, use the commands
```
python3 ebay-dl.py --csv sweatshirt
```
for the sweatshirt.csv file, 
```
python3 ebay-dl.py --csv doritos
```
for the doritos.csv file, and 
```
python3 ebay-dl.py --csv "apple product"
```
for the apple+product.csv file

I hope you find it useful! 
