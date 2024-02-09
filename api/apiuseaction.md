# API Koban - Cas d'utilisation

## Actions - Récupérer l'ensemble des actions à réaliser pour un utilisateur

L'API Koban permet de récupérer un tableau de toutes les actions à réaliser pour un utilisateur entre 2 dates.

**<u>Prérequis :</u>**

- Disposer des clés API de votre compte Koban
- Disposer du guid Koban de l'utilisateur concerné

**<u>Méthode à utiliser :</u>**

Appelez la méthode API [ncAction/GetPending](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#b004e476-874a-4243-867c-f32f2bbc5300) en GET en transmettant dans le paramètre userid le Guid Koban de votre utilisateur.
Cette méthode permet pour un utilisateur de récupérer toutes les actions à réaliser entre 2 dates en incluant éventuellement des filtres supplémentaires (dernière date de modification, présent ou non sur l'agenda...).

Lancez cette méthode avec les paramètres suivants pour récupérer les actions à réaliser pour l'utilisateur de code abcd entre le 01/12/2020 et le 31/12/2021 :

- **from** : Date de début (ici 01/12/2020)
- **to** : Date de fin (ici 01/01/2021 pour inclure l'ensemble du 31/12)
- **updated** : Date de dernière synchronisation (ici 01/01/2020 pour inclure toutes les actions créées ou modifiées depuis cette date)
- **userid** : abcd (remplacez par le guid de votre utilisateur)
- **st** : 0
- **s** : From
- **ag** : false

**<u>Résultat :</u>**

Le résultat est un tableau d'actions dont les propriétés suivantes sont importantes :

- **Label** : Le titre de l'action
- **ActionType** : Le type d'action (avec ses propriétés Label et Code)
- **Start** : La date de début de l'action
- **End** : La date de fin de l'action
- **Tags** : La liste des tags de l'action
- **Association** : Une action dans Koban est liée à un compte (Third), un contact (Contact) ou une piste (Lead). L'une de ces propriétés est renseignée avec son libellé (Label) et son identifiant Koban (Guid). Il se peut que pour une action, aucune association ne soit renseignée, dans ce cas aucune des propriétés n'est remplie.

**<u>Pour aller plus loin :</u>**

Si vous souhaitez avoir plus d'informations sur la personne associée (Third, Contact ou Lead), vous pouvez appeler les méthodes suivantes pour obtenir des informations complémentaires :

- **Pour un compte** : [ncThird/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#fc544c1c-bd86-4fe2-9347-a81f0a306fba)
- **Pour une piste** : [ncLead/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#a3ce4bdf-1b96-4753-b90b-56b16c95bdc7)
- **Pour un contact** : [ncContact/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#6f54d9a5-84d0-488e-8c22-1b21723dff52)