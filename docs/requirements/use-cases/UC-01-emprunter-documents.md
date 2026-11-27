**INF1163 \| BORNE DE PRÊT EN LIBRE-SERVICE**

UC-01 — Emprunter documents

Cas d’utilisation détaillé

**Acteur principal** — Usager de la bibliothèque.

**Objectif** — Emprunter un ou plusieurs exemplaires à la borne et obtenir un reçu si désiré.

**Déclencheur** — L’usager démarre un emprunt en soumettant ses identifiants à la borne.

**Préconditions** — La borne affiche l’accueil et son catalogue est chargé.

**Postconditions**

- Chaque prêt accepté est associé au compte de l’usager et à l’exemplaire identifié par son RFID. Une date de retour est enregistrée pour chaque prêt.

- Si aucun exemplaire n’a été accepté, aucun nouveau prêt n’est enregistré.

- En fin normale, la borne ferme la session et revient à l’accueil. Une erreur de reçu ne modifie pas les prêts enregistrés.

# Scénario nominal

| **Actions de l’usager**                                                                                                        | **Réponses de la borne**                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1.** L’usager saisit son numéro de compte et son NIP à 5 chiffres, puis valide.                                              | La borne vérifie les identifiants, ouvre la session et invite l’usager à présenter un exemplaire.                                                                                                                  |
| **2.** L’usager présente un exemplaire. Dans le prototype, il saisit au clavier son RFID à 8 chiffres pour simuler la lecture. | La borne retrouve l’exemplaire par son RFID, vérifie sa disponibilité et enregistre le prêt avec sa date de retour. Elle affiche le titre, la date de retour et le nombre d’exemplaires empruntés dans la session. |
| **3.** L’usager répète l’étape 2 pour chaque exemplaire supplémentaire, puis sélectionne **Terminer**.                         | La borne affiche le récapitulatif et demande si l’usager souhaite un reçu.                                                                                                                                         |
| **4.** L’usager choisit de recevoir un reçu.                                                                                   | La borne remet le reçu avec les titres des exemplaires et leurs dates de retour, puis ferme la session et revient à l’accueil.                                                                                     |

Deux exemplaires d’un même titre sont saisis séparément, chacun avec son propre RFID.

# Scénarios alternatifs

| **Actions de l’usager**                                                         | **Réponses de la borne**                                                |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **3a.** L’usager sélectionne **Terminer** avant d’avoir emprunté un exemplaire. | La borne ferme la session et revient à l’accueil sans proposer de reçu. |
| **4a.** L’usager refuse le reçu.                                                | La borne ferme la session et revient à l’accueil.                       |

# Scénarios d’exception

| **Actions ou situation de l’usager**                                                                                             | **Réponses de la borne**                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1a.** L’usager saisit un numéro de compte inconnu.                                                                             | La borne affiche « Numéro de compte ou NIP incorrect » et invite l’usager à reprendre l’étape 1.                                                                           |
| **1b.** L’usager saisit un NIP incorrect.                                                                                        | La borne affiche « Numéro de compte ou NIP incorrect » et invite l’usager à reprendre l’étape 1.                                                                           |
| **2a.** La lecture RFID de l’exemplaire échoue.                                                                                  | La borne indique que la lecture a échoué et invite l’usager à réessayer.                                                                                                   |
| **2b.** L’usager saisit un RFID mal formé ou inconnu du catalogue.                                                               | La borne indique que le RFID est invalide ou que l’exemplaire est introuvable. Elle n’enregistre aucun prêt pour cette tentative et invite l’usager à reprendre l’étape 2. |
| **2c.** L’usager présente un exemplaire déjà prêté ou saisit de nouveau le RFID d’un exemplaire déjà enregistré dans la session. | La borne indique que l’exemplaire est indisponible ou déjà enregistré. Le total reste identique. L’usager peut saisir un autre code ou sélectionner **Terminer**.          |

# Améliorations proposées par l’équipe

| **Actions ou situation de l’usager**                                                          | **Réponses de la borne**                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1c.** L’usager soumet des identifiants valides, mais son abonnement est expiré ou invalide. | À l’étape 1, la borne vérifie aussi la validité de l’abonnement. Si l’abonnement ne permet pas l’emprunt, elle invite l’usager à s’adresser au personnel et revient à l’accueil sans ouvrir de session. |
| **2a.1.** La lecture RFID échoue et l’usager choisit la saisie manuelle.                      | Après l’échec de lecture, la borne propose d’entrer le RFID à 8 chiffres au clavier. Elle reprend l’étape 2 avec le code saisi.                                                                         |
| **2b.1.** L’usager soumet un troisième RFID invalide consécutif.                              | La borne bloque les nouvelles saisies et demande l’assistance d’un employé. Les prêts déjà enregistrés sont conservés. Un RFID reconnu remet le compteur à zéro.                                        |
| **4b.** L’usager demande un reçu imprimé, mais l’impression est indisponible.                 | La borne propose le reçu par courriel s’il est disponible, ou **Sans reçu**. L’usager revient au choix du reçu.                                                                                         |
| **4c.** L’usager demande un reçu par courriel, mais l’envoi est indisponible.                 | La borne propose le reçu imprimé s’il est disponible, ou **Sans reçu**. L’usager revient au choix du reçu.                                                                                              |
| **4d.** Les deux modes de reçu sont indisponibles.                                            | La borne informe l’usager qu’aucun reçu ne peut être remis, confirme les prêts enregistrés et ferme la session. Elle revient à l’accueil.                                                               |

Avec le choix du mode de reçu, la borne propose **Imprimé**, **Par courriel** et **Sans reçu** à la fin de l’étape 3.
