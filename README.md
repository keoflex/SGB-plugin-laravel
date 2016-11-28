# SGB-plugin-laravel
This project is a plugin for the laravel framework that helps admins manage Google Drive

        Composer
        Node JS

## Google Setup
In your google account, create a service account.  This app will make use of the service account to make API calls to your google account.  Download the .p12

## Setup Steps
        Create the .env file in the root dir /
        Create these directories if they do not exist
                /storage
                        /app
                        /debugbar
                        /logs
                        /framework 
                                /cache
                                /sessions
                                /views
        Make sure the apache user can write to the files in /storage
        Initialize the database with the file /sql/schema.sql
         
        Update the .env file with the information from your google account.
                Google Domain Name
                Google Admin User for the Google Domain
                Google service account name
                Path to the .p12 file


## sample .env file
	APP_ENV=dev
	APP_DEBUG=true
	APP_KEY=someuniquekey

	DB_HOST=localhost
	DB_DATABASE=db
	DB_USERNAME=user
	DB_PASSWORD=pw

	ADMIN_EMAIL=you@domain.com
	DEV_EMAIL=you@domain.com

	google_client_id=xxx.apps.googleusercontent.com
	google_domain_name=domainname.com
	google_admin_user=admin@domainname.com
	google_service_account_name=xxx@yyy.iam.gserviceaccount.com

	; the Web app uses this one
	google_service_account_key_file=/etc/domainname.p12
	; the Cron file uses this one
	google_service_account_key_file2=/share/sites/dumas/etc/domainname.p12
