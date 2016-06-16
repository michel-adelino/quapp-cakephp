# Quapp — Backend API

Backend service for **Quapp**, a tournament management platform used to organize and run multi-day sports events. This application exposes a REST API consumed by mobile apps and web clients, handling match scheduling, live scoring, rankings, and event administration.

Built with **[CakePHP](https://cakephp.org) 5.2**, the official PHP rapid development framework.

## Features

- **Tournament management** — Years, days, rounds, groups, and teams
- **Match scheduling** — Automated scheduling patterns and playoff brackets
- **Live scoring** — Match events, score calculation, and ranking updates
- **PDF exports** — Match sheets, rankings, and field schedules via mPDF
- **Push notifications** — Device token registration for mobile clients
- **REST API** — JSON endpoints for iOS and Android applications

## Technology Stack

| Layer | Technology |
|-------|------------|
| Framework | [CakePHP](https://cakephp.org) 5.2 |
| Language | PHP 8.2+ |
| Database | MySQL / MariaDB |
| PDF generation | [mPDF](https://mpdf.github.io/) |
| Testing | PHPUnit 11 |
| Static analysis | PHPStan |

## Requirements

- PHP 8.2 or higher
- PHP extensions: `gd`, `gmp`, `intl`, `mbstring`, `pdo_mysql`
- Composer 2.x
- MySQL or MariaDB

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd quapp-cakephp
```

### 2. Install dependencies

```bash
composer install
```

### 3. Configure the application

Copy the local configuration template and adjust it for your environment:

```bash
cp config/app_local.example.php config/app_local.php
```

Set your database credentials, security salt, and other environment-specific values in `config/app_local.php`.

### 4. Set up the database

Import the schema and seed data as required for your deployment. SQL scripts are available under `config/schema/` and `src/Controller/sql/`.

### 5. Run the development server

```bash
bin/cake server -p 8765
```

The API will be available at `http://localhost:8765`.

## Development

```bash
# Run the test suite
composer test

# Check coding standards
composer cs-check

# Run static analysis
composer stan

# Run all checks (tests + coding standards)
composer check
```

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
