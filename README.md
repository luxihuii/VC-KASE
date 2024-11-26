# KASE

## Introduction
Verifiable Conjunctive Field Keyword Searchable Encryption with Aggregate Keys for Data Sharing

## Build

### Compile
make main
### Clean
make clean
### Environmental requirement
install the pbc library
## Use
Open three terminals, which represent the server, dataowner, user.
* server: ./main 100 4 0
* dataowner: ./main 100 4 1
* user: ./main 100 4 2

argv[0] denotes test program. argv[1] denotes number of files, argv[2] denotes the number of keyword fields, argv[3] denotes parties, where 0 represents server, 1 represents dataowner, and 2 represents user.

* After running, the result is as follows：

```html
server:
server start
setup generte time 0.530655 s
search input 1, exit input 0:
------------------------------------------
dataowner:
setup generte time 0.00365242 s
DataOwner start
enc generte time 0.988993 s
------------------------------------------
user:
setup generte time 0.00383019 s
User start
search input 1, exit input 0:
```

* At this time, choose to input 1 to search, and 0 to exit the program.

* Input the number of documents shared by the data owner to the user.

```html
dataowner: please input you share file number:  10
```
* Input the keyword field for query.

```html
user: please input you wanted keyword field:  2
```
* Input the search keyword (you can choose a keyword from the plaintext file 1004 (it can be the second field or not))

```html
user: please input Corresponding keyword: ngrlvuxxrg
```
* Continue querying input 1, otherwise input 0. Continuing to query the target document needs to satisfy the conjunctive query.

```html
user: if continue query, input 1, else input 0:  0
```

```html
user: trap generte time 0.00343105 s
```

```html
server: file 2  match	-----> (search result)
search generte time 0.0741453 s
```




