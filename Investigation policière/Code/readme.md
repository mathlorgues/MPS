Cryptographie.
=============

Partie 1: Codage César.
----------------------

Depuis l’antiquité, les hommes ont toujours éprouvé (guerres, commerce ...) le besoin de modifier un texte afin de le soustraire à la vue des personnes non autorisées, cette science s’appelle la **cryptographie**:  graphie-écriture et crypto-caché.

L’un des premiers codages utilisés est le code de César qui doit son nom à l’empereur romain Jules César, il consiste à décaler chaque lettre de l’alphabet de trois rangs :

|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|A|B|C|

Ainsi le mot « ANTIQUITE », devient après codage : « DQWLTXLWH »,  de même le mot codé « UDQJHU » s’écrit « RANGER » après décodage.

Par extension, tout codage obtenu en  décalant les lettres de l’alphabet d’un même rang est appelé code de César, le rang constant est appelé la **clé du codage**.

Par exemple un codage de César de clé 10, signifie qu’on décale chaque lettre de 10 rangs,  A est remplacé par K, B par L ...
Ce qui donne la correspondance suivante :

|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|A|B|C|D|E|F|G|H|I|J|

À l’aide du tableau précédent :

1. Coder le texte : « OPERATION ANNULEE »

2. Décoder le texte « EBQOXD OVSWSXOB VK MSLVO »

3. Pour faciliter le cryptage et le décryptage d’un texte, on peut utiliser les disques concentriques ([petit](https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/PetitDisque.png) et [grand](https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/GrandDisque.png)), on les fixe par le centre, celui de plus grand diamètre est fixe et l’autre mobile, en le faisant tourner, on obtient le décalage des lettres, donc la correspondance.


1. En utilisant un codage de César de clé 17, coder le texte : « LES PETITS RUISSEAUX FONT DE GRANDES RIVIERES».

2. En utilisant un codage de César de clé 17, décoder le texte « UV HLZ JFEK TVJ JVIGVEKJ HLZ JZWWCVEK JLI EFJ KVKVJ».

1. Un codage de César, transforme  « SUBSTITUTION » en « KMTKLALMLAGF »
Quelle est la clé ?

Parie 2: Décryptage d’un texte par analyse des fréquences.
----------------------------------------------------------

Si on ne connaît pas la clé, le code de César est assez facile à décrypter, une méthode certes un peu longue, appelée **brute-force** consiste à essayer toutes les 25 clés possibles. Une autre est l’analyse des fréquences.

Suivant la langue, toutes les lettres n’ont pas la même fréquence d’apparition dans un texte. Le tableau suivant donne la fréquence théorique d’apparition des lettres d’un texte de la langue française.

<!--|E|S|A|I|N|T|R|U|L|O|D|C|P|M|V|Q|G|F|H|B|X|J|Y|Z|K|W| -->
<!--|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---| -->
<!--|17,52|8,17|8,01|7,35|7,22|7,07|6,69|6|5,77|5,43|3,91|3,23|2,94|2,90|1,41|1,14|1,6|1,06|0,88|0,88|0,47|0,44|0,30|0,12|0,05|0,02| -->

 
|E  |S  |A  |I  |N  |T  |R  |U  |L  |O  |D  |C  |P  |M  |V  |Q  |G  |F  |H  |B  |X  |J  |Y  |Z  |K  |W|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|17,52|8,17|8,01|7,35|7,22|7,07|6,69|6|5,77|5,43|3,91|3,23|2,94|2,90|1,41|1,14|1,6|1,06|0,88|0,88|0,47|0,44|0,30|0,12|0,05|0,02|

1. Déchiffrer le texte suivant :
TW J L FYP ELFAP OLYD YZECP DPCGTNP TW QLFE WL OPXLDBFPC

<!-- IL Y A UNE TAUPE DANS NOTRE SERVICE IL FAUT LA DEMASQUER -->

1. Dans la corbeille, sur du papier froissé, les enquêteurs ont trouvé le message suivant :
RGGFIKVQCRWFIDLCVJVTIVKVTFDDVGIVMLVKEVGIVMVEVQGRJCRGFCZTV . Déchiffrer le.

