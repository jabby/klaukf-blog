---
layout: post
title:  "Mon Devoxx 2022 à moi !"
author: fanny
categories: [ event ]
tags: [ devoxx ]
image: assets/images/devoxxFR2.png
---

*ENFIN !! je crois que c'est le mot qui résume le plus l'attente (3 ans quand même !), les retrouvailles, les allers et venues dans les couloirs Neuilly et Paris, l'arrêt aux stands, les discussions avec les copains et les copines... Que ça fait du bien !
Retour en images et en texte de cette spéciale 10 ans de DevoxxFR...

## Mardi 19 avril : prépa physique et mentale

Cela fait deux jours que le stress gagne chacun de mes organes vitaux et m'empêche de correctement dormir et manger.
Il y a quelques jours j'apprends que je donnerai ma conférence "Rendez l'agilité aux développeurs et développeuses !" en amphi bleu. Le grand amphi cleu. L'ENORME amphi bleu. Il n'y a plus qu'à espérer que les spots m'aveuglent suffisamment pour que je n'y voie rien !

Après un faux départ (oubli de chargeur de portable, c'eut été dommage...), en route pour Paris depuis Saint Pierre des Corps (à 4km de Tours 😜).

On retrouve les potos pour partager un repas sympathique et on oublie la pression, car commme dirait un grand homme, qui vit avec moi : "La pression ça se boit !"

## Mercredi 20 avril : tranquille !

### Ce que l'on retrouve

Par rapport aux autres éditions, il y a beaucoup de choses qui n'ont pas changé et qu'on aime retrouver (d'ailleurs, on vient surtout pour ça !) : les gilets rouges qui assurent, les "oh tiens tu es là toi ? ça va ? la famille ? imotep !", 

Il y a aussi la partie stand que j'affectionne particulièrement : il y a trois ans, lors de l'édition 2019, je cherchais, l'âme en peine, une solution à mon avenir professionnel. CV à la main, j'avais fureté sur les stands et énormément échangé sur la vision des équipes de dev alors. C'est là que l'arrivée de 10 techs en sweat Apside m'avait tapée dans l'oeil. Une année chargée d'émotions donc, qui me fera toujours aimer échanger avec les boîtes présentes.

### Ce qui change

Non mais vous avez vu ce stand d'accueil ?? Cette bannière magistrale, cette organisation impeccable, ces gilets rouges au top !
![Le site d'accueil pour retirer les pass]({{ site.url }}{{ site.baseurl }}/assets/images/devoxxFR.png)
C'est un bonheur de venir retirer son pass la veille !

Bien-sûr, n'ayant pas eu la chance de pouvoir participer à la session 9 3/4 , c'est ma première aventure Devoxx masquée. L'année prochaine je viens avec un loup ! (le masque, pas l'animal, ça ne serait pas très pratique...)

Les couloirs sont jonchés de photos souvenirs des années précédentes, depuis 2012 : je peux vous dire que personne n'a pris une ride !

### La révolution (wasm) est incroyable parce que vraie - Philippe CHARRIERE et Laurent DOGUIN

![Laurent et Philippe sont prêts]({{ site.url }}{{ site.baseurl }}/assets/images/wasm4.png)

Première université de 3h pour ce mercredi matin.
Ce que j'apprécie avec ces deux grands messieurs, c'est que ce sont des gens intelligents qui ne vous font pas sentir bêtes (merci à eux !) : je comprends quand ils m'expliquent quelque-chose 😁

Ca parle Flash, ActiveX, applets Java, bref, ça ravive des souvenirs lointains.
On arrive au Javascript mais en termes de design et de graphisme, c'est à parfaire => qu'est-ce qui peut nous sauver ?
EMScripten avec asm.js ? joli essai.
WebAssembly !! le fameux wasm : on va régler les soucis des navigateurs, sans remplacer Javascript pour autant, ne confondons pas !
Il s'utilise partout, y compris sur JVM.

Wasm s'exécute partout : Javascript (navigateur et Node.js) GraalVM, runtimes...
et parle toutes les langues : C/C++, Rust, Golang, Swift... et se voit dédié certains langages : AssemblyScript et Grain par exemple.
Je vous invite à regarder la slide 35 qui récapitule tout bien => j'indiquerai le lien vers la présentation ASAP.

Ensuite nous passons à la partie démo, vous la trouverez dans la vidéo YouTube sur la chaîne DevoxxFR : à venir.
ça parle de pointeurs de mémoire (oups!), d'emojis 😉, d'accès au système d'exploit avec WASI (spoiler : jeu de mot pictural à suivre), wasmer, wasmtime, wasmedge... 

![WASI]({{ site.url }}{{ site.baseurl }}/assets/images/wasm5.png)

On passe un très bon moment : merci à tous les deux !

Pour suivre Laurent et Philippe sur twitter, ça se passe par là : [@ldoguin](https://twitter.com/ldoguin) et [@k33g_org](https://twitter.com/k33g_org)

![Nous sommes en salle Neuilly 252 AB et il y a beaucoup de monde]({{ site.url }}{{ site.baseurl }}/assets/images/wasm3.png)

### Architecturoplastie hexagonale d'un backend Node.js : Opération à coeur ouvert - Jordan NOURRY, Adrien JOLY et Julien TOPCU

Bienvenue à Shodopital, nos trois internes charcutent et décortiquent du code pour en tirer le plus de bénéfices possibles.
Première biopsie clean-codienne : on clarifie notre code !

![Les mains sont propres, on peut commencer l'opération dans le bloc]({{ site.url }}{{ site.baseurl }}/assets/images/nodejs1.png)

On précise nos paramètres, on refactore doucement mais sûrement, on reboote le patient (si ! si ! c'est possible !) et on redonne du sens pour éclaircir la compréhension du code.
Même les tests d'intégration présents sont piègeux ! et les changements en codebase ne sont pas trackés => comment faire ?

Non, on n'utilise pas un bistouri, on va casser l'ordinateur... Non, on va plutôt s'intéresser au comportement attendu des APIs et créer des approval tests. Et on teste régulièrement ! à chaque modification ! le pas à pas.
On supprime les undefined et les null.

Le nom des fonctions doit signifier ce que fait la fonction : on s'allège ainsi la charge mentale de relecture de tout le code pour le comprendre.

Enfin, on centralise le fonctionnel et sa complexité : on arrête de la disperser un peu partout dans notre architecture ! (à bon entendeur...)

Le but de l'architecture hesagonale, est donc d'inverser le sens de la dépendance entre la couche domain et la couche de persistence, normalement rencontré dans le modèle classique.

Controller ->use-> Domain <-use<- Persistence

Domain devient un hexagone où les objets métiers sont centralisés.

Pour suivre Jordan, Adrien et Julien, ça se passe par là : [@JkNourry](https://twitter.com/JkNourry) , [@adrienjoly](https://twitter.com/adrienjoly) et [@JulienTopcu](https://twitter.com/JulienTopcu)

![Nous sommes en salle Neuilly 252 AB et il y a beaucoup de monde.]({{ site.url }}{{ site.baseurl }}/assets/images/nodejs2.png)

Et n'oubliez pas, nous co-organisons, avec CraftsRecords et TADx, le Tremplin des speakers le 3 mai à Tours pour donner la chance à des speakers débutants de gagner une conférence au Camping des speakers, dans le Golfe du Morbihan les 9 & 10 juin 2022.
Inscriptions pour faire partie du public-jury du tremplin le 3 mai => [lien eventbrite]](https://www.eventbrite.fr/e/billets-le-tremplin-du-camping-des-speakers-306273120147)


### Rendez l'agilité aux développeurs et développeuses ! - votre humble serviteuse

Le palpitant accélère petit à petit depuis la fin de la dernière université (peut-être même pendant). Trop pour me concentrer sur une autre conférence.
248 inscrits sur l'application Devoxx, syndrôme de l'imposteur au max, je pense à mon premier jury de guitare classique quand j'étais au CP : même envie irresistible de monter sur scène mais pour faire une blague et repartir aussitôt.

J'attends sagement mon tour, entourée des personnes adorables (Stéphane en premier mais aussi Jérémy, Faustine, Corentin, Yann-Thomas, Olivier, Christophe, Thibault, et j'en oublie ! pardon...). Je passe dans les mains du technicien (adorable aussi), Adrien et Arnaud me rassurent à la dernière minute : merci à tous !

![Allez, il faut y aller !]({{ site.url }}{{ site.baseurl }}/assets/images/rendez1.png)

J'ai adoré la prise de risque, j'ai aimé préparer, répéter, partager, rencontrer des gens grâce à ce partage... Un grand merci aux organisateurs et aux membres du comité de sélection de m'avoir offert cette occasion unique !


### Créer & distribuer un plugin pour Kubernetes en quelques minutes ? Easy ! - Aurélie VACHE et Gaëlle ACAS

Grâce à une super organisation des talks, j'ai pu assister à cette présentation péchue et accessible pour nous autres communs des mortels !

![En place]({{ site.url }}{{ site.baseurl }}/assets/images/kube1.png)

Des gophers et une partie théorique plus tard (ou on se rend compte que l'important dans kubectl, ce n'est pas de savoir le prononcer, mais bien de l'utiliser !), place à la pratique : live-coding !!
La présentation est fun et accessible : on apprend autant qu'on passe un bon moment.
Le bon conseil : ne pas hésitez à partager ses trouvailles par des index à défaut de pouvoir l'ajouter dans le Krew index : tout est utile !

![Gaelle et Aurélie]({{ site.url }}{{ site.baseurl }}/assets/images/kube2.png)

Et pour les commandes ou plugins utiles et les bonnes pratiques : revisionnez à souhait la présentation (vidéo bientôt disponible en lien ici) ou référez-vous aux sketchnotes d'Aurélie sur le sujet (lien ici bientôt).

J'ai beau avoir déjà vu la présentation à la [TADx](https://www.tadx.fr) de février 2021 à distance et au JugSummerCamp de septembre 2021, je ne me lasse pas : Gaëlle et Aurélie sont à voir et à connaître absolument !

Pour suivre Aurélie et Gaëlle, ça se passe par là : [@aurelievache](https://twitter.com/aurelievache) et [@Gaelleacas](https://twitter.com/Gaelleacas)

Be jealous : j'ai un sticker collector !!
![Be jealous : j'ai un sticker collector]({{ site.url }}{{ site.baseurl }}/assets/images/kube3.png)


### Bilan de la première journée

Ouf ! sacrée journée ! je vais laisser la pression redescendre, participer au dîner des speakers, rencontrer encore plein de gens formidables, merci à toutes et tous !

![Sticker de speaker, et pas l'inverse]({{ site.url }}{{ site.baseurl }}/assets/images/repasspeak2.png)

On vous donne rendez-vous demain jeudi 21/04 à 20h pour le [BOF TADx](https://cfp.devoxx.fr/2022/talk/FIT-6322/Mais_au_fait_DevRel_c'est_vraiment_qu'un_lanceur_de_paillettes_%3F) - Tours Agile & DevOps experience à 20h autour de fabuleux DevRel !
(TADx, injustement non renommé PADx pour Paris Agile & DevOps experience pour l'occasion, mais j'aurai le dernier mot un jour...)

## Jeudi 21 avril : on recharge les piles !

DevoxxFR va enfin pouvoir commencer : mon estomac est dénoué ;-)
Beaucoup plus de monde à l'entrée, l'amphi Bleu se remplit en quelques minutes seulement.

### Première Keynote : les 10 ans de DevoxxFR !!!

Revival ! montée sur scène façon concert de rock : éclairage, fumée, et... rockstars !! Nicolas, Antonio et Zouheib nous partagent les coulisses de DevoxxFR, depuis sa germination, sa naissance, son annonce et son expansion !

![devoxxfr les 10 ans]({{ site.url }}{{ site.baseurl }}/assets/images/devoxx10ans1.png)

L'équipe entière monte sur scène et entonne un joyeux anniversaire des 10 ans des plus envolés : un grand merci pour tout ce que vous faites, vos partages, vos galères, votre fatigue mais toujours vos DevoxxFR pleins de succès ! Fière de vous avoir croisés et de faire un peu partie de l'aventure en tant qu'attendee depuis les 5 dernières sessions.

![devoxxfr les 10 ans]({{ site.url }}{{ site.baseurl }}/assets/images/devoxx10ans2.png)

A revoir absolument : les photos collectors !!!

Encore un grand merci !

### 10 ans de tech à travers le podcast Niptech - Benoît CURDY, Michael MONNEY et Baptiste FREYDT

Il existe des groupes qui fonctionnent parce qu'ils ont tout compris : partager dans la bonne humeur.
C'est exactement le cas de Niptech ! Au travers de leur rétrospective, de leur réussite, des aléas de la vie, des tentatices d'innovations, des retours aux valeurs sûres : on partage avec bonheur nos propres tentative de maintien de communauté, pour toujours plus lui apporter et la garder précieusement. Car oui : c'est un vrai plaisir de partager !

Merci à tous les trois !

![niptech sur scène]({{ site.url }}{{ site.baseurl }}/assets/images/niptech.png)

### Slow tech : il est urgent de changer le système - Frédéric BORDAGE

Présentation très claire et très concrète des solutions que l'on peut toutes et tous mettre en place au quotidien pour hacker le système et faire avancer la problématique de notre impact écologique.

On découvre la notion d'obégiciel : la croissance exponentielle du poids de nos utilisations logicielles. Il n'y a pas que la partie extraction de minerais ou de fabrication qui puise dans les réserves de notre belle planète encore bleue, mais pas pour longtemps.
On évoque l'éco-conception, mais surtout de la Slowtech.

Slow.tech  (low + high).tech

Le numérique étant une ressource non renouvelable car à notre rythme de consommation de matières premières, on ne pourra plus fabriquer d'ordinateur (le truc que je suis en train d'utiliser pour écrire ce blog...). Accepter de rendre son service moins hightech, c'est aussi accepter de le rendre plus accessible potentiellement : rendre plus simple l'accès aux informations.

Conclusion : concentrons-nous sur ce que la tech sert vraiment, et pour tout le reste, gardons notre bon sens !

Pour participer activement et aider, ça se passe ici : collectif@greenit.fr

### Comprendre les enjeux de consommation de ressource et d'énergie dans le secteur numérique - Quentin ADAM et Pierre BEYSSAC

On debunk sur les impacts écologiques de l'IT !
Pour cela, on découpe trois domaine :
- la fabrication, liée à l'extraction concrète des matières premières et de la nécessité de l'énergie
- le run, actuellement rapproché au réseau et au rapport Watt/Go
- la fin de vie, de plus en plus liée à la récupération

![Quentin et Pierre in stage]({{ site.url }}{{ site.baseurl }}/assets/images/ressourcenrj.png)

Concernant le run : le pilotage de la consommation mais aussi de la production, intégrer la notion de l'heure et de la localisation à la startégie de calcul, permettraient de corriger la marge d'erreur des calculs unitaires et communiqués actuels.

On compare la consommation des différents , mais aussi les pays, les secteurs économiques : on apprend plein de choses concrètes.

La morale est de prendre du recul sur les réels impacts : éteindre un composant électrique, ça peut être une bonne pratique, mais s'il y a risque de l'abîmer voire de le détruire (par baisse de température, par sur-intensité au redémarrage...) quitte à racheter ce composant et donc de le fabriquer... et donc de ré-extraire des matières premières...  réfléchissons et ne prenons pas tous les chiffres qui nous sont communiqués sur les réseaux ou via les médias comme argent comptant.

La métrique idéale qui nous permettrait de facilement nous positionner est beaucoup plus complexe que le simple Watt par Gigaoctet.

Concernant la fabrication, il ne faut pas ignorer le risque d'amoidrissement des matières premières. L'idée là est de se dire que pour chaque problématique de multiples solutions de contournement existe. Et que l'impact écologique étant un problème, il faut se pencher sur les solutions de contournement.

L'idée est de pérenniser nos utilisations : investir sur des objets qui tiennent dans le temps plutôt que de multiplier les achats d'objets de piètre qualité.
Cela me rappelle une discussion super intéressante avec un collègue, un jour où je me posais la question de revendre ma voiture essence encore en bon état pour une voiture neuve électrique, je me suis vue répondre : "la meilleure voiture est celle que tu n'achètes pas. Pousse ta voiture tant qu'elle fonctionne, et repose toi la question plus tard : peut-être alors qu'encore d'autres solutions apparaîtront entre temps".

Retenir : une mesure sans marge d'erreur, n'est pas une mesure.

Vous voulez en savoir plus ? bien-sûr je vous invite à aller voir la vidéo de retransmission mais aussi les émissions de Monsieur Bidouille (lien à venir).

Pour suivre Quentin et Pierre, ça se passe par là : [@waxzce](https://twitter.com/waxzce) et [@pbeyssac](https://twitter.com/pbeyssac)


###  Licences open source : entre guerre de clochers et radicalité - Pierre-Yves Lapersonne

Quelle est la meilleure ou la pire license opensource ? Pas facile.

![licences opensource]({{ site.url }}{{ site.baseurl }}/assets/images/licenseos.png)

Il y a différentes notions à prendre en comte : le droit d'auteur, le copyright, la non discrimination, les brevets...
Il existe MIT, BSD sur plusieurs versions, avec plus ou moins de conditions (citations, références...).

Comme c'est compliqué, notamment pour les brevets, il vaut mieux se référer à un juriste.
Là existe Apache 2.0.

Pour des licences LPL ou LGPL, il existe la notion de licence LIBRE, COPYLEFT, COPYLEFT faible, MOZILLA PUBLIC LICENSE 2.0, LGPL V3

Pour la licence GPL V3, il y a COPYLEFT FORT, GPL V3, AGPL V3

Bon à savoir : AppStore et iTunes d'Apple ne sont pas adaptées aux licences GPL, contrairement avec Google Play

Et puis, il y a les licences éthiques aujourd'hui, par l'Organisation for ethical source, imposant le non-nucléaire, le non-militaire, la non destruction de l'environnement, la non-violence de manière générale.

Pour faire bref : c'est compliqué ! et souvent les choix semblent radicaux et provoquent des réels cas de conscience.
Et c'est bien : cela fait se poser les bonnes questions et reflète les problématiques ambiantes qu'on n'aime pas trop mettre à jour.
Peu de procès et de jurisprudence pour le moment, du fait de la récence des licences, donc les ressources juridiques sont encore peu étoffées.

Je rajoute ma propre morale : on a tous un rôle à jouer dans l'éthique des entreprises, y compris quand on est développeuse ou développeur. Et là je vous conseille de re-visionner une des keynotes qui m'avait marqué à DevoxxFR en 2017 : De la responsabilité des ingénieurs d'Eric Sadin, à voir ici : https://www.youtube.com/watch?v=jpvMOIVU-Z4

Pour suivre Pierre-Yves, ça se passe par là : [@pylapp](https://twitter.com/pylapp) 

### Simplifiez vos revues de code avec le rebase intéractif - Sonia SEDDIKI

Une première pour Sonia, et en salle Maillot s'il vous plaît !

![c'est parti]({{ site.url }}{{ site.baseurl }}/assets/images/rebase1.png)

On parle amélioration de revue de code : pouvant être vue comme laborieuse, elle intervient souvent en fin de longue période de développement dnas un temps limité et donc avec peu de marge de manoeuvre pour corriger au besoin.
A cela s'ajoutent les différents niveaux de revue à vérifier pour augmenter la qualité et la clareté de merge request.

Condition : avoir une MR avec des commits clairs et cohérents. Intervient alors le rebase intéractif !

Commit du vendredi, TDD en faisant les tests en aval : on partage forcément des souffrances de tous les jours...

Grâce au "git rebase -i feature", on peut lister l'ensemble des étapes / commit, les modifier, les éditer, les différencier, les découper ... Les logs sont ainsi plus claires et parlantes. On peut ré-organiser l'historique des commits.

Pour re-rassembler des commits, pour encore plus de clarté, là encore une possibilité : fixup. On fusionne.

Et Squash ? Utilisé à la place de Fixup, il permet de conserver les messages en plus.

Attention : à faire sur vos propres branches ! pas des branches partagées ou dépendantes (encore moins sur main !!) dans le but de contrôler le périmètre géré. Si vous vous trompez : pas d'affolements ! on peut annuler avec un abort d'urgence qui revient au dernier état valide. Et les empilements de "git push" concurrents sont empêchés, ouf !

Très belle découverte : merci Sonia, et bravo !

![nous sommes en salle Maillot]({{ site.url }}{{ site.baseurl }}/assets/images/rebase2.png)

Pour suivre Sonia, ça se passe par là : [@sonia_seddiki](https://twitter.com/sonia_seddiki) 


### Dois-je migrer en Reactive et comment ? - Christophe JOLLIVET

Apside represent !
C'est dans un amphi bleu bondé que la conférence de Christophe commence.

![amphi bleu bondé]({{ site.url }}{{ site.baseurl }}/assets/images/reactif1.png)

On parle d'abord de requête en mode impératif pour bien comprendre l'apport du réactif : lorsqu'on envoie une requête à un serveur, le thread arrive, la requête met un certain temps à s'exécuter puis le thread est retourné avec la réponse. Ce temps peut être conséquent, notamment quand on multiplie le nombre de threads. Ce qui est alors avantageux avec réactif est que le thread lancé permet d'exécuter la requête, mais il est retourné dans le pool immédiatement, le libérant.

Passer en réactif pour aller plus vite est donc une erreur mais ça va vous permettre de scaler très vite.

Dans un flux réactif, on trouve un publisher et un subscriber. Et pas de pressure, il y a backpressure ! pour ne pas sur-solliciter le subscriber, on régule le rythme : plusieurs façons de faire, mais il s'agit d'une bonne pratique obligatoire si vous ne voulez pas tout casser !

![publiser et subscriber]({{ site.url }}{{ site.baseurl }}/assets/images/reactif2.png)

En termes de librairies, on est larges. Pour la présentation, c'est Spring qui est utilisé.
En nous aidant des marble diagrams, on s'y retrouve un peu mieux que l'énorme javadoc disponible.

La syntaxe peut nous perdre : on ne sait pas toujours la répartition des threads, on tatonne, mais c'est normal ! c'est comme tout : lancez-vous, testez et le métier viendra ;-)

On aborde ensuite WebMVC et WebFlux. On est vigilants aux imports, aux flux, aux monos : même si le code semble sensiblement identique de l'impératif, il y a ces modifications précieuses à apporter. On utiliser R2DBC en lieu et place de JDBC bloquant.

Mais attention : pas de pagination et, plus logique, pas de jointure autorisées : eh oui ! car qui dit jointure, dit blocage d'appel de requête ! On s'en sort cependant avec AfterConvertCallback, qui associe la jointure systématiquement, donc c'est tout ou rien.
Pas de fetch non plus en automatique : c'est à coder par nous-même côté Hibernate.

Autres petits oups : on doit veiller à travailler avec des flux non bloquants, et il y en a ! Dès lors qu'on va vouloir logguer par exemple, il va falloir être vigilant. Pour cela, il existe BlockHound qui nous permet de déterminer si un appel bloquant est détectée dans le code. Ca nous évite de lire avec nos petits yeux tout myopes les nombreuses lignes de code à vérifier !

Quand on est prêt à déployer en production, on peut continuer d'utiliser Actuator qui permet de récupérer les informations utiles et nécessaires pour satisfaire les bonnes pratique DevOps.

Alors, on migre ou pas là ?
Un grand oui si vous visez la scalabilité plus que la rapidité. La syntaxe est particulière et nécessite un peu d'apprentissage et d'habitude. En termes de persistence, on est limités mais les solutions telles que le NoSQL existent. Par contre c'est DevOps friendly.

![Christophe Jollivet]({{ site.url }}{{ site.baseurl }}/assets/images/reactif3.png)

J'ai adoré la présentation step by step en comparaison avec ce que l'on connait de l'impératif : cela permet d'appréhender facilement et rapidement les concepts du reactif.

Pour suivre Christophe, ça se passe par là : [@jollivetc](https://twitter.com/jollivetc) 

### Etre développeur : grandir et se développer - Gaëtan ELEOUET

"Etre développeur, ce n'est pas savoir coder.
Savoir coder, ce n'est pas être développeur."

![Gaetan en amphi bleu]({{ site.url }}{{ site.baseurl }}/assets/images/devgrand.png)

Le rôle du dévéloppeur ou de la développeuse n'est pas seulement de répondre à un besoin par du code, mais assurer un service pérenne et de manière qualitative. Il faut pour cela s'astreindre à aller au-delà du simple code : creuser la qualité, améliorer la communication des équipes. C'est ainsi que Jeff Kent, un des signataires du manifeste agile, propose 9 règles de callisthénie.

On parle agilité, craftmanship : des manifestes qui mettent en exergue des pratiques déjà existantes, notamment la boucle de feedback la plus rapide possible et qui permette de toujours plus améliorer les pratiques de chacun. Ont été évoqués les principes SOLID, les propriétés CUPID.

Pour grandir, les 25 millions de développeurs dans le monde, il faut se préoccuper de la communication.

La notion même d'expérience, de séniorité est de plus en plus complexe : le nombre de technos explose et il est de plus en plus difficile de maîtriser toute une stack technique. Alors on est déjà bien content lorque nous comprenons la stack. On n'est pas forcément un développeur ou une développeuse sénior arpès 6 ans d'expérience : on n'a pas forcément pu tout voir ou voir suffisamment de choses pour nous considérer comme sénior.

Eviter les pièges du super-héros, essayer d'agrandir sa zone de confort, expliquer le pourquoi on fait les choses, créer une culture véritablement bienveillante : autant de choses qui nous permettrons d'oser nous surpasser ou de tenter des nouveautés.

Pour suivre Gaëtan, ça se passe par là : [@egaetan](https://twitter.com/egaetan)

### Comment j'ai aidé ma fille à lire avec le machine learning - Vincent OGLOBLINSKY

Retour d'expérience : lors de l'apprentissage de la lecture, les enfants décortiquent les syllabes une à une. Un des outils magiques qui exitent est le digital. Le doigt quoi ! pointer son texte pour focuser son attention est une aide précieuse pour le déchiffrage.

Challenge : imaginer une solution qui aide à la lecture en déchiffrant une voix d'enfant alimentant une application web faisant marcher un speed-to-text like.
Rencontrer des orthophonistes a permis de comprendre les phases de l'apprentissage de la lecture afin de coller au mieux à l'habileté mentale du cerveau qui apprend.

![Vincent dans la salle Maillot]({{ site.url }}{{ site.baseurl }}/assets/images/lecture.png)

Le français, c'est pas facile : 26 lettres de l'alphabet, 36 phonèmes, 190 graphèmes associés... les combinaisons sont ultra-nombreuses !

Et le machine learning dans tout ça ? Il faut trouver des modèles de données en entrée de base, comprendre le fonctionnement du speed-to-text (donner du son court en entrée, puis traiter le signal pour ensuite dissocier la partie lexicale et le langage).
Mais la complexité de l'affaire est de s'adapter à la tessiture des voix d'enfants, pour lesquelles les datasets d'entrée sont beaucoup plus rares.

Deux possibilités de modèles :
- un modèle déjà entrainé, moins maitrisé mais existant
- un modèle à construire à partir de rien et donc avec besoin de beaucoup plus de données initiales pour pouvoir l'entraîner

C'est la première qui a été choisie, depuis tensorflow. Ajoutez du Python en local et déployez en javascript et ainsi le modèle pourra être utilisé dans le navigateur.
Pour la collecte, l'interface propose d'enregistrer le son, le vérifier (donc le ré-écouter) et d'envoyer le fichier natif pour les nettoyer, les raccourcir...

Ensuite, on entraîne le modèle, et ... on l'utilise ! on écoute en continu, on récupère la fréquence, on compare et on valide, ou pas !

A l'utilisation, l'enfant lit et sait visuellement si le déchiffrage est ok ou non.
L'utilisation est ludique et laisse des perspectives d'ouverture multiples.

Intéressé(e)s ? essayez vous même avec teachablemachine

Pour suivre Vincent, ça se passe par là : [@vogloblinsky](https://twitter.com/vogloblinsky)

### Accéder à mon cerveau par une API - Sébastien BLANC

ENORME ! une entrée en matière sonore, visuelle et tellement tordante !

![rock star]({{ site.url }}{{ site.baseurl }}/assets/images/cerveau1a.png)

On va parler interface homme machine : que ce soit avec un clavier, un stylo optique mais aussi la souris, la Wiimote, le gyromètre sur les iPhone...
Si on va plus loin, on peut parler de Interface cerveau-machine.
![rock star]({{ site.url }}{{ site.baseurl }}/assets/images/cerveau1.png)

"Il faut d'abord comprendre comment marche un cerveau, sachant que je suis un développeur J2EE."

Les zones du cerveau sont spécialisées et permette de déterminer ce qu'il pense.
Voici le streaming de cerveau de Sébastien :

![rock star]({{ site.url }}{{ site.baseurl }}/assets/images/cerveau2.png)

Et c'est plutôt très clair : cela indique qu'il est génial et que sa présentation est fait mouche.

Plusieurs types d'ondes existent :
- Delta : c'est quand on dort
- theta : lorsqu'on est en mode méditation
- alpha : quand on est en mode relaxation
- beta : quand on est focus
- gamma : on le saura un jour plus précisément qu'aujourd'hui peut-être

On utilise Docker / Kafka pour... voir les données du cerveau de Sébastien sur un topic Kafka, et ça... ça n'a pas de prix !
On teste le calm, le focus mais surtout on commence à réellement utiliser les cas d'application : en fonction de ces taux de calm ou de focus, on va pouvoir lancer des commandes particulières. Il n'en faut pas plus pour laisser libre court à l'imagintation de Sébastien pour la suite.

Il va construire un modèle et l'entraîner : mode deep learning ON via neurosity. Et on va parler Kinesis pour intéragir avec son cerveau.

Nouvel exemple : via Brainflow, qui peut se connecter aussi au casque.
Et enfin... tir de boulets de canon... par la pensée !!

BRAVO !

Pour suivre Sébastien, ça se passe par là : [@sebi2706](https://twitter.com/sebi2706)

### Jouer à Minecraft avec une IA générée par GPT-3 - Wassim CHEGHAM et Tiffany SOUTERRE

Quand on discute sur _Underscore_ on peut parfois se retrouver à se lancer dans des aventures impressionnantes mais tellement challengeantes ! 
Le POC présenté consiste à pouvoir donner des instructions au bot sous Minecraft via une intelligence artificielle (IA ou AI pour les english).

Après un rappel de ce qu'est le géniallissime jeu Minecraft, les NPC (non-player characters), on voit comment intéragir avec ces derniers grâce à OpenAI, GPT-3 qui, après un entraînement de folie, a donné Codex. Github Copilot lui, est capable de proposer des blocs de codes en fonction de ce qu'on souhaite faire faire à la fonction. J'aimerai clairement que ça existe pour les compte-rendus de réunions de 3h...

Bref, le joueur va donner une instruction, envoyée à Codex associée à un contexte.

On fait le tour du code, puis on passe à la partie démo, car nos deux speakers sont joueurs !



Vous êtes intéressé(e)s ? le code github sera open-sourcé ce soir 😇

Pour suivre Wassimm et Tiffany, ça se passe par là : [@manekinekko](https://twitter.com/manekinekko) et [@TiffanySouterre](https://twitter.com/TiffanySouterrej)


### BOF TADx - Mais au fait DevRel c'est vraiment qu'un lanceur de paillettes ?

Très bon moment passé à se poser la question : qu'est-ce qu'un DevRel ? un Developer advocate ? un Technical Account Manager ?
Plusieurs réponses différentes prouvent la richesse et la pluralité de ce qu'on met derrière ce rôle mais un point commun : le partage.
Servir la communauté, être "un membre actif positif" - Horacio Gonzales

Merci à toutes et tous !

![Les invités]({{ site.url }}{{ site.baseurl }}/assets/images/tadxbof1.png)
![on était bien en 242]({{ site.url }}{{ site.baseurl }}/assets/images/tadxbof2.png)
![les participants]({{ site.url }}{{ site.baseurl }}/assets/images/tadxbof3.png)

### BOF Duchess France

Très bon moment là encore, passé à échanger sur la multiplicité des profils, des parcours, des valeurs...
On parle syndrôme de l'imposteur (qui à mon sens ne doit pas totalement disparaître pour permettre de rester humble dans son partage), études, partage de connaissances auprès des étudiants et étudiantes, encouragements, mentoring, entraide, mixité... Merci !! Ce fut très précieux pour moi pour la fin de cette deuxième journée intense !

![le bof des duchess]({{ site.url }}{{ site.baseurl }}/assets/images/duchessbof.png)
