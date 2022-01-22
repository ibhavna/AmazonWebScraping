# AmazonWebScraping
This webscraping is done by using a python library - Selenium and then finally connected to database using pymysql. The CSV file which was provided to me to construct the urls, I loaded that in my jupiter notebook using pandas. Then I constructed the urls as per the suggested format using list comprehension. Then I created a dictionary named "data" whose values are empty lists, which later were appended by the extracted data. Then I invoke the chrome driver under a for loop of targetd urls with a sleep time of 3 seconds each. 

#extracting data
I extracted the mentioned data under "try" block so that if urls with "error 404" would come so that can be sent to exception without terminating the code.
For product titles:- I selected the class name, bcoz that was common to every product, and iterated a variable through it and later printed it in text format, same I did for extracting product price.
For product image url :- I firstly selected the common class having image, then searched by tag name = img, then by get attribute = src. I received the urls in string format.
For product details :- I selected the common id, bcoz when I was doing with "class", so it  was not fetching the data, then I went for find elements by tag name = "li". Then iterated a variable and printed it in text format.

After this , when I printed the data, I was able to spot few "" blanks in the value pairs of the dictionary, so I got them removed using try and except and remove method of list.
finally dumped that into json and connected the json with mysql database using PyMySQL.


