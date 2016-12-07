Cryptographie.
=============

Partie 1: Codage César.
----------------------

Depuis l’antiquité, les hommes ont toujours éprouvés (guerres, commerce ...) le besoin de modifier un texte afin de le soustraire à la vue des personnes non autorisées, cette science s’appelle la cryptographie:  graphie-écriture et crypto-caché.

L’un des premiers codages utilisés est le code de César qui doit son nom à l’empereur romain Jules César, il consiste à décaler chaque lettre de l’alphabet de trois rangs :

|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|D|A|B|

Ainsi le mot « ANTIQUITE », devient après codage : « DQWLTXLWH »,  de même le mot codé « UDQJHU » s’écrit « RANGER » après décodage.

Par extension, tout codage obtenu en  décalant les lettres de l’alphabet d’un même rang est appelé code de César, le rang constant est appelé la clé du codage.
Par exemple un codage de César de clé 10, signifie qu’on décale chaque lettre de 10 rangs,  A est remplacé par K, B par L ...
Ce qui donne la correspondance suivante :

|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|D|A|B|D|E|F|G|H|I|J|

À l’aide du tableau précédent :

1. Coder le texte : « OPERATION ANNULEE »

2. Décoder le texte « EBQOXD OVSWSXOB VK MSLVO »

3. Pour faciliter le cryptage et le décryptage d’un texte, on peut utiliser les disques concentriques ([petit](https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/PetitDisque.png) et [grand](https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/GrandDisque.png)), on les fixe par le centre, celui de plus grand diamètre est fixe et l’autre mobile, en le faisant tourner, on obtient le décalage des lettres, donc la correspondance.


1. En utilisant un codage de César de clé 17, coder le texte : « LES PETITS RUISSEAUX FONT DE GRANDES RIVIERES».

2. En utilisant un codage de César de clé 17, décoder le texte « UV HLZ JFEK TVJ JVIGVEKJ HLZ JZWWCVEK JLI EFJ KVKVJ».

1. Un codage de César, transforme  « SUBSTITUTION » en « KMTKLALMLAGF »
Quelle est la clé ?

Parie 2: Décryptage d’un texte par analyse des fréquences.


Partie 3: Codage affine.
