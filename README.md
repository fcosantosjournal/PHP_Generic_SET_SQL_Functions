# PHP_Generic_SET_SQL_Functions
An small collection of PHP SQL Functions to use or adapt to improve

# GenericModel Class Documentation

## Introduction

The `GenericModel` class is designed to provide a generic and reusable implementation for common CRUD (Create, Read, Update, Delete) operations on a MySQL database. It serves as a foundation for creating models with basic database interaction functionalities.

## Installation

No specific installation steps are required for the `GenericModel` class. Simply include it in your project and instantiate it as needed.

## Usage

### Instantiating the `GenericModel`

```php
<?php

use App\Models\GenericModel;

// Instantiate the GenericModel class
$model = new GenericModel();

// Example: Get all records from the 'example_table'
$result = $model->getAll('example_table');
print_r($result);

// Example: Get a record with ID 1 from the 'example_table'
$result = $model->getOne(1, 'example_table');
print_r($result);

// Example: Insert a new record into the 'example_table'
$fields = 'column1, column2, column3';
$values = "'value1', 'value2', 'value3'";
$result = $model->insert($fields, $values, 'example_table');
echo $result ? 'Record inserted successfully' : 'Failed to insert record';

// Example: Update a record with ID 1 in the 'example_table'
$fields = 'column1';
$values = "'new_value'";
$model->update(1, $fields, $values, 'example_table');

// Example: Delete a record with ID 1 from the 'example_table'
$model->delete(1, 'example_table');


