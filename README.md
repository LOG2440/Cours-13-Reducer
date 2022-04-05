# reducer

Exemple de l'implémentation d'un fonction **Reducer** en JS pur.

# Fonction Reducer

Une fonction **Reducer** est une fonction qui prend 2 paramètres : _state_ et _action_ et retourne un _state_ modifié.
Les paramètres peuvent avoir n'importe quelle forme, mais sont le plus souvent des objets. Par convention, l'attribut _action_ a le format suivant :

```
{
 type : string,
 payload : Object
}
```

Où _type_ est le type de l'action (souvent un _String_) et _payload_ est le contenu de l'action a utiliser par le reducer sur le _state_ à modifier. Le contenu de _payload_ varie en fonction des besoin de l'action.


# Exemple

Cet exemple illustre un _reducer_ qui permet de gérer l'état d'un compteur : incrémenter, décrémenter et remettre à 0 sa valeur à travers les actions suivantes :

```js
const ACTIONS = {
  INCREMENT: "increment",
  DECREMENT: "decrement",
  RESET: "reset",
};
```

Toute autre action est ignorée et l'état n'est pas modifié.

## Exemple d'utilisation

Voici un exemple d'une action d'incrémentation à l'aide du _reducer_ :

```js
let counter = { name: "Timer", count: 0 };
const incrementAction = { type: ACTIONS.INCREMENT, payload: 1 };

counter = reducer(counter, incrementAction);
console.log(counter); // { name: 'Timer', count: 1}
```


# Exercice

- Modifier le code pour ajouter un nouveau paramètre `maxValue` de type `number` qui représente la valeur maximale du compteur.
- Modifier le _reducer_ pour qu'une action d'incrémentation (`INCREMENT`) ne puisse pas modifier l'attribut `count` à plus que `maxValue`.
- Modifier le _reducer_ pour qu'une action de décrémentation (`DECREMENT`) ne puisse pas modifier l'attribut `count` à moins que `0`.
- Modifier le _reducer_ pour tenir compte de ces changements lors d'une action de remise à 0 (`RESET`).
  
Une solution possible est disponible sur la branche [complex_state](https://github.com/LOG2440/reducer/blob/complex_state/reducer.js) du projet.
