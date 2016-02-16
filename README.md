## Installazione

	1. eseguire `composer install`
	2. creare il database
	3. in `app/config/parameters.yml` configurare coerentemente alle proprie impostazioni
	4. eseguire il restore del database a partire dal file dump.sql oppure dalla root lanciare il comando `php bin/console doctrine:schema:update --force`
 	6. configurare apache (vedere il file di config sotto)

 ## Configurazione Apache

 ```
 <VirtualHost phptest.local:80>
	ServerAdmin webmaster@localhost

	DocumentRoot /home/carmelo/Sites/PHPTest/web
	<Directory /home/carmelo/Sites/PHPTest/web/>
		AllowOverride All
        Require all granted
        Allow from All
	</Directory>


	ErrorLog ${APACHE_LOG_DIR}/error.log

	# Possible values include: debug, info, notice, warn, error, crit,
	# alert, emerg.
	LogLevel warn

	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

```

## Hosts

	Modificare il file hosts in modo che "phptest.local" punti a localhost


## Test

	visitare phptest.local

