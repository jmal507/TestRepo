# Volga Website
### Author
Jamal Barrett
```
```
## Components:
**Introduction**
Volga is a website that lists various books. Its users can just see lists of books in various genres. It also displays the query responsible for the data displyed.
```
```
## Files:
**index.html**
User see's this page upon loading. The login must be hardcoded as the implementation for user friendly login is not implemented. From this page there are various links in the left sidebar showing all the current genres within the database. Clicking one of the list elements brings you to a seperate php page where a table of books specific to that element is rendered. On the left sidebar, there is an unfinished attempt at Genre Specific searches through both id and name. Using form data it returns user-specified search results. Those results are posted onto "index.php" and the user is forwarded to that page.

**index.php**
This page simply displays form data from "index.html".

**getGenre(x).php**
Each file that starts with getGenre is what appears after a user clicks a genre's respective link from the sidebar on "index.html". The number at the end of the file denotes which genreId is being referenced. Each php file with getGenre uses the same implementation:
1.) link to the database with harcoded login credentials
2.) save that data in a msqli connect
3.) depending on whether or not the link has connected: throw an error or continue with data extraction
4.) save a query to parse through a list of isbn's for the specific genreId
5.) Echo the Table heading for the Title, Price, ISBN, Pages, Binding, and Publication Date
5.) iterate through the result of the query and save its isbn
6.) save a query to parse through a list of books where the isbn matches the previous result
6.) iterate through the result of the second query while the isbn of the last query is saved
8.) Echo Title, Price, ISBN, Pages, Binding, and Publication Date into the table's data
```
```
## Folder(s) ##
**books**
Images for all books but those with genreId 301, 302 and 303
```
```
