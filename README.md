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

Oû _type_ est le type de l'action (souvent un _String_) et _payload_ est le contenu de l'action a utiliser par le reducer sur le _state_ à modifier. Le contenu de _payload_ varie en fonction des besoin de l'action.



