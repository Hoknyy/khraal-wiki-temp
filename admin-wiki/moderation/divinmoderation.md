---
icon: user-shield
---

# DivinModeration - guide staff

Cette page sert de référence rapide pour les modérateurs et administrateurs du réseau KhraalGames.

Objectif des modérateurs : inspecter les comportements suspects, modérer le chat, aider les joueurs et appliquer les sanctions prévues. Les modérateurs ne doivent pas utiliser d'outils qui donnent des items, valident des quêtes, modifient l'économie, changent le gameplay ou contournent une progression joueur.

## Règles de périmètre

Les commandes autorisées aux modérateurs doivent rester orientées observation, enquête, support joueur et sanction modération.

Les commandes réservées aux administrateurs incluent tout ce qui peut impacter fortement un gamemode, retirer toutes les sanctions, gérer une whitelist globale, recharger la configuration ou appliquer des sanctions lourdes hors procédure.

Ne jamais utiliser une commande d'administration pour aider un joueur à progresser plus vite, donner une récompense, valider une quête, contourner une restriction gameplay ou compenser un bug sans validation admin.

## Commandes principales

| Commande | Permission | Public conseillé | Usage |
| --- | --- | --- | --- |
| `/report <joueur>` | Aucune permission staff requise | Joueurs + staff | Signaler un joueur au staff. |
| `/mysanction` | Aucune permission staff requise | Joueurs + staff | Voir son propre profil/casier de sanctions. Alias : `/mysanctions`, `/casier`. |
| `/warn <joueur>` | `divinmoderation.warn` | Modos + admins | Ouvre le menu de sanction. C'est l'entrée principale pour sanctionner proprement. |
| `/sanctions <joueur>` | `divinmoderation.history` | Modos + admins | Voir l'historique de sanctions d'un joueur. |
| `/modtool` | `divinmoderation.modtool` | Modos + admins | Ouvre la boîte à outils de modération. |
| `/socialspy` | `divinmoderation.socialspy` | Modos + admins | Active ou désactive la lecture staff des messages privés. |
| `/freeze <joueur>` | `divinmoderation.freeze` | Modos + admins | Immobilise ou libère un joueur pendant une vérification. |
| `/invsee <joueur>` | `divinmoderation.invsee` | Modos + admins | Voir l'inventaire d'un joueur. À utiliser pour enquête, pas pour modifier. |
| `/armorsee <joueur>` | `divinmoderation.invsee` | Modos + admins | Voir armure et offhand d'un joueur. |
| `/endersee <joueur>` | `divinmoderation.invsee` | Modos + admins | Voir l'ender chest / vault menu d'un joueur selon l'intégration active. |
| `/kick <joueur> [raison...]` | `divinmoderation.kick` | Modos + admins | Expulser un joueur du réseau ou du shard selon l'implémentation active. |
| `/modkick <joueur> [raison...]` | `divinmoderation.kick` | Modos + admins | Alias staff de kick. Alias : `/mkick`. |
| `/unmute <joueur>` | `divinmoderation.unmute` | Modos seniors + admins | Retirer un mute actif. À utiliser seulement en correction d'erreur. |
| `/unban <joueur>` | `divinmoderation.unban` | Admins ou responsables modération | Retirer un ban actif. |
| `/pardon <joueur>` | `divinmoderation.pardon` | Admins seulement | Retire toutes les sanctions actives. Action sensible. |
| `/modban <joueur> <durée\|permanent> [raison...]` | `divinmoderation.ban` | Admins ou responsables modération | Bannir directement un joueur du réseau. Alias : `/mban`. |
| `/kickall [raison...]` | `divinmoderation.kickall` | Admins seulement | Expulse tous les joueurs non exemptés du gamemode courant. Action de maintenance. |
| `/whitelist <on\|off\|status\|add\|remove\|list>` | `divinmoderation.whitelist` | Admins seulement | Gère la whitelist cross-shard du gamemode courant. |
| `/modreload` | `divinmoderation.admin` | Admins techniques seulement | Recharge la configuration DivinModeration. |

## Workflow recommandé pour un modérateur

1. Recevoir un report, observer le contexte et vérifier le joueur ciblé.
2. Utiliser `/sanctions <joueur>` pour voir l'historique.
3. Si le joueur est suspect en jeu, utiliser `/freeze <joueur>` seulement le temps de la vérification.
4. Utiliser `/invsee`, `/armorsee` ou `/endersee` uniquement pour constater des preuves liées à une suspicion.
5. Appliquer la sanction via `/warn <joueur>` pour respecter l'escalade automatique.
6. Ajouter une raison claire, courte et compréhensible.
7. Ne jamais retirer une sanction sans trace claire ou validation d'un responsable quand la sanction est lourde.

## `/warn <joueur>` - menu de sanction

`/warn <joueur>` ouvre le menu principal de sanction. C'est la commande à privilégier pour la majorité des cas, car elle applique les catégories, gravités, raisons et conséquences prévues par DivinModeration.

Le menu permet notamment de choisir :

» La catégorie de l'infraction.
» La gravité.
» La raison.
» Les actions liées à l'enquête : historique, freeze, téléportation staff, inspection inventaire selon permissions.

## Catégories de sanctions

