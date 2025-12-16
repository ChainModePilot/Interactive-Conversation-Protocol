# Interactive Conversation Protocol

## 1. Définition du Projet

Interactive Conversation Protocol (ICP) est un protocole structuré pour décrire les significations directives. Les clients peuvent combiner des significations directives en messages modulaires multimodaux reconnaissables par l'homme basés sur la structure de ce protocole.

**Positionnement Central** : Une forme de langage intermédiaire pour l'interaction homme-machine, essentiellement une représentation textuelle structurée d'un graphe de concepts, que nous appelons "Conception Annotation" (Annotation de Conception).

## 2. Pourquoi ce Projet a été Créé

### ❓ Problèmes à Résoudre

Nous devons faire face à la réalité : pendant une période considérable, la façon d'interagir avec les utilisateurs est déterminée par les développeurs côté client (ou entreprises). Sous la plupart des modèles commerciaux existants, la participation de l'utilisateur à l'interaction est la base de la valeur du produit et de la rentabilité, comme le nombre d'utilisateurs actifs et les revenus publicitaires. Personne ne peut forcer les côtés clients à ouvrir des permissions suffisantes, permettant à l'IA d'exécuter des opérations complètement sans intervention humaine.

Si l'IA est suffisamment intelligente, les humains n'ont vraiment pas besoin de commencer depuis la page d'accueil à chaque fois. Par conséquent, nous pouvons voir que le dialogue homme-machine devenant l'interface d'interaction principale de la prochaine génération est presque devenu un consensus.

Cependant, les défauts naturels de l'expressivité du langage naturel, initialement espérés pour être compensés par des interactions bien conçues, sont maintenant remplacés par des boîtes de dialogue. Les limitations des boîtes de dialogue sont immédiatement exposées :

#### (1) Perte de la Fonction Indicative du Curseur

Les formes d'interaction passent du mode "écran + opération de focus" au mode de langage naturel. Les opérations de focus traditionnelles sont réalisées via des claviers, des souris et des écrans tactiles, offrant une indication précise. L'interaction en langage naturel apporte les impacts suivants :

- **Perte de Précision Indicative** : La difficulté d'expression et de compréhension augmente, et l'ambiguïté grandit, ce que nous appelons l'"effet de perte de curseur".
  > Par exemple, lorsqu'un utilisateur dit "supprime ça", le système a des difficultés à déterminer à quel objet spécifique "ça" fait référence, tandis que les interfaces traditionnelles peuvent localiser avec précision via des clics de souris.

- **Efficacité Limitée de l'Expression d'Information** : L'expression d'information purement vocale est inefficace, et l'avantage de la saisie vocale se reflète principalement dans les scénarios d'expression mot par mot.
  > Par exemple, lorsque vous voulez agrandir une miniature, vous devrez peut-être dire "agrandir" ou taper "agrandir", tandis que l'interaction traditionnelle ne nécessite qu'un simple clic.

- **Exigences Élevées pour l'Expression Linguistique** : L'interaction en langage naturel impose des exigences élevées sur les capacités d'expression linguistique des utilisateurs, créant des difficultés dans l'interaction homme-machine.
  > Par exemple, les utilisateurs qui ne sont pas doués en expression linguistique peuvent être incapables de décrire précisément leurs besoins, conduisant à des écarts de compréhension du système, tandis que les interfaces traditionnelles abaissent le seuil d'expression grâce à des éléments visuels comme les boutons et les menus.

- **Faible Efficacité de Lecture d'Information** : La lecture de flux de texte et la lecture vocale sont moins efficaces que la lecture d'information structurée.
  > Par exemple, lorsque le système utilise la voix pour diffuser une longue liste de données, les utilisateurs doivent écouter toute la liste pour trouver des informations cibles, tandis que les interfaces traditionnelles permettent aux utilisateurs de scanner et localiser rapidement via des formes structurées comme des tableaux et des cartes.

- **Contraint par les Tours de Dialogue** : Les interactions contraintes par les tours de dialogue ne sont pas conviviales pour les opérations continues rapides.
  > Par exemple, lorsque les utilisateurs doivent effectuer plusieurs opérations en continu, ils doivent attendre que chaque tour de dialogue se termine avant de passer à l'étape suivante, tandis que les interfaces traditionnelles peuvent cliquer rapidement sur plusieurs boutons en succession pour compléter des opérations par lots.

