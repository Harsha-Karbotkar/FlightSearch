# Flight Data Import and Search

## Introduction

This project is about uploading the flight details from backend and then performing the search operation from a frontend form with the user provided inputs.



## Prerequisite 
- PHP version 7.4 or newer 
- Codeigniter  4.4.3
- MySQL
- Local(Xampp) server


## Technologies Used:
- Codeigniter
- MYSQL Database
- HTML & CSS
- JS & JQUERY

## Setup:
### Virtual Host:
- Create virtual host at apache\conf\extra\httpd-vhosts.conf.Server name shall be flightbookings.com
- Create host Windows\System32\drivers\etc\hosts


### DB Configuration:
Update in app\Config\Database.php:
- database:flightbookings
- hostname:flightbookings.com

Note:Change user and password as per your system

## Database Tables
- airline_master:Master for airlines
- flight_master:Master for flights
- destination_master:Master for available destinations
- flight_trips:Table will contain the trip details provided for each of the flight and route

Note: Foreign keys were not added as it was creating problems for truncate command while data testing

## Api
- Data will be imported through an api with post method
- Input data should be in json format
- Api link :http://flightbookings.com/pushflightdata


## Fuctionality

### Data import
- All the tables will be populated through the API only
- The data is imported in respective tables
- Certain fields of trip details can be updated provided the same flight,route and departure time exists in the database.
- Validations are done for mandatory fields


### Search form
- Route:http://flightbookings.com/
- In order to check the search functionality,kindy import the data using API mentioned.
- Source and Destination dropdowns will be populated post data import.
- Search will be based on user selected filters
- Search will be  on the departure/return date and operational days.E.g if departure date is 4th Nov'23 then flight will be listed down.And if the operation days is 2,5, it is assumed that the flight will be available on every tuesday & friday,so even if date is not matching the flight will appear in search listing.
