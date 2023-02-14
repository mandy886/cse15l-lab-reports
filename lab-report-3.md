# Researching Commands - Grep
# -c pattern
-c counts only--doesn't print lines--which can be useful for easily accessing the count of lines matching the pattern.

## Example 1
```
$ grep -c "1940" written_2/non-fiction/OUP/Abernathy/ch1.txt
1
```
Revealed that ch1.txt has 1 line that contains "1940".
## Example 2
```
$ grep -c "the" written_2/non-fiction/OUP/Abernathy/ch1.txt
68
```
Revealed that ch1.txt has 68 lines that contain "the".

# -n 
-n prints line numbers before matching lines. This can help you locate the String within the file.
## Example 1
```
$ grep -n "realistic" written_2/non-fiction/OUP/Abernathy/ch1.txt
25:The conventional wisdom explains the industry’s decline in this way: Apparel, particularly women’s apparel, is driven by price-based competition among generally small manufacturing and contracting establishments.17 Labor costs represent a significant portion of cost for many garment categories,18 and U.S. wage levels far exceed those of competitors in countries like the People’s Republic of China and Mexico.19 Although the magnitude of these differences varies as exchange rates fluctuate, under any 
exchange-rate scenario, the labor cost differential is sufficiently high to put U.S. manufacturers at a very significant competitive disadvantage.
77:Finally, Chapter 15 (“Information-Integrated Channels”) touches on a number of public policy issues raised by our findings. These include what can be done about the continuing problem of sweatshops, the new international economics of trade, and the effect of information integration on the business cycle and consumer prices at the macroeconomic level. Last but not least, we take a realistic look at the competitive future of the U.S. retail, apparel, and textile industries.
```
Appends line numbers ```25:``` and ```77``` to the beginning of lines containing ```realistic```.
## Example 2
```
$ grep -n "1940" written_2/non-fiction/OUP/Abernathy/ch1.txt
5:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.
```
Appends line numbers ```5``` to the beginning of lines containing ```1940```.

# -l 
-l lists filenames only--doesn't print lines, just the names they’re found in so that you can check which files in the directory contain the String.
## Example 1
```
$ grep -l "1940" written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
```
Prints out this filepath because "1940" is found in ch1.txt.

## Example 2
```
$ grep -l "beauty" written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```
Prints out this filepath because "beauty" is found in ch14.txt.

# -v 
-v inverts during printing so you can see which lines do NOT match the pattern.
## Example 1
```
$ grep -v "." written_2/non-fiction/OUP/Abernathy/ch1.txt   


```
Printed out blank lines because there were no lines that did not include "."

## Example 2
```
$ grep -v "the" written_2/non-fiction/OUP/Abernathy/ch1.txt   
grep -v "the" written_2/non-fiction/OUP/Abernathy/ch1.txt    



Five Decades of Change
A Dying Industry—or Not?
The Channel Perspective: Five Propositions
Proposition 1:  The retail, apparel, and textile sectors are increasingly linked as a channel through information and distribution relationships.
Similar dynamics are cropping up in nonclothing areas as well. Grocery stores now stock a profusion of toothbrushes, Home Depot has shelves and shelves of different light bulbs, and Dell offers custom-configured personal computers. The growing presence of fashion-basic elements in myriad consumer products means that all retailers and suppliers may find new competitive opportunities using replenishment.
How This Book Is Organized




```

# Sources
I was found all these grep command line options on [O'Reilly](https://www.oreilly.com/library/view/java-cookbook/0596001703/ch04s14.html) by Googling "grep command line options java."
