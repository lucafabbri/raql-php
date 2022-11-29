# RAQL.PHP
## Installation

you can install the library using composer

```bash
composer require higrow/raql-php
```
## Usage
### Laravel/Eloquent

Create a model that uses RAQLTrait

```PHP
use RAQL\PHP\Eloquent\RAQLTrait;

class MyModel extends Model{
  use RAQLTrait;
  ...
}
```

Call the .raql($query) Query Builder extension method

```PHP
$query = "(field1 like 'name' or field1 = 'mario') and field2 >=10

MyModel::raql($query)->get();

```
