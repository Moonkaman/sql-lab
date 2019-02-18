# Database Queries

## find all customers that live in London. Returns 6 records.

## select \* from customers where city='London';

4 Around the Horn Thomas Hardy 120 Hanover Sq. London WA1 1DP UK
11 B's Beverages Victoria Ashworth Fauntleroy Circus London EC2 5NT UK
16 Consolidated Holdings Elizabeth Brown Berkeley Gardens 12 Brewery London WX1 6LT UK
19 Eastern Connection Ann Devon 35 King George London WX3 6FW UK
53 North/South Simon Crowther South House 300 Queensbridge London SW7 1RZ UK
72 Seven Seas Imports Hari Kumar 90 Wadhurst Rd. London OX15 4NB UK

## find all customers with postal code 1010. Returns 3 customers.

## select \* from customers where postalcode='1010';

12 Cactus Comidas para llevar Patricio Simpson Cerrito 333 Buenos Aires 1010 Argentina
54 Océano Atlántico Ltda. Yvonne Moncada Ing. Gustavo Moncada 8585 Piso 20-A Buenos Aires 1010 Argentina
64 Rancho grande Sergio Gutiérrez Av. del Libertador 900 Buenos Aires 1010 Argentina

## find the phone number for the supplier with the id 11. Should be (010) 9984510.

## select phone from suppliers where supplierid = '11'

(010) 9984510

## list orders descending by the order date. The order with date 1997-02-12 should be at the top.

## select \* from orders order by orderdate desc

10443 66 8 1997-02-12 1
10442 20 3 1997-02-11 2
10440 71 4 1997-02-10 2
10441 55 3 1997-02-10 2
10439 51 6 1997-02-07 3
10438 79 3 1997-02-06 2
etc...

## find all suppliers who have names longer than 20 characters. You can use `length(SupplierName)` to get the length of the name. Returns 11 records.

## select \*, length(suppliername) as NameLength from suppliers where length(suppliername) > 20 order by NameLength

14 Formaggi Fortini s.r.l. Elio Rossi Viale Dante, 75 Ravenna 48100 Italy (0544) 60323 23
8 Specialty Biscuits, Ltd. Peter Wilson 29 King's Way Manchester M14 GSD UK (161) 555-4448 24
3 Grandma Kelly's Homestead Regina Murphy 707 Oxford Rd. Ann Arbor 48104 USA (313) 555-5735 25
10 Refrescos Americanas LTDA Carlos Diaz Av. das Americanas 12.890 São Paulo 5442 Brazil (11) 555 4640 25
etc...

## find all customers that include the word "market" in the name. Should return 4 records.

## select \* from customers where customername like '%market%'

10 Bottom-Dollar Marketse Elizabeth Lincoln 23 Tsawassen Blvd. Tsawassen T2F 8M4 Canada
32 Great Lakes Food Market Howard Snyder 2732 Baker Blvd. Eugene 97403 USA
71 Save-a-lot Markets Jose Pavarotti 187 Suffolk Ln. Boise 83720 USA
89 White Clover Markets Karl Jablonski 305 - 14th Ave. S. Suite 3B Seattle 98128 USA

## add a customer record for _"The Shire"_, the contact name is _"Bilbo Baggins"_ the address is _"1 Hobbit-Hole"_ in _"Bag End"_, postal code _"111"_ and the country is _"Middle Earth"_.

## update _Bilbo Baggins_ record so that the postal code changes to _"11122"_.

## list orders grouped by customer showing the number of orders per customer. _Rattlesnake Canyon Grocery_ should have 7 orders.

## list customers names and the number of orders per customer. Sort the list by number of orders in descending order. _Ernst Handel_ should be at the top with 10 orders followed by _QUICK-Stop_, _Rattlesnake Canyon Grocery_ and _Wartian Herkku_ with 7 orders each.

## list orders grouped by customer's city showing number of orders per city. Returns 58 Records with _Aachen_ showing 2 orders and _Albuquerque_ showing 7 orders.

## delete all users that have no orders. Should delete 17 (or 18 if you haven't deleted the record added) records.
