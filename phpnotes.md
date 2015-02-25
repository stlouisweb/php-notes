# PHP Design Patterns


## Factory Pattern

In a factory pattern a **class** creates the **object** you want to use. 
### example:

```php
<?php
// Defining the Automobile class.
class Automobile
{
    private $vehicleMake;
    private $vehicleModel;

    public function __construct($make, $model)
    {
		$this->vehicleMake = $make;
		$this->vehicleModel = $model;
	}
	
	public function getMakeAndModel()
	{
		return $this->vehicleMake . ' ' . $this-> vehicleModel;
	}
}

// The factory which creates objects of the Automobile class.
class AutomobileFactory
{
	public static function create($make, $model)
	{
		return new Automobile($make, $model);
	}
}

// Using the factory to create an Automobile object.
$Camaro = AutomobileFactory::create('Cheverolet', 'Camaro');

print_r($Camaro->getMakeAndModel());  //outputs "Cheverolet Camaro"
```

Using the factory pattern like this is DRY because you could make changes to the Automobile class later and you would only need to modify the factory instead of every place in your project that uses the automobile class.
The factory pattern also makes it easier to instantiate complex objects of a given class, you can do all the heavy lifting inside the factory.

In class-based programming a factory is an abstraction of a constructor of a class, while in prototype-based programming a factory is an abstractions of a prototype object.

