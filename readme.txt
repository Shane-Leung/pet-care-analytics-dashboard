# Owner Progress Reports

## Overview

Owner Progress Reports is a mobile-first web application developed for Woofya to provide pet owners with data-driven insights into their pet's activity, wellbeing, and challenge progression. The application integrates with the Directus CMS to retrieve and visualise live data through an intuitive dashboard experience.

---

## Key Features

* Five user-facing dashboard pages:

  * Journal
  * Progress
  * Leaderboard
  * Challenge Progress
  * Goal Progress
* Directus API integration for live activity and mood data
* Dynamic progress visualisations using Chart.js
* Challenge and streak tracking
* Responsive mobile-first user interface
* Configurable local user login via email query parameter

---

## Technology Stack

| Category           | Technologies                       |
| ------------------ | ---------------------------------- |
| Frontend           | HTML, CSS, Bootstrap 5, JavaScript |
| Backend            | PHP 8                              |
| Data Visualisation | Chart.js                           |
| CMS / API          | Directus                           |

---

## Repository

**GitHub Repository**

https://github.com/woofya/Owner-Progress-Reports

**Production URL**

https://woofya.com/app/signin

> The production environment is currently unavailable.

---

# Getting Started

## Prerequisites

Ensure the following software is installed before running the project:

* PHP 8.0 or later
* Local web server (MAMP, XAMPP or VS Code PHP Server)
* Modern web browser
* Internet connection (required for Directus API requests)

---

## Installation

Clone the repository.

```bash
git clone https://github.com/woofya/Owner-Progress-Reports.git
cd Owner-Progress-Reports
```

---

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

> **Note:** Do not commit production credentials or API tokens to the repository.

---

## Running the Application

Start the PHP development server:

```bash
php -S localhost:8000
```

Navigate to:

```text
http://localhost:8000/app/progress.php
```

To test with a different user:

```text
http://localhost:8000/app/progress.php?email=user@example.com
```

---

## Project Structure

```text
Owner-Progress-Reports/
│
├── app/
│   ├── journal.php
│   ├── progress.php
│   ├── leaderboard.php
│   ├── challenge-progress.php
│   ├── goal-progress.php
│   ├── includes/
│   └── config.php
│
├── assets/
├── css/
├── js/
└── README.md
```

---

## Release Notes

Current release includes:

* Complete implementation of five dashboard pages
* Live Directus API integration
* Dynamic activity and progress visualisations
* Challenge streak tracking
* Mobile-first responsive design
* Configurable local user authentication

---

## Authors

Developed as part of the Woofya Owner Progress Reports project.
