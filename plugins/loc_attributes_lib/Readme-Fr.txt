Cette bibliothèque implémente des attributs pour les emplacements, tout comme les attributs des objets. Il implémente également plusieurs condacts, similaires à ceux des attributs d'objet:

- LCLEAR -> comme OCLEAR
- LSET -> comme OSET
- LNEG -> comme ONEG
- LZERO -> comme OZERO
- LNOTZERO -> comme oNOTZERO

Enfin, comme il n’ya aucun moyen de définir des attributs dans la base de données du jeu, il existe un condact nommé LINIT:

LINIT locno low_attributes high_attributes

Vous pouvez l'utiliser à l'ancienne (c'est-à-dire si locatyion a les attributs 0 et 1 actifs):

LINIT 10 11000000000000000000000000000000 0000000000000000000000000000000000

Ou vous pouvez utiliser la fonctionnalité ATTR txtpaws:

#define const laLargeRoom 0
#define const laDangerousPlace 1

LINIT 10 ATTR laLargeRoom laDangerousPlace

En outre, vous pouvez l'utiliser "à la dure" en utilisant des nombres décimaux:

LINIT 10 3 0

Veuillez noter que, bien que le condact soit nommé LINIT (initialisation de l'emplacement), il peut être utilisé autant de fois que vous le souhaitez au même endroit, si cela a du sens.

NOTE IMPORTANTE:

Veuillez noter qu'en raison d'une limitation dans le compilateur ngPAWS, qui utilise le dernier bit de chaque paramètre pour marquer s'il possède une indirection, LINIT ne peut pas utiliser les attributs d'emplacement 31 et 63 (doit toujours être défini sur 0).
Une fois initialisées, elles peuvent être utilisées normalement (et peuvent être définies avec LSET), mais leur utilisation n'est pas recommandée, à moins que les 62 autres attributs aient été utilisés.

Licence: MIT (https://opensource.org/licenses/MIT)
