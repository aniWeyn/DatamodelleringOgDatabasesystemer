# Datamodellering og Databasesystemer

## Assignment 1
### XAMPP Installation problems
#### XAMPP - Port 80 in use by “Unable to open process” with PID 4!
This solution will let you to develop with XAMPP and with Microsoft solutions (such as ISS and MS SQL)

##### Solution:
Set Apache to listen on a different port:
1. click on the "Config" button on the same line as the "Apache" module
2. select the "httpd.conf" file in the dropdown 
3. change the "Listen 80" line to "Listen 8080"
4. save the file and close it.

**phpMyAdmin page: http://localhost:8080/phpmyadmin/**

Source: https://stackoverflow.com/a/22357053

### Installing PHPUnit - Windows
Denne PCen -> Egenskaper -> Avanserte systeminnstillinger -> Miljøvariabler -> Brukervariabler for DinBrukerNavn -> Ny

Add this two path to the PATH:
```sh
C:\bin
C:\xampp\php
```

### FunctionalTest - Failed asserting that false is true
If you changed port 80 rember to change 

```sh
protected $baseUrl = 'http://localhost:8080/IMT2571/assignment1/';
```

### UnitTests - No such file or directory
go to UnitTests.php 
check is

```sh
require_once("../src/model/DBModel.php");
```
correct due to your files system you have created
