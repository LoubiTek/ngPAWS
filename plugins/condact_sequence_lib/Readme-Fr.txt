Cette bibliothèque vous permet d'exécuter des condact chaque fois qu'un message donné est imprimé via une nouvelle balise de séquence. Bien qu'il ne soit pas utile de l'utiliser dans un message WRITE ou WRITELN,
il peut être utile lorsqu'il est inclus dans:

- Messages système
- Les noms d'objets
- Descriptions de localisation

Par exemple, vous pouvez augmenter le nombre d'un drapeau à chaque fois qu'un message système est affiché (c'est-à-dire chaque fois que le message "Vous prenez xxx" est imprimé).

La syntaxe pour la balise de séquence est

{C: <condact> | <paramètres>}

c'est à dire.

{C: SET | 100}
{C: CREATE | 8}
{C: PLACE | 40 | 23}

Garder à l'esprit:

- Tous les éléments d’un message sont exécutés avant l’impression du message, donc leurs positions importe peu, excepté dans le cas ou vous en ajoutez plusieurs dans le même
  message, car ils seront exécutés dans l'ordre d'apparition.
- Seuls les condacts d'action peuvent être exécutés, et non les conditions (cela n'a même pas de sens).
- Il n'y a pas de contrôle de syntaxe, assurez-vous d'ajouter le nombre approprié de paramètres pour le condact que vous utilisez
- Vous ne pouvez pas utiliser de condact dont le paramètre est une chaîne (comme WRITE ou TITLE)
- Si vous utilisez des condact dont les paramètres sont des mots (comme SYNONYM), vous devez spécifier les mots par numéro de mot, et non par le mot lui-même (c.-à-d. {C: SYNONYM | 78 | 32}
- Vous ne pouvez pas utiliser les identifiants txtpaws dans les balises de séquence (comme d'habitude)

Les crédits pour cette bibliothèque vont à edlobez, dont les idées m'ont amené à penser que cette bibliothèque était une bonne chose à avoir.

Licence: MIT (https://opensource.org/licenses/MIT)