<!-- Apportez la formule secrète comme prévu et ne prévenez pas la police
RGGFIKVQ CR WFIDLCV JVTIVKV TFDDV GIVML VK EV GIVMVEVQ QRJ CR GFCZTV
-->

Partie 3: Codage affine.
------------------------

Principe :  A chaque lettre est associée un nombre entier n selon son rang dans l’alphabet de 0 pour la lettre A à 25 pour la lettre Z.
Deux nombres a et b sont choisis comme clés.

Méthode :
- Au nombre n de départ, on associe le nombre m = an + b.
- Ce nombre m n’étant pas toujours compris entre 0 et 25, il ne permet pas de chiffrer une lettre.
- Pour résoudre ce problème, le codage se fait en associant au nombre de départ n le nombre entier p,
reste de la division euclidienne de m par 26.
- Puis, on retranscrit p en lettres.

Par exemple, si on prend a = 4 et b = 1.
La lettre Z est remplacée par n = 25.
Puis m = 4 × 25 + 1 = 101.
Or 101 n’est pas compris entre 0 et 25, on effectue donc la division euclidienne de 101 par 26 ce qui
donne :  101 = 3 × 26 + 23.
Donc p = 23 qui correspond à la lettre X. Z est donc codée par X.

On prend a=3 et b=7.
1. Coder la lettre J avec la clé (3;7).

1. Coder le mot "Moi" avec la clé (3;7).

 <!-- RXF -->

1. Décrypter le mot HPJJF avec la clé (3;7).

 <!-- AUSSI -->

Partie 4: Codage à l'aide d'une table de Vigenère.
==================================================

Même si l’on connaissait depuis fort longtemps les faiblesses de la cryptographie par substitution, il n’y eut pas entre César et le XVI ème siècle de véritable nouveau procédé cryptographique, à la fois sûr et facile à utiliser. Blaise de Vigenère, né en 1523, fut l’initiateur d’une nouvelle façon de chiffrer les messages qui
domina 3 siècles durant.

Vigenère était quelqu’un de très hétéroclite, tantôt alchimiste, écrivain, historien, il était aussi diplomate au service des ducs de Nevers et des rois de France. C’est en 1586 qu’il publie son Traité des chiffres ou Secrètes manières d’écrire, qui explique son nouveau chiffre (le texte intégral est disponible sur le site de la
Bibliothèque Nationale de France).

L’idée de Vigenère est d’utiliser un chiffre de César, mais où le décalage utilisé change de lettres en
lettres. Pour cela, on utilise une table composée de 26 alphabets, écrits dans l’ordre, mais décalés de ligne
en ligne d’un caractère. On écrit encore en haut un alphabet complet, pour le texte à coder, et à gauche,
verticalement, un dernier alphabet, pour la clé .

Il s’agit de la table de Vigenère suivante :
![table de vigenère](https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/table.png)

Pour coder un message avec le chiffre de Vigenère, on choisit une clé qui sera un mot de longueur arbitraire. On écrit ensuite cette clé sous le message à coder, en la répétant aussi souvent que nécessaire pour que sous chaque lettre du message à coder, on trouve une lettre de la clé. Ensuite pour coder, on regarde dans le tableau l'intersection de la ligne de la lettre à coder et de la colonne de la lettre de la clé.

Exemple: On veut coder le mot CRYPTOGRAPHIE avec la clé MATHWEB :

|Texte à crypter|C|R|Y|P|T|O|G|R|A|P|H|I|E|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Clé            |M|A|T|H|W|E|B|M|A|T|H|W|E|
|Texte crypté	  |O|R|	|	|	|	|	|	|	|	|	|	|	|

Pour coder la lettre C, la clé est donnée par la lettre M.
On cherche donc dans le tableau l'intersection de la
ligne C et de la colonne M. On trouve la lettre O.
On procède de façon analogue pour la suite.

 <img src="https://github.com/mathlorgues/MPS/blob/master/Investigation%20polici%C3%A8re/Code/table%20couleur.png" alt="table de vigenère avec explication visuelle" height="1000" width="1000">

 1. Compléter le tableau précédent.

 <!-- ORRWPSHDAIOEI -->

 1. Décoder le message MPIVJFESSSROKTMXE avec la clé MATHS.

 <!-- apportez la formule -->
