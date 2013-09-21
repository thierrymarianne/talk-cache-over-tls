Cache + SSL / TLS
========================

Sujet présenté lors du sfPot parisien du 17 septembre 2013 à la Pépinière 27

[Présentation au format HTML](http://cache-ssl-tls.weaving-the-web.org/show#Cover)

[Présentation au format PDF](https://github.com/thierrymarianne/cache-ssl-tls/blob/master/CACHE_SSL_TLS.pdf)

[Événement Meetup](http://www.meetup.com/afsy-sfpot/events/139415812/)

[Bonnes pratiques selon SSLLabs](https://www.ssllabs.com/projects/best-practices/)

[Serveur de test SSLLabs](https://www.ssllabs.com/ssltest/index.html)

[Association francophone des utilisateurs de Symfony](http://afsy.fr/)

Générer votre clef Diffie-Hellman à l'aide de cette commande (ça peut prendre un certain temps)

    openssl dhparam -out /etc/ssl/private/dh4096.pem -5 4096

A faire
========================

Configuration de DNSSEC pour mise en place de TLSA

Changelog
========================

A la suite de la conférence de Benjamin Sonntag ayant lieu le 20 Septembre 2013 à la Cantine,
les points suivants ont étés revus :
* Réduction de la liste des chiffrements proposés par SSL proxy
* Aucune version de SSL servies (dont SSL v3.0), seules les versions de TLS sont proposées
* Ajout du paramètre de clef pour Diffie-Hellman ([Perfect Forward Secrecy](http://news.netcraft.com/archives/2013/06/25/ssl-intercepted-today-decrypted-tomorrow.html))
* Ajout de l'entête HTTP Strict Transport Security dans la configuration du SSL proxy (nginx)
 (en plus de ne l'avoir eu auparavant dans les fichiers de configuration exemple séparés uniquement)