---
title: SQL
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "September 18, 2020"
summary: 
published: true
sidebar: misc_sidebar #name of yml sidebar file withouth extension
permalink: sql.html
folder: misc
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## Structured Query Language (SQL)

Structured Query Language (SQL, pronounced “See-Quel”) is the standard language for working with relational databases. In a database, SQL statements are used to generate queries to collect or modify data.

### What is a relational database?

A relational database is a type of database that stores data that are related to one another. Relational databases are based on the relational model, where each row in a table is a record with a unique ID, known as a key. The columns of a table hold attributes of the data, allowing for relationships between data points to be explored.

For example, imagine you run a small online business. For simplicity, assume to keep two data tables, one for customer information, and the other for orders. The customer information table would have the customer’s name, shipping address, billing address, phone number, and other customer information. Each attribute would be a separate column and each customer would be a separate row and be assigned a unique ID number. In the second table, customer orders, the attributes would be the customer’s ID number, the product ordered, the quantity, and other order details. Again, each attribute would be a separate column, and each order would be a separate row.

These two tables have one thing in common, the customer’s ID number, or key. This allows a relationship to be formed between the two tables. When you want to ship the product to the customer, you would find the correct product (and quantity), and then use the key to find the customer’s shipping information.
This was a very simplistic example, but can be scaled to many tables, all with different information, but related by different keys. This method is very efficient and great for maintaining data consistency across different applications.

### Why learn SQL?

* https://learnsql.com/blog/four-reasons-aspiring-data-scientists-must-learn-sql/

### Getting started with SQL:

* https://www.youtube.com/watch?v=IXycPq7MnwE
* https://www.youtube.com/watch?v=bEtnYWuo2Bw&t=333s

### Online tutorials

* http://www.sqlcourse.com/
* https://github.com/linbojin/sql-tutorial
* https://gist.github.com/momer/19a159ffc336a047b2fa

{% include links.html %}