Les sanctions DivinModeration sont pensées pour escalader selon l'historique du joueur.

### Chat

À utiliser pour insultes, spam, provocation, toxicité, contournement léger ou comportement perturbateur dans le chat.

» 1ère infraction : mute 30 min.
» 2ème infraction : mute 2 h.
» 3ème infraction : mute 8 h.
» 4ème infraction : mute 1 j.
» 5ème infraction : mute 3 j.
» 6ème infraction et plus : mute 7 j maximum.

### Comportement

À utiliser pour anti-jeu, perturbation d'événement, nuisance volontaire ou comportement qui dépasse le simple chat.

» 1ère infraction : kick avec avertissement.
» 2ème infraction : kick avec avertissement.
» 3ème infraction : kick + mute 1 h.
» 4ème infraction : ban 12 h.
» 5ème infraction : ban 3 j.
» 6ème infraction et plus : ban 7 j maximum.

### Triche / exploitation

À utiliser pour cheat, duplication, abus de bug, contournement gameplay, avantage injuste ou tentative de nuire à l'économie.

» 1ère infraction : kick avec avertissement.
» 2ème infraction : ban 1 j.
» 3ème infraction : ban 7 j.
» 4ème infraction : ban 30 j.
» 5ème infraction et plus : ban permanent.

## Freeze

`/freeze <joueur>` immobilise le joueur pendant une vérification. Pendant un freeze, le joueur ne doit pas être laissé bloqué sans contact staff.

Bonnes pratiques :

» Expliquer rapidement au joueur qu'une vérification est en cours.
» Garder une durée courte.
» Ne pas utiliser le freeze comme sanction.
» Unfreeze dès que la vérification est terminée.

## Inspection d'inventaire

Les commandes `/invsee`, `/armorsee` et `/endersee` servent à vérifier une suspicion ou comprendre une situation. Pour les modérateurs, l'usage attendu est lecture/inspection.

Interdictions côté modération :

» Ne pas retirer d'item sans validation admin.
» Ne pas ajouter d'item.
» Ne pas corriger une perte joueur depuis ces menus.
» Ne pas déplacer des items pour aider ou pénaliser un joueur hors procédure.

Si une correction d'inventaire est nécessaire, escalader à un admin avec preuves et contexte.

## SocialSpy

`/socialspy` permet au staff autorisé de surveiller les messages privés dans un contexte de modération.

À utiliser uniquement pour :

» Enquête sur harcèlement, scam, menaces ou contournement de mute.
» Vérification après report.
» Surveillance temporaire d'un comportement suspect.

Ne pas utiliser par curiosité ou hors contexte staff.

## Commandes sensibles réservées admin

Ces commandes doivent rester hors périmètre modérateur standard :

| Commande | Pourquoi sensible |
| --- | --- |
| `/modban` | Ban direct réseau, contourne le flux normal si mal utilisé. |
| `/unban` | Retire une sanction lourde. |
| `/unmute` | Corrige une sanction active, doit être justifié. |
| `/pardon` | Retire toutes les sanctions actives. |
| `/kickall` | Affecte massivement un gamemode. |
| `/whitelist` | Bloque ou autorise l'accès à un gamemode. |
| `/modreload` | Action technique pouvant impacter le plugin. |

## Permissions utiles

| Permission | Rôle attendu |
| --- | --- |
| `divinmoderation.warn` | Modération standard. |
| `divinmoderation.history` | Lecture historique staff. |
| `divinmoderation.modtool` | Outils de modération. |
| `divinmoderation.socialspy` | Staff modération autorisé. |
| `divinmoderation.freeze` | Staff capable de gérer une vérification joueur. |
| `divinmoderation.invsee` | Inspection staff. À encadrer en lecture seule côté politique staff. |
| `divinmoderation.kick` | Modération standard ou senior selon politique. |
| `divinmoderation.unmute` | Modos seniors ou admins. |
| `divinmoderation.unban` | Admins ou responsables modération. |
| `divinmoderation.pardon` | Admins seulement. |
| `divinmoderation.ban` | Admins ou responsables modération. |
| `divinmoderation.kickall` | Admins seulement. |
| `divinmoderation.whitelist` | Admins seulement. |
| `divinmoderation.admin` | Admins techniques seulement. |

## Notes techniques utiles

Les bans sont appliqués au niveau réseau, pas seulement sur un gamemode. Un ban posé depuis le Skyblock bloque donc le joueur sur tout le réseau.

Les mutes passent par DivinChatAPI quand DivinPlayerSync / DivinMessages est disponible. Cela permet au mute d'être respecté par le système de chat centralisé.

L'historique de sanctions est stocké côté MySQL pour garder une trace exploitable par le staff.

Les notifications staff passent par Redis pour être visibles cross-shard.

## Politique staff recommandée

Modérateur standard : `/warn`, `/report`, `/modtool`, `/sanctions`, `/socialspy`, `/freeze`, `/invsee`, `/armorsee`, `/endersee`, `/kick`.

Modérateur senior : mêmes commandes + `/unmute` si correction d'erreur claire.

Admin / responsable modération : accès aux commandes sensibles : `/modban`, `/unban`, `/pardon`, `/kickall`, `/whitelist`, `/modreload`.
