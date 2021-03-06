# Very short description of the package

This package can find latitude and longitude from jpeg photos metadata.

## Installation

You can install the package via composer:

```bash
composer require simpledev/geofinder:dev-master
```

## Usage Example

``` php
use Simpledev\Geofinder\Geofinder;

if(!empty($_FILES['photo']))
{
	$photo = $_FILES['photo'];
	$finder = new Geofinder();
	$coords = $finder->getCoords($photo['tmp_name']);

	var_dump($coords); //return array(2) { ["latitude"]=> float(47.977730555556) ["longitude"]=> float(-4.4286277777778) } or false if geolocation not found

	if($coords){
		$lat = $coords['latitude']; //get latitude
		$lng = $coords['longitude']; //get longitude

		//do something with latitude and longitude
	}
}
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Credits

- [Fabien LE CORRE](https://github.com/simpledev)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

## PHP Package Boilerplate

This package was generated using the [PHP Package Boilerplate](https://laravelpackageboilerplate.com).