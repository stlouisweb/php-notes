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

print_r($camaro->getMakeAndModel());  //outputs "Cheverolet Camaro"
```

Using the factory method 
