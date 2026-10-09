# Diagnostic

Une section par test en échec : renseignez ses quatre champs.

## testAddingALineToAnUnknownOrderIsNotFound

**Symptôme** : 

**Cause** :

**Règle du module en jeu** :

**Correctif** :

## testAddingALineToAPaidOrderIsAConflict

**Symptôme** : Quand on essaie d'ajouter une ligne sur un order paid, on reçoit une 201 created au lieu d'une erreur.

**Cause** : 

**Règle du module en jeu** :

**Correctif** :

## testAddingALineToMyOrder

**Symptôme** :

**Cause** :

**Règle du module en jeu** :

**Correctif** :

## testAddingALineWithAZeroQuantityIsUnprocessable

**Symptôme** : Quand on essaie d'ajouter un dish en quantité 0, on reçoit une 201 created et non une erreur.

**Cause** : Dans le fichier, la quantité doit pouvoir être nulle.

**Règle du module en jeu** : 

**Correctif** : Le minimum quantity était réglé sur 0 dans OrderAddLineInput.php, ce qui permet au user de mettre une quantity de 0, le test pete quand même, je me demande si il n'y a pas un autre test que je n'ai pas résolu qui le fait péter.

## testListingKitchenTicketsReturnsMine

**Symptôme** :

**Cause** :

**Règle du module en jeu** :

**Correctif** :

## testListingKitchenTicketsWithoutTokenIsUnauthorized

**Symptôme** : On peut lister les kitchens tickets en ayant aucun token, mais on ne peut pas en ayant un token invalide.

**Cause** : On vérifie que le token est valide mais on ne vérifie pas strictement qu'on en fourni un.

**Règle du module en jeu** : Tout le monde peut se connecter sans token à la liste des tickets

**Correctif** :

## testOpeningAnOrderIgnoresAnAbandonedOne

**Symptôme** : Lorsque Bob ouvre ses commandes, il voit toujours celle qu'il a abandonnée alors qu'elle devrait disparaitre.

**Cause** : 

**Règle du module en jeu** :

**Correctif** :

## testPayingMyOrderMarksItPaid

**Symptôme** : Les commandes payées ne passent pas de pending à payed.

**Cause** : 

**Règle du module en jeu** :

**Correctif** :

## testRefreshingTwiceWithTheSameTokenIsUnauthorized

**Symptôme** : Alice arrive à se connecter deux fois avec le même token, le test doit verifier que ce n'est pas possible.

**Cause** : dans le fichier qui gere les refreshs token, single use est passé sur faux.

**Règle du module en jeu** : ça met en périle la sécurité du compte. Un token qui peut être utilisé deux fois sans le refresh est un token qui peut etre volé et réutilisé.

**Correctif** : Passer le single use en true pour garantir un statut 401 unauthorized si un user essaie de se connecter avec le meme token non refresh dans gesdinet_jwt_refresh_token.yaml.

## testRemovingALineFromSomeoneElsesOrderIsForbidden

**Symptôme** : 

**Cause** :

**Règle du module en jeu** :

**Correctif** :
