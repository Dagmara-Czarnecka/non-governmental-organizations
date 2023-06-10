# Non-governmental-organizations
The aim of the workshop is to collect information about NGOs from any chosen category. The information will come from the website https://spis.ngo.pl/. The page content is generated on the server, so a combination of the requests and bs4 libraries would suffice to extract most of the information, but to decrypt email addresses you need to run JavaScript code - for that you will need the selenium library.

Go to https://spis.ngo.pl/ and choose any foundation.

Initially, the foundation's email address is not displayed, nor is it stored in the code of the website in an open form. Only clicking on the "Show" link activates the JavaScript script on the page, which decrypts it and shows it in the right place.

My task is to collect information about foundations from the selected category. Write a script that uses requests and bs4 to read the category page (put the URL to this page manually at the beginning of the script) and extract links to the pages of individual foundations from it, and then use selenium to visit these links one by one and extract information about foundations:

email address (string)
www addresses (list of strings - there may be more)
telephones (list of strings - there may be more)
KRS (string)
REGON (string)
VAT number (string)
year of creation (string)
Save the collected information in a CSV file. Place website addresses in one column, separated by a space. Put the phones in one column, separated by commas.