#### (2) Débordement de Fragmentation d'Information

La structure d'information de streaming des conversations manque d'organisation, contrairement au logiciel traditionnel qui organise l'architecture d'information en unités de page, construisant des hiérarchies de présentation d'information visuellement conviviales à travers des interfaces graphiques visuelles. Cela mène aux problèmes dérivés suivants :

- **Difficulté d'Isoler Différentes Informations** : Les flux d'information continus dans une seule conversation rendent difficile de distinguer les frontières entre différents sujets, et même plusieurs sujets complètement non liés peuvent être mélangés.
  > Par exemple, un utilisateur demande d'abord "aide-moi à vérifier la météo de demain" dans une conversation, puis demande "comment va le progrès de ce projet", et ensuite demande "recommande quelques bons livres". Ces sujets complètement non liés sont mélangés, rendant difficile de localiser et réviser rapidement.

- **Explosion de Sessions Zombie** : Lorsque l'information est artificiellement isolée à travers des sessions, l'information dans les sessions est pliée dans des boîtes noires avec des sessions comme unités, devenant éventuellement des sessions zombie en raison de la faible visibilité.
  > Par exemple, les utilisateurs créent plusieurs sessions comme "lié au travail", "notes d'étude", "liste de courses", mais chaque session n'a que des messages dispersés. Au fil du temps, ces sessions sont oubliées et deviennent des sessions zombie qui ne peuvent pas être utilisées efficacement.

- **Incapable de Gérer Multi-dimensionnellement** : L'information similaire dispersée à travers d'innombrables sessions ne peut pas être organisée car l'information ne peut pas être gérée le long d'une dimension spécifique.
  > Par exemple, les utilisateurs ont demandé sur "tutoriel Python", "tutoriel JavaScript", "tutoriel React" et d'autres ressources d'apprentissage dans différentes sessions, mais ne peuvent pas les voir et les gérer uniformément le long de la dimension "ressources d'apprentissage", et ne peuvent rechercher que session par session.

- **Manque d'Objets Indicables** : L'information se dissout dans l'information de texte, et lorsque nous devons nous référer à quelque chose, il n'y a pas d'objet spécifique auquel se référer.
  > Par exemple, lorsqu'un utilisateur dit "optimise cette proposition à nouveau", "cette proposition" n'est qu'un paragraphe dans le flux de texte sans identification et structure indépendantes, rendant difficile pour le système de localiser et opérer avec précision.

#### (3) Différences Significatives dans les Interfaces Homme-Machine à Travers Différents Terminaux

Plus de dispositifs terminaux à l'avenir seront pilotés par des Agents, correspondant à la perception humaine à travers des écrans, caméras, microphones, haut-parleurs et autres dispositifs pour compléter l'interaction homme-machine. Cependant, différents terminaux ont des différences inhérentes dans leurs caractéristiques physiques, et il est impossible d'utiliser forcément le même mode d'interaction. Cela crée des difficultés dans l'intégration de l'IA :

- **Déconnexion des Médias** : Lorsque la structure d'information renvoyée par l'IA est hostile aux terminaux, cela causera inévitablement une perte ou une confusion dans l'expression d'information. Inversement, la structure d'information fournie par les terminaux n'est pas nécessairement conviviale pour l'IA.
  > Par exemple, une visualisation de données complexe initialement conçue pour un tableau de bord à grand écran est directement "lue" par la voix sur un haut-parleur intelligent, rendant presque impossible pour les utilisateurs d'établir une cognition globale ; inversement, une seule ligne d'information d'invite sur une montre intelligente peut difficilement porter complètement les sémantiques complexes que l'IA s'attend à exprimer.

- **L'IA Manque de Maîtrise des Caractéristiques des Terminaux** : Pour améliorer l'expressivité, les humains utilisent souvent plusieurs logiciels et terminaux pour démontrer dans des contextes complexes ou lors de l'expression de logique complexe. L'IA semble seulement savoir comment "parler".
  > Par exemple, lorsqu'un chef de produit présente une proposition, il montrera des diapositives, dessinera des diagrammes de structure sur un tableau blanc et cliquera sur des opérations sur des pages de démonstration ; tandis que l'IA actuelle ne peut souvent expliquer qu'avec un long texte ou une chaîne de voix, rendant difficile d'utiliser les capacités des terminaux comme la projection, l'annotation et l'animation pour améliorer l'expression.

