# My First CodeIgniter 4 Project For Practical

# List Practical
 - [HMCV Routes BaseController](https://github.com/Ekhel/CI4-practical/tree/master/modules/Beranda)
    - Set Route file from app/Routes.php

    ```php
    if (file_exists(ROOTPATH.'modules')) {
	    $modulesPath = ROOTPATH.'modules/';
	    $modules = scandir($modulesPath);

	    foreach ($modules as $module) {
		    if ($module === '.' || $module === '..') continue;
		    if (is_dir($modulesPath) . '/' . $module) {
			    $routesPath = $modulesPath . $module . '/Config/Routes.php';
			    if (file_exists($routesPath)) {
				    require($routesPath);
			    } else {
				continue;
			    }
		    }
	    }
    }
    ```
    
