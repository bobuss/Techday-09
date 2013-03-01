# TechDay'09 : Debriefing

Le 21 Juillet 2010...

## Le techDay de Rémi

### release-4.12.00-rc1

    * 4408488 [CORE] Rename kfGuiNavigator to wkGuiNavigator(#3904).
    * 472ae57 [CORE] Use of helper for album pagination(#3904).
    * 0fe9ba5 [CORE] Use family id and informations instead of calculating index and looking in grade informations(#3904).
    * f3b0759 [CORE] Improve exceptions logs(#3910)
    * 8ee04ee [CORE] Update WkToolkitPlugin (#3913)
    * 9069def [CORE] Use Fql queries to retrieve users informations(#3924).
    * 8ae4518 [PINBA] Tell pinba informations about fql queries(#3929)


*Le 21/07/10 12:28, Rémi JANOT a écrit :*

    Go prod
    Rémi (Mode chef de projet confirmé par Cécile)

*Le 21/07/2010 12:36, Thomas Aebi a écrit :*

    Remi en CdP = Weka au Pole emploi

    Les bugs:
    - La box d'echange d'image sous la pub ne marche plus (le stream est "pas d'image...")
    - L'échange d'image ne marche plus (idem)
    - L'achat d'image ne marche plus (pack 3€ testé 5 fois, code invalide)

    On reparlera des évolutions de poste plus tard hein....

    Thomas

*Le 21/07/10 12:43, Alexandre RODIERE a écrit :*

    gg Thomas !!

    alx ..

*Le 21/07/10 14:19, Thomas Aebi a écrit :*

    En même temps c'était facile, avec Remi il faut toujours tester les achats !! ;)

*Le 21/07/10 13:38, Cécile BONNEHON a écrit :*

    Rémi : Dans mon bureau !




### release-4.12.00-rc2

    1 ticket de moins

    * 4408488 [CORE] Rename kfGuiNavigator to wkGuiNavigator(#3904).
    * 472ae57 [CORE] Use of helper for album pagination(#3904).
    * 0fe9ba5 [CORE] Use family id and informations instead of calculating index and looking in grade informations(#3904).
    * f3b0759 [CORE] Improve exceptions logs(#3910)
    * 9069def [CORE] Use Fql queries to retrieve users informations(#3924).
    * 8ae4518 [PINBA] Tell pinba informations about fql queries(#3929)


finalement, l'expression régulière et la condition de ratrapage du nom de la table était foireux dans #3929

### d'où la release-4.12.00-rc3

    * 4408488 [CORE] Rename kfGuiNavigator to wkGuiNavigator(#3904).
    * 472ae57 [CORE] Use of helper for album pagination(#3904).
    * 0fe9ba5 [CORE] Use family id and informations instead of calculating index and looking in grade informations(#3904).
    * f3b0759 [CORE] Improve exceptions logs(#3910)
    * 9069def [CORE] Use Fql queries to retrieve users informations(#3924).



*Le 21/07/10 13:47, Bertrand Tornil a écrit :*

    à ce rythme, le techday de Rémi va se résumer à
    "change the background color to pink"

*Le 21/07/10 14:28, Thomas Aebi a écrit :*

    Ok , goprod


## Le techDay de Bertrand

### release-4.12.01-rc1

*Le 21/07/10 14:51, Bertrand Tornil a écrit :*

    en cours, et à tester

    * f37612d [MEMCACHE] refactor the memcache class and use a static local cache (#3242)

*On Wed, Jul 21, 2010 at 3:06 PM, Bertrand Tornil <bertrand.tornil@cafe.com> wrote:*

    c'est en preprod...
    déjà testons ce que ca aurait pu casser

*Le 21/07/10 15:10, Rémi JANOT a écrit :*

    Y'a pas de ticket à moi, et j'ai pas dis go prod...
    Rémi qui assure ses arrières

*2010/7/21 Bertrand Tornil <bertrand.tornil@cafe.com> wrote:*

    étant donnée la stabilité de la preprod, c'est tout bon pour moi :)
    de toute manière, ca ne peut que se tester en prod.
    tu es prêt Vermeer ?
    B

*Le 21/07/10 15:14, Vermeer GRANGE a écrit :*

    +1

*Le 21/07/10 15:20, Thomas Aebi a écrit :*

    ***se liquéfie sur place****

*Le 21/07/10 15:22, Bertrand Tornil a écrit :*

    Pater Noster,
    Faite que cette prod marche,
    Ca éviterai que Thomas nous fasse une descente d'organe,
    Pensez à ses voisins de bureauLL
    Merci

*2010/7/21 Bertrand Tornil <bertrand.tornil@cafe.com> wrote:*

    normalement c'est passé
    j'en sais rien, j'ai plus accès à facebook

*2010/7/21 Vermeer GRANGE <vermeer@cafe.com> wrote:*

    Les résultats en images :

![Résultats Memcache][resultatsMemcache]

    le nombre moyen d'appel memcached par requete php descend donc d'environ 600 à 400. merci Bertrand!

    Autres améliorations notables de QoS :

![Résultats QOS][resultatsQOS]

    A noter qu'il n'y a aucune modification des appels facebook dûs à cette MEP.

    Toutes ces améliorations sont donc dues aux changements memcached ( -30% d'appels)

    Vermeer

    PS: La durée moyenne des requetes php est artificiellement basse en ce moment en raison de nombreuses requetes texte-alerte.php très rapides. C'est pourquoi j'évite de mentionner la durée moyenne des requetes, je préferre cibler des appels en particulier (index.php, ajax.php....)


*Le 21/07/10 16:48, Bertrand Tornil a écrit :*

    au passage, après quelques minutes, le patch a eu un autre effet intéressant, à savoir l'arrêt des saut dans la courbe des get_miss

![Résultats get_misses][get_misses]

*Le 21 juil. 2010 à 18:21, Bertrand Tornil a écrit :*

    pour terminer, je suis également assez fier des résultats sur :

![Résultats request time][req_time]

*Le 21/07/10 18:28, Laurent Letourmy a écrit :*

    Le résultat est en effet sans appel ! Félicitations.


## Le Techday de Choukri


    * 64d48bd [TECHDAY] Fix sql request for Super reward (#3943).

    -            'uid'=>$_REQUEST['uid'],
    +            'fbuid'=>$_REQUEST['uid'],


FIN du TechDay.

[resultatsMemcache]: resultatsMemcache.jpg
[resultatsQOS]: resultatsQOS.jpg
[get_misses]: get_misses.jpg
[req_time]: req_time.jpg
