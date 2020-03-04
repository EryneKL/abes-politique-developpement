# Environnement de d�veloppement int�gr�

Un Environnement de D�veloppement Int�gr� permet de manipuler des outils de programmation depuis une interface graphique, il doit assister les d�veloppeurs dans toutes les phases de la r�alisation d�une application : d�finition, conception, programmation, d�bogage, compilation, test, maintenance et production de documentation. Il doit �galement orienter le d�veloppeur vers de bonnes pratiques.

## Java

Pendant longtemps, les d�veloppeurs de l'Abes ont utilis� les IDEs Eclipse et Netbeans. Il s'est av�r� que pour faciliter l'entraide, il �tait pr�f�rable que nous utilisions tous le m�me IDE. Ceci permet de fortement capitaliser sur son fonctionnement, de le prendre en main et de ma�triser sa configuration.

Jusqu'en 2018, notre choix s'�tait port� sur l'�diteur Eclipse. 
Nous packagions l'IDE en pr�-configurant les modules et plug-ins conform�ment aux pr�conisations de notre politique de d�veloppement (sonarlint etc.) 

Nous avons test� l'�diteur en ligne Eclipse Che.
Eclipse Che est une solution prometteuse mais pas encore m�re. L�IDE est dans le cloud o� l�environnement d�ex�cution est embarqu� dans l�espace de travail du d�veloppeur. L�environnement de travail du d�veloppeur est donc stock� sur un serveur dans un container Docker.
Une  version b�ta a �t� lanc�e en juillet 2016. Nous avions mis cette solution de c�t� tout en suivant son d�veloppement. En effet, Eclipse Che n'est pas aussi complet qu'un �diteur client lourd.

Depuis 2018, nous utilisons d�sormais Intellij IDEA qui nous parait �tre l'�diteur le plus performant.

Le d�marrage rapide pour travailler sur un projet consiste �:
* faire un clone du projet depuis Gitlab ou Github
* choisir le SDK appropri� (dans les project settings, project, project SDK)

## Javascript

Le code VusJs et plus g�n�ralement Javascript peut �tre �dit� via Intellij. Nosu utilisons �galement Webstorm et VSCode. 

## PL/SQL

SQL Developer reste l'�diteur favori en ce qui concerne l'�dition de code PL/SQL. Le versionning n'est pas contre pas g�r� via l'�diteur. Pour versionner le code, nous mettons en oeuvre deux solutions suivant les applications : soit un batch r�cup�re les proc�dures stock�es, fonctions etc. et les versionne dans Gitlab r�guli�rement, soit les codes PL/SQL sont copi�s dans un r�pertoire "sql" de l'application et sont versionn�s avec le code de l'application.
