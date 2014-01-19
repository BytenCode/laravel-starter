laravel-starter
===============

#Laravel Starter Project


This is a starter project for Laravel based projects.

It includes:

* Laravel 4
* CodeSleeve / Asset-Pipeline
* Catarlyst / Sentry 2

Included Assets
* jQuery 2.0.3
* Twitter Bootstrap 3.0.3

#Usage:

##Get Code

	git clone https://github.com/BytenCode/laravel-starter.git

##Install Dependecies

	composer update

##Laravel Configurations

Add the folowing lines to your app/config/app.php under providers:

	'Codesleeve\AssetPipeline\AssetPipelineServiceProvider',
	'Cartalyst\Sentry\SentryServiceProvider',

And this one under Aliases

	'Sentry' => 'Cartalyst\Sentry\Facades\Laravel\Sentry',

Run Sentry's migrations

	php artisan migrate --package=cartalyst/sentry

Opcionaly define your own configurations for these packages:

	php artisan config:publish codesleeve/asset-pipeline
	php artisan config:publish cartalyst/sentry

##Get started on your project