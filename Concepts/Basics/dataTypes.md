# PHP Object

use this function to retrive a variable type. 
```php
var_dump($variable)
```
Classes and objects are the main aspects of object-oriented programming.

A class is a blueprint, template, for objects.
An Object is an instance of a class.

When a object is created, it inherit all the properties and behaviors from the class.
Each object in a class will have different values, but will share the same properties.

Imagine a class named Car.
A Car can have properties like model, color, and so on. For each property we define a variable, $model, $color, $etc.

If we include a __construct() function in a Class, PHP will automatically call this function when a new object is created.

### Exaple
```php
<?php
class Car {
  public $color;
  public $model;
  public function __construct($color, $model) {
    $this->color = $color;
    $this->model = $model;
  }
  public function message() {
    return "My car is a " . $this->color . " " . $this->model . "!";
  }
}

$myCar = new Car("black", "Volvo");
echo $myCar -> message();
echo "<br>";
$myCar = new Car("red", "Toyota");
echo $myCar -> message();
```

## Constants

A constant is an identifier for a simple value.
This valeu cannot be chaged during the script.
Unlike variables, constats always global acrros the entire script.

- Syntax
define(name, value, case-insensitive)

Parameters:

name: Specifies the name of the constant  
value: Specifies the value of the constant  
case-insensitive: Specifies whether the constant name should be case-insensitive. Default is false  

```php
<?php
define("GREETING", "Welcome to W3Schools.com!");
echo GREeTiNG; // outputs Welcome to W3Schools.com!  
```
Constant Arrays
```php
<?php
define("cars", [
  "Alfa Romeo",
  "BMW",
  "Toyota"
]);
echo cars[0];
```


