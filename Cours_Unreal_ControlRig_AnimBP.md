# Résumé du cours Unreal du jeudi 01/10

>Perso on a abordé beaucoup de sujets très vite, j'ai pas tout compris sur le moment.
>J'ai fait des recherches de mon côté pour mieux capté, voilà ce que j'ai compris de ce qu'on a vu aujourd'hui.

>Les (?) ça veut dire que je suis pas sûr des infos
------------------------------------
### Les objectifs d'aujourd'hui étaient : 

- De modifier un des mesh du template third person pour avoir un mesh adapté à la first person view
- De faire une animation du personnage qui se protège du soleil avec une de ses mains.

### Pour ce faire on a vu :

- Modifier la caméra (pourquoi on a pas besoin du camera broom, l'utilisation de la rotation du controller)
- Pourquoi on a besoin de deux meshes (un pour la world representation et un autre pour la first person view)
- Le Control Rig
- L'Animation Blue Print



## CONTROL RIG & cie

> *TLDR : ça permet de modifier un modèle 3D et/ou de l'animer depuis Unreal sans passer par un logiciel externe.*

- Skeleton Mesh : 
  - Un mesh avec des bones qui permette de modifier le mesh (=/= static mesh qui ne peut pas être modifier)
		
- Bone : 
  - Un segment dans un skeleton mesh qui relie différentes parties d'un modèle 3D

- Control Rig Blueprint : 
  - Un blueprint qui permet de modifier un skeleton mesh depuis le moteur.
  - Son objectif : faciliter l'animation et l'édition de modèle 3D dans Unreal.
  - Permet notamment de créer des "Controls".
  - peut se créer directement à partir d'un skeleton mesh en faisant **Clic Droit dessus > Create > Control Rig**.
  - En double-cliquant dessus depuis le Content Browser cela va ouvrir **le Control Rig Editor** 

- Controls :
  - Des Actors(?) visibles uniquement dans le Control Rig Editor (?) qui permettent de modifier indirectement le transform d'un ou plusieurs bone dans un mesh en modifiant leur transform.
  - la liaison entre le transform d'un control et le transform de son (ou ses) bones ne se fait pas automatiquement et doit se faire via le Control Rig Editor
	 
- Control Rig Editor : 
  - Permet de positionner des Controls et de lier leurs transforms aux transforms des bones du Skeleton Mesh.

### Sources  
[Doc Unreal : Vue rapide sur les Controls Rig](https://dev.epicgames.com/documentation/unreal-engine/how-to-create-control-rigs-in-unreal-engine?application_version=5.7)

### Pour aller plus loin 
J'ai trouvé cette [playlist](https://www.youtube.com/playlist?list=PL2A3wMhmbeArc-d471A4cku1pYA31X-ir) qui explique vraiment bien.
Il a l'air de rentrer vraiment en profondeur dans les control rigs, si ça vous intéresse.
 
## ANIMATION

>*TLDR: c'est un rabbits hole, je vous laisse la doc et bon courage*

Deux moyens de faires des animation depuis Unreal :

- Avec le [Sequencer](https://dev.epicgames.com/documentation/unreal-engine/cinematics-and-movie-making-in-unreal-engine?application_version=5.7)
- Avec un [Animation Blueprint](https://dev.epicgames.com/documentation/unreal-engine/animation-blueprints-in-unreal-engine?application_version=5.7)

### Quand utiliser l'un ou l'autre ? 

<img src="https://d1iv7db44yhgxn.cloudfront.net/documentation/images/809f9bf2-5630-4afe-b2d7-c51bcb5d6de8/image_7.gif" alt="Description" width="300" height="200">

- Le Sequencer :
  - Pour faire des animations "fixes" (pour faire le perso qui se protège du soleil avec sa main c'est suffisant)
  - ça ressemble à [l'Animation View](https://docs.unity3d.com/uploads/Main/AnimationEditorDopeSheetView.png) d'Unity ou à [l'Animation Player](https://docs.godotengine.org/en/stable/_images/animation_animation_panel_overview.webp) de Godot.

- L'Animation Blueprint :
  - Pour faire des animations procédurales (?). (Une main qui s'accroche automatiquement à une poignée de porte quand on s'approche d'une porte)

### Sources 

[Doc Unreal sur comment animer des Controls Rig](https://dev.epicgames.com/documentation/unreal-engine/animating-with-control-rig-in-unreal-engine?application_version=5.7)

------------------




