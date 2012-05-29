#Boxcar.io Provider API bundle for Laravel

##Usage
In your routes.php simply start the bundle, set your login info, and call the API  
  
	Route::get('boxcar/create', function()
	{
		$api_key    = '123';
		$api_secret = '123';

		Bundle::start('boxcar');

		$output = Boxcar\Boxcar::init($api_key, $api_secret)
		                       ->broadcast('Test Name', 'Test Broadcast, this was sent at ' . date('r'));

		print_r($output);
		exit;
	});



See the [Boxcar Provider API documentation](http://boxcar.io/help/api/providers) for API details.

Bundle created by [Ben Edmunds](http://benedmunds.com).