# Data collection protocol

## Part 1

Trouver une vidéo de ruche avec la préscence de reine, retenir à quel moment celle-ci apparait.
- [Logiciel pour télécharger des vidéos youtube](https://ytdl-org.github.io/youtube-dl/index.html)

La télécharger, le logiciel peux aussi télécharger toutes les vidéos d'une playlist si besoin, puis extraire les **frames** 
sur [VLC](https://www.videolan.org/vlc/index.fr.html)

- [Tuto pour extraire des frame sur VLC](https://www.isimonbrown.co.uk/vlc-export-frames/)

Enregistrer les frame sous le format **PNG** (TRES IMPORTANT), puis les nommer tel quel : numVidéo_numFrame.png , n'oubliez pas de prendre note des vidéos que vous télécharger et de tenir un csv avec la liste des vidéos. Si jamais on rencontrera un problème sur les donnés cela nous permettra d'identifier directement le probleme.

Vous aurez donc un dossier de ce type
![](folder.png)

## Part 2

Il faut maintenant labeliser les frames extraites, nous allons uttiliser le logiciel [LabelImg](https://github.com/tzutalin/labelImg)

Une fois le logiciel installer, il faut ouvrir le dossier contenant les frames extraites (open dir sur la gauche), de plus il faut que le format du label soit YOLO (sur la gauche du logiciel également)

![voici le logiciel ainsi que les bouton important](labelimg.png)

Une fois que vous avez importer les frames, celle-ci devrait apparaitre dans le logiciel, vous devez ensuite dessiner un rectangle autour de la reine (W le raccourci clavier), puis le nommer, ici queen.

![labelImg rectangle](labelimgqueen.png)

Appuyez ensuite sur save puis next.
Ces étapes sont à répéter pour chaque photo.

## Syntax à uttiliser 

| Type d'abeilles| Health        |
| ---------------|:-------------:| 
| worker         | varoa         |
| drone          | little varoa  | 
| queen          | healthy       |