- **Écart Entre Virtuel et Réalité** : Le contexte (ou contexte) actuellement utilisé par l'IA est basé sur des connaissances prédéfinies et mémorisées, tandis que le contexte dans les scénarios réels est souvent dynamique et lié à l'environnement réel.
  > Par exemple, l'IA peut "se souvenir" des profils personnels et des conversations historiques des utilisateurs, mais il est difficile de percevoir en temps réel que l'utilisateur est assis dans une salle de conférence, feuilletant quelle page d'un document papier, ou pointant vers quel tableau d'affichage physique, donc incapable de faire des instructions et des suppléments naturels basés sur des situations sur place comme un assistant réel.

### 💡 Idées d'Amélioration et Objectifs

Auparavant, le travail principal des chefs de produit était de concevoir des interfaces et des flux d'opération faciles à apprendre et à utiliser. Avec le support de l'IA, les utilisateurs n'ont plus besoin d'apprendre les interfaces d'interaction logicielle et la logique d'opération. L'IA a la capacité de fournir aux utilisateurs uniquement les informations nécessaires basées sur les questions et instructions des utilisateurs, et les utilisateurs n'ont besoin que d'opérations d'intervention minimales.

Cependant, tant que les utilisateurs eux-mêmes interviennent, il y a des problèmes avec la convivialité de l'interaction, la précision et l'efficacité. Interactive Conversation Protocol joue un rôle précisément au point de contact homme-machine :

#### Amélioration du Pouvoir Expressif du Langage Naturel (Humain → IA)

Améliorer le pouvoir expressif ici fait référence à l'amélioration du langage naturel. Pour compenser les problèmes mentionnés ci-dessus (perte d'indication du curseur, débordement de fragmentation d'information et différences dans les interfaces homme-machine à travers différents terminaux). Au moins le traitement suivant peut être fait sur le langage naturel original :

