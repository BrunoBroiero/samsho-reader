# SamSho Reader

> Traduction non relue par un locuteur natif. Une erreur de mot vaut la peine d'être signalée.

Mod d'accessibilité pour **SAMURAI SHODOWN** (2019, Steam) : il rend le jeu lisible avec votre lecteur d'écran. Menus, options, sélection du personnage et du stage, sous-titres du mode histoire, tutoriel, liste des commandes, base de données, galerie, en ligne, résultats et chiffres du combat.

Presque tous les mots que vous entendrez sont ceux du jeu, dans la langue où il est réglé. Les rares mots que le jeu n'a pas (directions des commandes, noms des touches, « vie », « rage ») sont traduits dans les onze langues du jeu.

Auteur : **Bruno Broiero**. Réalisé avec Claude.

## Prérequis

- SAMURAI SHODOWN pour Steam (Windows).
- Un lecteur d'écran en marche : NVDA ou JAWS. Le mod parle via PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), le chargeur de mods pour les jeux Unreal. Il est inclus dans le téléchargement, dans la version qui fonctionne avec ce jeu (expérimentale, 21 septembre 2026) : rien à récupérer à part.
- Une manette XInput (type Xbox) est facultative, mais le mod est conçu pour elle.

## Installation

1. Téléchargez le `SamShoReader-x.y.z.zip` le plus récent depuis la page Releases.
2. Extrayez tout son contenu dans `SamuraiShodown\Binaries\Win64\` (le dossier du jeu ; sous Steam : `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`) : `dwmapi.dll`, le dossier `ue4ss` et les README.
3. Lancez le jeu **depuis Steam** (pas depuis le .exe : sans Steam il démarre en anglais et hors ligne).
4. Au chargement, le mod dit « SamSho Reader ». Si vous ne l'entendez pas, appuyez sur F8 : il nomme le lecteur d'écran trouvé.

## Touches du mod

| Touche | Manette | Effet |
|---|---|---|
| F1 | Stick droit gauche ou droite | Dit tout ce qui est retenu (une liste de commandes, un tableau, un résultat) |
| F2 / F3 | Stick droit haut / bas | Élément précédent / suivant de ce qui est retenu |
| F10 | Clic du stick droit | Change la notation des commandes (Normale, Arcade, Arcade simplifiée, FGC, FGC simplifiée). Le choix est enregistré |
| F4 | Clic du stick droit, quand rien n'est retenu | Lit la légende des boutons de l'écran (« 9 ou A Confirmer, 0 ou B Retour ») |
| F7 | | Arrête la voix |
| F6 | L3 + R3 (les deux sticks pressés ensemble) | Éteint le mod et le rallume ; confirmé avec les mots du jeu pour activé et désactivé. Non enregistré : il démarre toujours allumé |
| F8 | | Nomme le lecteur d'écran utilisé |
| Ctrl + Échap | | Coupe la voix |

Les flèches, Entrée et Retour arrière appartiennent au jeu, pas au mod.

## Pendant le combat

Rien ne parle tout seul : le combat s'entend déjà. Le stick droit demande le chiffre voulu :

| Stick droit | Dit |
|---|---|
| Gauche | Vie des deux côtés : « vie 71%, 80% » (votre côté d'abord) |
| Haut | Rage : « rage 41%, maximale » |
| Bas | Rounds gagnés : « ROUNDS 1, 0 ». En Survie, Contre-la-montre et Ironman, vos victoires d'affilée |
| Droite | Le chrono du round |
| Clic | Tout |

Clavier : F2 vie, F3 rage, F10 rounds, F1 tout.

En Survie, Contre-la-montre et Ironman, seul votre côté est dit.

## La liste des commandes et ses notations

Dans le jeu, une commande est une rangée d'images : flèches, boutons, un « plus », des conditions. Le mod les transforme en mots et, comme chaque joueur arrive à une liste de commandes d'un endroit différent (la salle d'arcade, les forums, ou aucun des deux), il propose cinq façons de les dire. F10 ou le clic du stick droit en change, et le choix est enregistré. La même commande, quart de cercle avant et coupe forte, dans chacune :

| Notation | Ce qu'on entend |
|---|---|
| Normale | bas, diagonale bas avant, avant plus Coupe forte |
| Arcade | quart de cercle avant, Coupe forte |
| Arcade simplifiée | quart de cercle avant, C |
| FGC | 2 3 6, Coupe forte |
| FGC simplifiée | 2 3 6, C |

- **Normale** dit chaque direction avec son mot. La plus longue, et celle qui ne suppose rien.
- **Arcade** nomme la figure : quart de cercle, demi-cercle, dragon punch et leurs inverses. C'est ainsi qu'on dit les commandes à voix haute.
- **FGC** utilise les chiffres du pavé numérique, la notation de la communauté : 6 est avant, 2 bas, 3 la diagonale bas avant ; toujours face à droite.
- Les variantes **simplifiées** remplacent les noms des boutons par les lettres de la borne : A coupe légère, B moyenne, C forte, D coup de pied.

Comment la lecture a été pensée, car une image dit par sa forme des choses que les mots doivent dire à voix haute :

- Une diagonale est une seule entrée, donc elle s'appelle « diagonale » : « bas, diagonale bas avant, avant ». Dit « bas, bas avant, avant », on ne distingue plus une entrée de deux.
- Deux boutons dessinés collés se pressent ensemble, donc ils sont reliés par « plus » dans toutes les notations.
- Une condition que le jeu dessine autour du nom du coup (« pendant ~ ») est dite une fois, pas en deux moitiés.
- Une condition comme « répétez » est dite après les boutons concernés : « avant plus Coupe légère, répétez » — comme on le dit, pas comme c'est dessiné.
- Les noms des boutons et des conditions sont les mots du jeu, pris dans la légende de sa propre liste de commandes ; les directions, les figures, « plus » et « ou » sont ceux du mod, dans les onze langues.
- « Ou » prend plusieurs formes dans le jeu (deux boutons au choix, deux commandes, une liste) ; toutes sont dites avec le même mot.

La liste se parcourt avec le stick droit (haut et bas, coup par coup ; gauche ou droite, en entier) ou avec F2, F3 et F1. À l'entrée, le mod dit le combattant et la catégorie (« SHIKI, COUPS SPÉCIAUX »), puis chaque coup comme « nom, condition s'il y en a : commande », par exemple « Elysium Halo : avant, bas, diagonale bas avant plus Coupe légère ou Coupe moyenne ou Coupe forte ».

## Ce qui est lu

- Le menu principal et tous les sous-menus, avec la description de chaque entrée.
- Options : jeu, affichage, son (volumes en %), langue et sous-titres, configuration des boutons (chaque action avec sa touche ou son bouton).
- Sélection du personnage, y compris aléatoire, costumes et couleurs ; sélection du stage ; attribution des côtés en Versus.
- Histoire : sous-titres et dialogues, déblocages, épilogue et générique.
- Tutoriel : consigne, tâche et message final, avec les touches en mots.
- Liste des commandes : chaque coup avec sa commande dans la notation choisie ; parcourue avec le stick ou F2 / F3.
- Pause et réglages de l'Entraînement.
- Base de données : profil, classements personnels, registres généraux.
- Galerie : films, illustrations, voix et musique, avec leurs onglets et pages.
- En ligne : classements, écrans de combat classé et libre, listes de fantômes du Combat fantôme.
- Résultats : la réplique du vainqueur est lue seule ; le score est retenu et se demande avec le stick ou F1.
- Bannières de déblocage et avis.

## Ce qui n'est pas lu

- L'écran de félicitations à la fin de l'histoire est une image sans texte.
- Les salons et le chat en ligne n'ont pas été testés avec des adversaires.

## Langues

Le mod parle la langue du jeu. Ses propres mots n'ont été vérifiés à l'oreille qu'en espagnol ; dans les autres langues ils sont traduits sans relecture par un locuteur. Un mot faux est un bug qui mérite d'être signalé.

## Notes

- Le mod ne modifie aucun fichier du jeu.
- UE4SS est l'œuvre de l'équipe RE-UE4SS, sous licence MIT ; `prism.dll` et `tolk.dll` viennent de [PRISM](https://github.com/ethindp/prism), sous MPL 2.0. Voir `THIRD-PARTY.md`.
- Pour désinstaller, supprimez `dwmapi.dll` et le dossier `ue4ss`.
- Le code source du mod n'est pas encore public ; il le sera une fois le mod rodé par l'usage. Le téléchargement est libre d'utilisation.
