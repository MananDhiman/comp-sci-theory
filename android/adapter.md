# Adapter
Acts as bridge between View and data. Responsible for making a view for each item in the data set. 

Used to bind data from data source (ex: arraylist, hashmap, sqlite db) with ui component such as list view, grid view

Types - Base: Parent Adapter

* ArrayAdapter - List of single items, backed by array
* Custom arrayAdapter - display custom list
* simpleAdapter - Easy adapter to map static data to views defined in xml
* Custom simple adapter- display custom list and needed to access child items of list or grid
