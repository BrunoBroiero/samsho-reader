# SamSho Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) · **Français** · [Italiano](README.it.md) ·
[Português (Brasil)](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Un mod de lecteur d'écran pour **SAMURAI SHODOWN** (2019 ; Steam, PC). Il lit les menus, l'histoire, les listes de commandes, les tableaux et le texte à l'écran avec le lecteur d'écran que vous utilisez déjà (NVDA, JAWS), dans la langue du jeu.

Par Bruno Broiero, avec l'aide de Claude.

## Ce qu'il fait

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

N'est pas lu :

- L'écran de félicitations à la fin de l'histoire est une image sans texte.
- Les salons et le chat en ligne n'ont pas été testés avec des adversaires.

## Installation

Il faut la version Steam pour PC de SAMURAI SHODOWN, Windows x64 et un lecteur d'écran en marche (NVDA ou JAWS). UE4SS, le chargeur de mods pour les jeux Unreal, est inclus dans le zip, dans la version qui fonctionne avec ce jeu.

Extrayez tout le contenu du zip dans `SamuraiShodown\Binaries\Win64` (sous Steam : `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`) : `dwmapi.dll`, le dossier `ue4ss` et ces README.

Lancez le jeu depuis Steam, pas depuis le .exe : sans Steam il démarre en anglais et hors ligne. Le mod dit « SamSho Reader » dès qu'il fonctionne ; si vous ne l'entendez pas, F8 nomme le lecteur d'écran trouvé. Aucun fichier du jeu n'est modifié.

Pour désinstaller, supprimez `dwmapi.dll` et le dossier `ue4ss`. UE4SS et PRISM, la bibliothèque qui parle au lecteur d'écran, ont leurs propres licences : voir `THIRD-PARTY.md`.

## Touches

Hors d'un combat :

| Touche | Manette | Effet |
|---|---|---|
| F1 | Stick droit gauche ou droite | Dit tout ce qui est retenu (une liste de commandes, un tableau, un résultat) |
| F2 / F3 | Stick droit haut / bas | Élément précédent / suivant de ce qui est retenu |
| F10 | Clic du stick droit | Change la notation des commandes (Normale, Arcade, Arcade simplifiée, FGC, FGC simplifiée). Le choix est enregistré |
| F4 | Clic du stick droit, quand rien n'est retenu | Lit la légende des boutons de l'écran (« 9 ou A Confirmer, 0 ou B Retour ») |

Dans un combat :

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

Toujours :

| Touche | Manette | Effet |
|---|---|---|
| F6 | L3 + R3 (les deux sticks pressés ensemble) | Éteint le mod et le rallume ; confirmé avec les mots du jeu pour activé et désactivé. Non enregistré : il démarre toujours allumé |
| F8 | | Nomme le lecteur d'écran utilisé |

## Ce que lisent F1, F2, F3 et le stick droit

Beaucoup d'écrans montrent plus que ce qui est sous le curseur : une liste de commandes, les scores d'un résultat, un tableau de records, une leçon. Le mod ne lit pas tout cela à l'arrivée : il le garde et le livre avec ces touches : F3 passe à l'élément suivant, F2 revient au précédent et F1 dit tout d'un coup. À la fin, F3 ne dit rien : c'est ainsi que l'on sait qu'il n'y a plus rien. À la manette, le stick droit fait de même : bas est F3, haut est F2, gauche ou droite est F1.

Ce qu'est un élément dépend de l'écran :

- **Liste de commandes** : chaque coup avec sa commande, dans la notation choisie avec F10 ou le clic du stick ; en changer répète le coup dans la nouvelle. En entrant, le personnage et la catégorie sont dits.
- **Tutoriel** : chaque phrase de l'explication et de la tâche, avec les entrées mises en mots ; le clic change aussi leur notation.
- **Résultat**, après un combat : la phrase du vainqueur est dite seule ; les scores attendent dans les touches, volontairement, pour que la phrase ne soit pas enterrée sous les chiffres.
- **Résultat de versus** : victoires, défaites, nuls, taux et points de chaque côté.
- **Données du joueur** : les tableaux de records et de classements, une ligne par élément ; à l'arrivée, le titre et la première ligne sont dits.
- **Légende des boutons** : sans rien de gardé, le clic du stick (ou F4) lit la légende des boutons de l'écran lui-même.

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

## Signaler un problème

Quittez le jeu normalement et envoyez `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log` : il enregistre ce que le jeu a affiché et ce que le mod en a dit, mot pour mot, donc inutile de noter ce que vous avez entendu. Indiquez l'écran et ce que vous attendiez d'entendre.

## Compilation

Le mod est en Lua, chargé par UE4SS ; rien n'est compilé sauf `prism_bridge.dll`, le petit module natif qui transmet la parole à PRISM et lit la manette (`native\prism_bridge\build.ps1`, nécessite MSVC). `python tools\package.py` construit le zip de la release depuis le dossier du jeu.

## Traductions

Ce README est publié dans toutes les langues du jeu. Seules les versions anglaise et espagnole ont été relues par un locuteur ; les corrections aux autres sont bienvenues. Le mod lui-même parle la langue du jeu : presque tout ce qu'il dit est le texte du jeu, et ses rares mots à lui (directions, noms de touches, « vie », « rage ») n'ont été vérifiés à l'oreille qu'en espagnol.
