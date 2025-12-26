<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>

# Laravel Filament

Panduan singkat untuk menyiapkan dan menjalankan project Laravel + Filament ini.

## Persyaratan

- PHP 8.x
- Composer
- Node.js & npm (opsional untuk build asset)
- Database (MySQL / SQLite / PostgreSQL)

## Langkah setup

1. Clone repository

	```bash
	git clone https://github.com/justrahyan/laravel-filament.git
	cd laravel-filament
	```

2. Install dependency PHP

	```bash
	composer install
	```

3. Salin file environment dan generate app key

	- Di Git Bash / Linux / macOS:

	  ```bash
	  cp .env.example .env
	  ```

	- Di Windows Command Prompt:

	  ```cmd
	  copy .env.example .env
	  ```

	Kemudian:

	```bash
	php artisan key:generate
	```

4. Atur konfigurasi database pada file `.env`, lalu jalankan migration

	```bash
	php artisan migrate
	```

5. Buat akun admin Filament

	- Secara interaktif:

	  ```bash
	  php artisan make:filament-user
	  ```

	- Contoh non-interaktif (ganti nama/email/password sesuai kebutuhan):

	  ```bash
	  php artisan make:filament-user --name="Admin" --email=admin@example.com --password=secret
	  ```

6. (Opsional) Pasang dan build asset frontend

	```bash
	npm install
	npm run build    # produksi
	npm run dev      # jika ingin hot-reload selama development
	```

7. Jalankan aplikasi

	```bash
	php artisan serve
	```

Akses aplikasi di `http://127.0.0.1:8000` dan masuk ke panel Filament dengan akun yang Anda buat.

## Repository asal

https://github.com/justrahyan/laravel-filament