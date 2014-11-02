## Méthodes d'authentification

[Brouillon]

### Authentification avec Persona

 1.  Persona, système authentification par Mozilla : [https://login.persona.org/](https///login.persona.org/)
 2.  Il suffit de renseigner une adresse e-mail et de l'inscrire sur Persona
 3.  Possibilité de laisser les flux visibles aux visiteurs

### Authentification HTTP

 1.  Ne laisse rien de visible
 2.  Pour Apache, basé sur un fichier .htaccess
    - Exemple de .htaccess pour un utilisateur "marie" à placer dans le répertoire de FreshRSS ou dans un répertoire parent :

	
	AuthUserFile /home/marie/repertoire/.htpasswd
	AuthGroupFile /dev/null
	AuthName "Chez Marie"
	AuthType Basic
	Require user marie


Plus d'informations dans [la documentation d'Apache.](http://httpd.apache.org/docs/trunk/howto/auth.html#gettingitworking)
