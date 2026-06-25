
---------------------------
1. RELEASE NOTES
---------------------------
- Full 5-page implementation (Journal, Progress, Leaderboard, Challenge Progress, Goal Progress)
- Directus API integration for live mood/activity data
- Mobile-first UI using Bootstrap + custom CSS
- Challenge streak tracking and dynamic chart rendering
- Configurable user login via email query parameter (local version)

---------------------------
2. REPOSITORY AND URL'S
---------------------------

Github URL: https://github.com/woofya/Owner-Progress-Reports

URL deploy project (not deployed currently): https://woofya.com/app/signin

---------------------------
3. DEPLOYMENT INSTRUCTIONS
---------------------------

---------------------------
PRE-CONDITIONS
---------------------------
Before running the project, make sure you have the following installed:

 - PHP 8.0+: Required to run backend files (e.g., `includes/progress.php`).
 - Local Server: Use MAMP, XAMPP, or VS Code PHP Server extension.
 - Modern Browser: Chrome, Edge, or Firefox recommended.
 - Internet Connection: Needed to fetch live data from the Woofya API.


---------------------------
DEPLOYMENT
---------------------------

1. Open the OWNER-PROGRESS-REPORTS folder in VS Code.  
2. Create or verify your configuration file at: app/config.php
 - note: refer to credentials.txt or use example:
Example:

php
<?php
$config = [];

// Base API Configuration
$config['directus_url']   = 'https://admin.woofya.com/';
$config['directus_token'] = '5hduYIeKcDRyovhccg76NvZK-MJMlNgv';

// Default Email for Local Testing
$config['default_email']  = 'gazihoque95@gmail.com';
$config['email'] = !empty($_GET['email']) ? $_GET['email'] : $config['default_email'];

?>

3. Start PHP local server in bash terminal: php -S localhost:8000
4. Open browser and go to: http://localhost:8000/app/progress.php

