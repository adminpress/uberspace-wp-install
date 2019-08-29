# uberspace-wp-install
Shell Script um auf Uberspace7 auf die Schnelle ein neues Kundenentwicklungsprojekt mit WordPress auszurollen

## WP-Install
wp-install erzeugt ein Unterverzeichnis mit der passenden Domainbenennung im Webroot für die Installation von WordPress. Eine separate Datenbank für diese Installation wird erzeugt. Anschliessend wird WordPress in der aktuellsten Version geladen, die wp-config.php generiert und WordPress fertig eingerichtet. Lediglich die IPs (v4 und v6) müssen noch beim verwaltenden Nameserver hinterlegt werden um die Installation ansprechen zu können. Es empfiehlt sich, einen Wildcard-Eintrag im DNS für die fragliche Domain zu erzeugen, dann ist die Installation sofort ansprechbar.

## cleanup
Ein Script, das entstand um die Testläufe von wp-install wieder rückstandsfrei zu entsorgen

## ToDo
+ Automatismus, der aus der .my.cnf von uberspace das Datenbankpasswort ausliest und an die dbpass-Variable übergibt. Derzeit noch **hardgecodet** einzufügen, was natürlich ein **Sicherheitsrisiko** darstellt
+ Parameterübergabe von shortname und title und erst beim fehlen einer der beiden Parameter die interaktive Abfrage
+ komplett interaktiver Modus um alle Variablen abzufragen (Voreinstellungen liefern) und ggf. zu ändern