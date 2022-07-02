# Plugin netro (beta)

# Description

Ce plugin vous permet de piloter votre équipement d'arrosage netro dans Jeedom.

# Limitations

- Les capteurs sont pris en compte. Cependent, n'ayant pas de capteurs en ma possession, aucun test réel n'a pu avoir lieu.
- Dû a une limitation de l'API de netro, lorsque l'on souhaite arreter un arrosage, TOUS les arrosages en cours sont arretés. Cependant le plugin est pret pour l'évolution de l'API, et indique la zone qu'il souhaite arreter.
- Netro n'autorise que 2000 appels par jours. N'abusez pas du bouton "Synchroniser" sous peine d'épuiser ce quota pour la journée.

# Configuration

## Configuration du plugin

Une fois le plugin installé et activé, il faut renseigner la clefAPI. Cette clé est en réalité le numéro de série de votre appareil netro.

Validez ensuite la configuration pour que le plugin récupére la configuration de votre appareil et de vos zones.

En cas de modification de vos équipements, vous devez relancer une synchronisation manuellement depuis l'écran du plugin via le bouton "Synchroniser".

Si vous possédez des capteurs, vous devez cocher la case correspondante dans la configuration.

## Configuration de l'équipement

Il est possible de rapporter la météo auprés de votre appareil netro. Le plugin ne prends en charge que le plugin **Meteo France**.

Il suffit d'aller sur votre équipement netro et de choisir l'équipement meteoFrance que vous souhaitez utiliser.

La mise à jour se fera chaque matin.

# Récupération des données

Vous pouvez forcer la récupération de toutes les données en cliquant sur le bouton "Synchroniser" dans l'écran du plugin.

## cron 
L'état de l'arrosage est récupéré toute les minutes.

## cron10
Les informations des capteurs sont récupérées toutes les 10 minutes

## cronHourly
Les informations des prochaines programmations sont récupérées toutes les heures

## cronDaily
L'envoi de la météo est faite 1x par jour, tout comme la mise à jour de l'humidité de chaque zone, cette donnée étant calculée quotidiennement par netro.

