# lab-s-creation-utilisateurs.
Pratique de la création et gestion des comptes utilisateurs(Internes et externes) et des groupes et ajouter des membres.

LAB 1 — CRÉATION DES UTILISATEURS
====================================================================

Objectif : Créer 3 utilisateurs internes avec toutes les informations nécessaires.

ACTIONS DANS LE PORTAIL :
1. Connectez-vous au portail : https:https://portal.azure.com
2. Naviguez vers : Entra ID Tous les utilisateurs
3. Cliquez sur « Nouvel utilisateur »  « Créer un utilisateur » (pas inviter !)
4. Renseignez les informations suivantes pour chaque utilisateur :
5. 
UTILISATEUR 1 : Alice Admin
- Nom : Alice Admin
- Nom d’utilisateur : alice@firstaad56666874.onmicrosoft.com
- Groupe d’affichage : Utilisateurs
- Rôles : Aucun
- Mot de passe : générer automatiquement (forcer changement au premier login)
- Paramètres facultatifs :
• Département : Finance
• Poste : Administratrice Junior
• Manager : Aucun

UTILISATEUR 2 : Bob User

- Nom : Bob User
- Nom d’utilisateur : bob@firstaad56666874.onmicrosoft.com
- Département : Marketing
- Poste : Collaborateur
- Mot de passe : généré automatiquement
- 
UTILISATEUR 3 : Claire Support
- Nom : Claire Support
- Nom d’utilisateur : claire@firstaad56666874.onmicrosoft.com
- Département : IT
- Poste : Support Technique
- Mot de passe : généré automatiquement
- CAPTURE D'ECRAN DES TROIS UTILISATEURS CREES
- <img width="1213" height="905" alt="Manage Microsoft Entra ID Identities (FR) _ Gérer les identités Microsoft Entra ID - Google Chrome 17_11_2025 10_41_39" src="https://github.com/user-attachments/assets/3ad8a6de-856c-489f-b4bc-f12529c8d8c6" />

LAB 2 — CRÉATION DES GROUPES ET TYPES D’APPARTENANCE
====================================================================
Objectif : Créer des groupes Sécurité, M365 et un groupe dynamique (licence P1).

ACTIONS DANS LE PORTAIL :
1. Naviguez vers entra ID - Groupes- < Tous les groupes>
2. Cliquez sur « Nouveau groupe »
   
GROUPE 1 : Sécurité – Employés

- Type de groupe : Sécurité
- Nom : SEC-Employes
- Description : Groupe regroupant tous les employés internes
- Type d’appartenance : Assigné
- Membres à ajouter : Alice, Bob, Claire

- GROUPE 2 : Microsoft 365 – Projet Alpha
  
- Type : Microsoft 365
- Nom : M365-ProjetAlpha
- Description : Ressources collaboratives pour le projet Alpha
- Type d’appartenance : Assigné
- Membres : Alice, Bob
- 
GROUPE 3 : Groupe Dynamique IT

- Type : Sécurité
- Nom : SEC-Dynamique-IT
- Appartenance : Dynamique (Utilisateur)
-  Règle dynamique :
(user.department -eq "IT")
- Résultat attendu : Claire rejoint automatiquement ce groupe.

  LAB 3 — INVITATION D’UTILISATEURS EXTERNES (B2B)
====================================================================
Objectif : Inviter un utilisateur invité et lui attribuer des permissions.
ACTIONS :
1. Identité - Utilisateurs -Tous les utilisateurs - « Nouvel utilisateur »
2. Sélectionnez « Inviter un utilisateur externe »
3. Renseignez :
- Adresse email : sergedieudonnee@gmail.com
- Nom : Serge TOGNON
- Message : Bienvenue dans notre tenant de test
- Envoyer automatiquement l’invitation : OUI
4. Ajouter cet invité dans le groupe « M365-ProjetAlpha »
