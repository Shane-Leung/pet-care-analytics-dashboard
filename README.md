# Owner Progress Reports

## Overview

Owner Progress Reports is a mobile-first web application developed for Woofya to provide pet owners with data-driven insights into their pet's activity, wellbeing, and challenge progression. The application integrates with the Directus CMS to retrieve and visualise live data through an intuitive dashboard experience.

## Features

* Five integrated dashboard pages

  * Journal
  * Progress
  * Leaderboard
  * Challenge Progress
  * Goal Progress
* Directus API integration for live activity and mood data
* Dynamic activity and progress visualisations using Chart.js
* Challenge streak tracking
* Mobile-first responsive interface
* Configurable local user authentication via email query parameter

## Technology Stack

| Layer              | Technology                         |
| ------------------ | ---------------------------------- |
| Frontend           | HTML, CSS, Bootstrap 5, JavaScript |
| Backend            | PHP 8                              |
| Data Visualisation | Chart.js                           |
| CMS / API          | Directus CMS                       |

## Prerequisites

Before running the project, ensure the following software is installed:

* PHP 8.0 or later
* Local PHP server (MAMP, XAMPP, or VS Code PHP Server)
* Modern web browser
* Internet connection (required for Directus API requests)

## Installation

Clone the repository.

```bash
git clone https://github.com/woofya/Owner-Progress-Reports.git
cd Owner-Progress-Reports
```

## Configuration

Create the following configuration file:

```text
app/config.php
```

Example configuration:

```php
<?php

$config = [];

$config['directus_url'] = 'https://admin.woofya.com/';
$config['directus_token'] = 'YOUR_DIRECTUS_TOKEN';

$config['default_email'] = 'example@email.com';

$config['email'] = !empty($_GET['email'])
    ? $_GET['email']
    : $config['default_email'];
```

> **Important:** Never commit production credentials or API tokens to the repository.

## Running the Application

Start the PHP development server.

```bash
php -S localhost:8000
```

Open the application in your browser.

```text
http://localhost:8000/app/progress.php
```

To test a different user locally:

```text
http://localhost:8000/app/progress.php?email=user@example.com
```

## Project Structure

```text
Owner-Progress-Reports/
├── app/
│   ├── challenge-progress.php
│   ├── goal-progress.php
│   ├── journal.php
│   ├── leaderboard.php
│   ├── progress.php
│   ├── includes/
│   └── config.php
├── assets/
├── css/
├── js/
└── README.md
```

## Current Release

The current release includes:

* Complete implementation of all five dashboard pages
* Live Directus API integration
* Dynamic activity and progress visualisations
* Challenge streak tracking
* Mobile-first responsive design
* Configurable local development environment

## License

This project is licensed under the MIT License.
