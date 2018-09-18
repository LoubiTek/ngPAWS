Cette extension permet à l'auteur d'utiliser des attributs numériques supplémentaires pour les objets du jeu. Par exemple, un attribut "points de vie" peut être assigner, ou un attribut de densité.

Nouveau condact:

ATTRLET "string" objno value -> définit la valeur de l'attribut "string" pour l'objet objno à la valeur
ATTRGET "string" objno flagno -> copie la valeur de l'attribut "string" pour l'objet objno dans le drapeau flagno

Exemple:

ATTRLET "hitpoints" 10 100
ATTRGET "hitpoints" 10 fAux

REMARQUE: les noms d'attribut doivent être valides au niveau javascript, ils ne doivent donc contenir que des caractères de a-z, A-Z, 0-9 et des tirets bas, sans jamais commencer par un nombre.

Licence: MIT (https://opensource.org/licenses/MIT)