- **Marquage de l'Information Exprimée** : Marquez l'information qui nécessite un traitement spécial. Le traitement spécial mentionné ici comprend l'utilisation d'information structurée, l'assemblage d'interfaces, l'exécution de programmes auxiliaires, etc. Vous pouvez l'imaginer comme prendre des notes en encerclant des points sur un morceau de texte. En termes de forme de marquage, nous nous référons à Markdown, utilisant des caractères spéciaux pour représenter des significations spécifiques, tandis que l'explication et le déclenchement des fonctions auxiliaires se réfèrent au principe d'annotation dans le développement Java. Grâce à cette méthode, nous pouvons compléter le ton de la parole, indiquer ce qui est important, ce qui nécessite des formes de présentation spéciales et ce qui nécessite des pré-opérations (telles que l'authentification visible uniquement pour soi-même) dans le contenu expositif original.
  > Par exemple, lorsqu'un utilisateur dit "aide-moi à organiser les tâches de cette semaine", marquant légèrement les dates, priorités et personnes responsables dans la phrase, l'IA peut directement générer une liste de tâches vérifiable au lieu de simplement retourner un texte descriptif.

- **Ajout d'Information de Contexte** : Complétez l'information virtuelle nécessaire et l'environnement du monde réel dans l'information narrative pour reproduire la situation réelle du locuteur. Les interfaces d'interaction traditionnelles préétablissent souvent des informations de contexte optionnelles dans l'interface pour capturer les intentions précises des utilisateurs à partir de clics simples, tandis que le langage naturel nécessite d'organiser un texte long pour décrire complètement le contexte. En complétant des informations de contexte telles que le temps, l'emplacement, l'état de l'appareil et l'identité du participant dans le protocole, l'IA peut comprendre plus précisément la sémantique réelle de "ici et maintenant".
  > Par exemple, lorsqu'un utilisateur dit seulement "réserve un restaurant que Marry aime à proximité", complétez l'emplacement, les préférences budgétaires et les commandes historiques comme informations de contexte. L'application des informations de contexte est très large, et nous discuterons des scénarios spécifiquement plus tard.

- **Traduction en Langage Intermédiaire Standard** : Après le traitement de l'information originale (ajout d'annotations et d'informations de contexte), pour permettre une interprétation complète et précise, un système d'identification de données convenu est nécessaire. Pour s'adapter à l'expressivité de tous les terminaux, ce système d'identification peut être construit sur des spécifications JSON, fournissant des tableaux de paramètres et des structures convenus. De cette façon, les IAs à divers points de réception peuvent mobiliser tous les terminaux disponibles pour montrer une expressivité maximale et reproduire la signification complète de l'exprimant.
  > Par exemple, une phrase "envoie ce passage au groupe de projet et fais confirmer tout le monde avant la fin du travail aujourd'hui" est finalement traduite en une structure JSON standard contenant le corps du message, la liste des destinataires, la date limite et la configuration du bouton de confirmation. Les outils de chat, les backends Web ou les applications mobiles peuvent tous rendre leurs interfaces adaptées respectives en conséquence.

#### Interface Personnalisée à la Demande (IA → Humain)

Notre prémisse est que les gens préféreront interagir avec l'IA par "parler", ce qui est le moyen le plus proche de la communication humaine. Par conséquent, les gens trouveront de plus en plus gênant de trouver les interfaces fonctionnelles dont ils ont besoin en cliquant. Les informations et interfaces dont les gens ont besoin devraient être directement poussées aux "yeux" des utilisateurs. Pour atteindre cet effet, les points de réception devraient avoir certaines capacités d'interprétation :

- **Interprétation du Langage Intermédiaire** : Puisque le langage intermédiaire est au format JSON, tous les points de réception peuvent lire la sémantique complète, évitant au moins la déconnexion dans la réception d'information.
  > Par exemple, les mêmes données de langage intermédiaire d'une "demande de révision de rapport de dépenses" peuvent être rendues comme une interface à grand écran avec des tableaux et des aperçus de pièces jointes sur le bureau, n'afficher que des informations clés et deux boutons (approuver/rejeter) sur mobile, tandis que les haut-parleurs intelligents peuvent lire des résumés et attendre une confirmation vocale.

- **Construction Dynamique d'Interfaces de Messages** : Basé sur un contexte complet et des annotations, choisissez la solution la plus conviviale pour l'interaction et assemblez dynamiquement une interface interactive avec une hiérarchie d'information (bien sûr, les annotations incompatibles avec les terminaux peuvent également être ignorées). Cette interface n'est pas nécessairement une information multimodale en lecture seule, mais peut également être un corps de mini-programme interactif.
  > Par exemple, lorsque l'IA comprend "c'est une collecte d'information", elle peut automatiquement insérer une petite carte de formulaire remplissable dans l'interface de chat au lieu d'avoir les utilisateurs répondre aux questions une par une en texte brut.

- **Reproduction du Contexte** : Avoir la capacité d'indiquer ou de contrôler certains éléments dans le contexte. Cela nécessite généralement de mobiliser plusieurs applications ou dispositifs terminaux. Nous avons vu que la perspective à la première personne peut être reproduite à travers des caméras sur des lunettes, la perspective à la troisième personne peut être servie par des drones compagnons, et la projection ou les icônes VR peuvent pointer vers une certaine position sur des objets physiques... et ainsi de suite.
  > Par exemple, dans un scénario de maintenance à distance d'appareil, l'IA peut mettre en évidence la position des vis qui doivent être démontées dans le champ de vision AR de l'ingénieur tout en affichant simultanément des diagrammes de circuit et des instructions d'étape sur un grand écran, permettant au "contexte" d'être reproduit conjointement à travers plusieurs terminaux.

#### ❗️❗️ Note Spéciale : Le Langage Intermédiaire est-il Vraiment Nécessaire ?

Beaucoup de gens pensent que le langage intermédiaire n'est pas réellement nécessaire, généralement pour deux raisons :

(1) À long terme, AGI a la capacité de "lire entre les lignes" et de comprendre les intentions implicites des utilisateurs. Il n'est pas nécessaire de traiter artificiellement le langage naturel inutilement juste pour aider l'IA à mieux comprendre.

(2) Concevoir des interfaces d'interaction conviviales pour les humains est également le devoir d'AGI à l'avenir, et l'IA peut même concevoir une interface d'interaction exécutable spécifiquement pour chaque interaction. Par conséquent, il est encore plus inutile de traduire les mots de l'IA dans un langage intermédiaire.

Nous avons quand même finalement conçu le protocole ICP dans le système iFay. Nous avons les 3 préoccupations suivantes et croyons qu'elles sont difficiles à résoudre à court terme, nous avons donc choisi de concevoir un langage intermédiaire de style annotation :

(1) Le Contrôle de l'IA sur l'Environnement n'est pas si Grand

Généralement, les gens comparent l'interaction humain-IA à la communication entre une personne et un assistant. Ils pensent qu'un assistant intelligent ajustera activement les conditions environnementales pour atteindre de bons effets de communication, comme allumer les lumières quand il n'y a pas assez de lumière ; faire des marques sur les parties importantes des documents. Mais les permissions et capacités des assistants ne leur permettent pas toujours de tout faire, comme lorsqu'un bâtiment perd soudainement de l'électricité et ne peut pas jouer des diapositives de présentation.

Par conséquent, une approche plus prudente est de préparer tous les matériaux nécessaires et d'adapter la présentation (ou la laisser au gestionnaire de propriété). C'est comme apporter tous les matériaux pour rencontrer un client. Si le client a une salle de conférence, si les diapositives de présentation peuvent être jouées, ou si les rapports papier doivent être consultés, c'est décidé par l'autre partie.

(2) L'IA et les Humains Peuvent Ne Pas Être Si Proches

Parce que le contrôle de l'IA sur l'environnement est limité, l'IA ne comprend pas vraiment la signification humaine dans de nombreux cas. C'est comme pointer vers un ensemble de données sur une diapositive et demander à l'IA : "Qu'est-ce que cette information signifie ?" En fait, l'IA ne sait pas où vous pointez. Idéalement, un équipement de capture de mouvement serait nécessaire pour dire à l'IA cette information. Vous pouvez également imaginer un autre scénario : un patron tient une réunion à huis clos, et après qu'elle se termine, dit à l'assistant : "Suis les résolutions de la réunion." À ce moment, l'assistant n'a pas réellement obtenu des informations de première main, mais plutôt des procès-verbaux de réunion organisés par un enregistreur de réunion. Les procès-verbaux de réunion sont similaires à l'information traitée par le langage intermédiaire.

Par conséquent, dans de nombreux cas, l'information explicitement fournie par les humains n'est pas suffisante pour le jugement. À ce moment, des informations de contexte doivent être complétées, mais ce n'est pas l'autorité d'une IA spécifique.

(3) Il Peut Ne Pas Y Avoir d'AGI Universel du Tout

L'IA future rencontrera définitivement les mêmes problèmes de division du travail que la société humaine. Il y aura des IAs individuelles (similaires à iFay) et des IAs avec des fonctions publiques sociales (similaires à coFay). Il y aura inévitablement des limites de permissions entre elles.

Il est difficile pour nous de prédire si dans l'écosystème IA futur, la responsabilité de l'IA est seulement de traiter l'information fournie (entrée système), ou si l'IA devrait également être responsable de collecter activement plus d'"implications".

Nous choisissons donc une approche prudente. Nous supposons que l'IA ne traite que l'information connue. C'est juste que cette information passe par un flux de traitement à chaque fois, et cette action de traitement peut être complétée par un logiciel, un dispositif terminal ou une IA. C'est également une pratique très mature dans les solutions techniques d'ingénierie actuelles, comme utiliser un navigateur pour accéder à un site web, où le serveur peut apprendre une partie de l'information de contexte de l'utilisateur.

### 🌟 Vision

ICP (Interactive Conversation Protocol) vise à construire une forme de langage intermédiaire entre les humains et les machines, réalisant une communication bidirectionnelle efficace, précise et riche entre les humains et les machines :

#### Humain → Machine : Réplication Complète de la Signification et du Contexte Exprimés

- Capturer la signification et le contexte exprimés par les humains de la manière la plus complète possible
- Transformer le langage naturel et les intentions d'interaction en éléments structurés que les machines peuvent comprendre avec précision
- Préserver la précision de l'interaction et les informations contextuelles

#### Machine → Humain : Assemblage Dynamique de Méthodes Interactives

- Intégrer les annotations de concepts avec le contexte actuel
- Assembler dynamiquement les méthodes d'interaction les plus appropriées basées sur les capacités des dispositifs et les préférences de l'utilisateur
- Soutenir la présentation d'information multi-perceptuelle (texte, voix, vision, toucher, odorat, etc.)

