---
description: >-
  Welcome to the Mountain Clinic application documentation! This guide will walk
  you through setting up the project, understanding the system structure, and
  configuring the environment for smooth use.
---

# Getting Started

## Overview

The mountain clinic system is built in Laravel and is designed to help paramedics and administrators manage health checks for climbers, create health certificates, and handle post-check payments.

## Prerequisites

Before getting started, ensure you have the following installed:

* **PHP >= 8.1**
* **Composer** (for Laravel package management)
* **MySQL** (via XAMPP or any other MySQL service)
* **Node.js >= 16.x** (for front-end dependencies)
* **NPM** or **Yarn**
* **Credenstials Google**
* **Docker** (optional, for containerized development)

## Starting

1. Copy env file or create

```bash
cp .env.example .evn
```

2. Add Google Credenstials in .env file

<pre class="language-php"><code class="lang-php"><strong>GOOGLE_CLIENT_ID
</strong>GOOGLE_CLIENT_SECRET
</code></pre>

3. Airtable Credentials (airtable)

```
AIRTABLE_API_KEY
AIRTABLE_BASE_ID   
AIRTABLE_TABLE_NAME
```

4. Email Smtp

```
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=youremail@example.com
MAIL_PASSWORD="lcom jxkf krxj gtvf"
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="your-email@yourdomain.com"
MAIL_FROM_NAME="${APP_NAME}"
```

5. Database Mysql

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_react
DB_USERNAME=root
DB_PASSWORD=
```

6. Migrate Dataabase

```bash
php artisan migrate
```

7. Start Serve

```bash
php artisan serve
npm run dev
php artisan reverb:start
php artisan queue:work
```
