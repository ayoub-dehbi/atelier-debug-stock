# Journal de débogage
Nom : Dehbi Ayoub

| N° | Action pour reproduire | Résultat attendu / obtenu | Hypothèse et cause identifiée | Correction | Test après correction |
| --- | --- | --- | --- | --- | --- |
| 1 | Charger la page et afficher la liste des produits.|Attendu : la liste des produits s’affiche. Obtenu : la liste ne s’affiche pas. |Le sélecteur #liste-produits ne correspondait pas à l’identifiant HTML : j’avais oublié le s. |Corriger le sélecteur pour qu’il corresponde exactement à l’id HTML : document.querySelector("#liste-produits"). |La liste est bien sélectionnée et les produits s’affichent. |
| 2 |Ajouter un produit et vérifier le tableau. |Attendu : le nouveau produit apparaît tout de suite. Obtenu : les données étaient ajoutées, mais le tableau ne changeait pas. |J’avais oublié d’appeler la fonction d’affichage après l’ajout. |Appeler la fonction d’affichage après avoir ajouté le produit. |Le nouveau produit apparaît immédiatement dans le tableau. |
| 3 |Envoyer le formulaire avec un champ invalide. |Attendu : le formulaire est refusé si tous les champs ne sont pas valides. Obtenu : la validation ne fonctionnait pas correctement. |J’avais utilisé || au lieu de && pour vérifier plusieurs conditions valides. |Utiliser && pour vérifier que toutes les conditions de validation sont vraies. |Le formulaire est accepté uniquement lorsque tous les champs sont valides. |
| 4 |Calculer le total de plusieurs quantités. |Attendu : 2 + 3 donne 5. Obtenu : le résultat pouvait être "23". |Les valeurs des champs étaient des chaînes de caractères (string), donc elles étaient concaténées. |Convertir les valeurs en nombres avec Number() avant de les additionner. |Le total est bien calculé comme un nombre. |
| 5 |Saisir du texte dans la barre de recherche. |Attendu : les résultats changent à chaque caractère saisi. Obtenu : la recherche se mettait à jour seulement après avoir quitté le champ. |J’avais utilisé l’événement change au lieu de input. |Remplacer l’événement change par input. |Les résultats de recherche se mettent à jour pendant la saisie. |

Bilan : quelle méthode réutiliserai-je sur mon prochain brief ?
