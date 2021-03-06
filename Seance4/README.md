# UML SEANCE 3 : Diagramme de séquence

## Qu'est ce le Diagramme de séquence ?

<p>Ce diagramme permet de décrire les interactions entre les acteurs et le système</p>

<p>L'intérêt principal de ce diagramme est qu'il montre le déroulement chronologique d'un scénario (contrairement au diagramme d'activité)</p>

<h2>Lien avec le diagramme de cas d'utilisation</h2>

<p>Tandis que le diagramme de cas d'utilisation présente une vue externe du système, le diagramme de 
séquence expose les interactions entre les objets afin de réaliser un cas d'utilisation.

Un diagramme de séquence est donc également réalisé à partir de la description d'un cas d'utilisation.
</p>

<h2>Principaux éléments du diagramme de séquence</h2>
<table>
<tr>
<th>Élément</th>
<th>Représentation UML</th>
</tr>
<tr>
<td>La ligne de vie représentant la chronologie</td>
<td><img src="../img/ligneVie.PNG" alt="ligne de Vie" ></td>
</tr>
<tr>
<td>Message asynchrone (qui n'attend pas de retour)</td>
<td><img src="../img/messageAsynchrone.PNG" alt="Message Asynchrone" ></td>
</tr>
<tr>
<td>Message synchrone (qui attend un retour)</td>
<td><img src="../img/messageSynchrone.PNG" alt="Message Synchrone" ></td>
</tr>
<tr>
<td>Message de retour (après un message synchrone)</td>
<td><img src="../img/retourExplicite.PNG" alt="Message de retour" ></td>
</tr>
<tr>
<td>Message réflexif (message interne à l'objet : méthode privée)</td>
<td><img src="../img/messageReflexif.PNG" alt="Message réflexif" ></td>
</tr>
</table>
Les messages sont des actions (appels à des méthodes réalisant l'action)
 
<p>Pour compléter et décrire le mieux possible les scénarios, le diagramme de séquence permet également
de représenter des conditions et des boucles</p>

<table>
<tr>
<th>Élément</th>
<th>Représentation UML</th>
</tr>
<tr>
<td>Boucle (permet de répéter plusieurs fois une séquence d'actions)</td>
<td><img src="../img/loop.PNG" alt="loop" ></td>
</tr>
<tr>
<td>Condition (permet d'effectuer une ou plusieurs actions si une condition est remplie)</td>
<td><img src="../img/if.PNG" alt="Condition" ></td>
</tr>
</table>
On peut également ajouter des paramètres en message en les inscrivant entre les parenthèses.

Tous ces messages sont les plus utilisés et peuvent suffir à décrire correctement le déroulement
des scénarios. cependant, il existe d'autres interactions que l'ont peut décrire dans le diagramme de séquence
par exemple, il est possible de créer ou de détruire une instance.

<h2>Le système enrichi</h2>

Il permet d'ajouter des éléments supplémentaires :

<ul>
<li>Les actions internes au système (par exemple la vérification des identifiants de l'utilisateur)</li>
<li>les déroulements alternatifs</li>
<li>les enchainements en cas d'erreur</li>
</ul>

Pour ce faire, on utilise entre autre des messages réflexifs (méthodes privées) et des références
 
## Diagramme de séquence décrivant le cas d'utilisation : émettre avis (énoncé Sens Critique)

<p>Voici le diagramme correspondant à la description du scénario du cas d'utilisation émettre avis</p>
<p>Ce UC permet à un critiqueur de donner son avis sur une oeuvre</p>
<p>Tout d'abord, voici la description du UC :</p>
<img src="../img/descriptionUc.PNG" alt="description" >

<p>Et voici le diagramme de séquence correspondant :</p>
<img src="../img/diagSequence.png" alt="diagramme de séquence" >

<p></p>
<h2>Réponses aux questions relatives à: <a href="https://mbf-iut.i3s.unice.fr/doku.php?id=2016_2017:s2:td:td_sequences">cet énoncé</a>
 </h2>
<h3>Quels sont les acteurs</h3>
Client et Hotel 
<h3>Comprenez-vous le scénario?</h3>
Oui, un client souhaite réserver un hôtel, il fait donc une recherche, le système lui retourne les hotels disponibles afin qu'il puisse sélectionner celui de son choix
<h3>Quelle structure correspond à une boucle?</h3>
"Loop"
<h3>à une condition?</h3>
"Opt"
<h3>Quel objet est créé?</h3>
L'objet "reservation"
<h3>Qui exécute le comportement de “réserver une chambre à une date donnée” ?</h3>
la classe Hotel Chain
<h3>Qui répond à “available(date)” ?</h3>
L'objet hotel
<h3>Qui fait appel à “available(date)” ?</h3>
L'objet hotelChain fait appel à la méthode  “available() de l'objet hotel
<h3>Qui exécute “lookForAvailableHotels(Place)” ?</h3>
l'objet hotelChain
<h3>Que devez-vous modifier pour que les “éléments” clef correspondent à des classes ?</h3>
il faut changer le stéréotype de l'élément


<h2>Conclusion de la séance</h2>
Le diagramme de séquence est très utile pour décrire graphiquement les interactions et la chronologie 
d'un cas d'utilisation. Il doit être défini dans un contexte précis, pour un cas d'utilisation précis.
Il offre beaucoup de possibilités et complète les diagrammes vus précédemment (diagramme de classe et de cas d'utilisation)
