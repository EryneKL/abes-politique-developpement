# Documentation

La documentation d�un logiciel est indispensable car elle permet de :

* donner une vue d'ensemble de l'int�r�t et de l'usage d�un logiciel
* reprendre plus ais�ment le code d�velopp� par un autre programmeur
* retrouver plus facilement comment le logiciel a �t� structur�
* partager le logiciel avec d�autres programmeurs : ce point est essentiel lors de la publication d�une API

On distingue trois types de documentation : 

* __La documentation � l�usage des utilisateurs__
* __La documentation � l'usage des d�veloppeurs__
* __La documentation � l'usage des administrateurs__

# __La documentation � l�usage des utilisateurs__

* Elle explique comment prendre en main l'application. On y retrouve la description des fonctionnalit�s, des interfaces... exemple : http://documentation.abes.fr/aidestar/accueil/

* Les nouvelles applications d�velopp�es � l'Abes privil�gient une architecture qui s�pare la partie interface utilisateur de la partie serveur qui peut �tre interrog�e ind�pendamment. Cette partie serveur API est document�e au format openAPI qui d�crit chaque service. Cette documentation s'adresse donc plut�t aux d�veloppeurs qui veulent utiliser l'API.

https://swagger.io/docs/specification/about/ d�crit la sp�cification openAPI. Des outils permettent de g�n�rer automatiquement du code client � partir de cette description. Elle est accessible sous format brut (ex : https://item.sudoc.fr/api/v2/api-docs) ou via une pr�sentation en html.

# __La documentation � l'usage des d�veloppeurs__

Nous identifions le besoin de deux types de documentation : 

## Une documentation d�crivant l�architecture et la conception

Il ne s�agit pas de d�crire de mani�re exhaustive et syst�matique chaque d�tail de l'application, mais plut�t de donner une vue d'ensemble, de d�crire les �l�ments indispensables � la compr�hension de la structure de l�application. Nous pouvons utiliser le formalisme UML et ses principaux type de diagrammes. Les diagrammes UML peuvent �tre g�n�r�s avec diff�rents �diteurs, par exemple http://www.umlet.com.

* le diagramme de classes donne une vue statique des �l�ments
* le diagramme de s�quence montre les interactions entre les objets
* le diagramme de d�ploiement situe l�application dans son contexte
* un diagramme des flux entrants et sortants permet de d�crire la communication et les d�pendances de l�application
* il faut aussi inclure les informations jug�es utiles pour faciliter la prise en main de l'application par un nouveau d�veloppeur : 
     * l�adresse du d�p�t Github ou Gitlab
     * les �l�ments de configuration
    * les projets associ�s � l'application

Cette documentation peut prendre la forme d'un document texte ou d'un wiki.

## Une documentation technique

Nous utilisons la Javadoc pour documenter le code Java. Les blocs sont r�dig�s et ajout�s en en-t�te de chaque classe et m�thode de l�application. Il faut d�crire ce que fait la m�thode, quels sont les param�tres en entr�e et en sortie et quelles erreurs sont susceptibles d'�tre renvoy�es.
Il faut aussi ajouter des commentaires dans le code lui-m�me lorsqu'ils sont n�cessaires � la compr�hension du traitement. 
Lors de chaque release g�n�r�e � partir d'un job Jenkins, la Javadoc est transform�e en pages HTML qui sont publi�es sur un site en interne. Ainsi, on conserve la Javadoc relative � chacune des releases de nos applications.
Un site en externe sera bient�t disponible pour publier la Javadoc des applications dont le code source est d�pos� sur Github.

Pour le Javascript et le PL/SQL, les commentaires sont actuellement inclus dans le code.

# __La documentation � l'usage des administrateurs__

Pour certaines applications, des t�ches de maintenance doivent �tre r�alis�es r�guli�rement (mise � jour de donn�es par exemple). L'ex�cution de ces t�ches peut prendre la forme de lancement de traitements via une interface utilisateur ou via des outils accessibles en lignes de commande. Ces t�ches doivent �tre d�crites ainsi que leur mode d'ex�cution.
