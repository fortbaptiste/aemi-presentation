# AEMI GMAO - Document de Presentation v1

## Partie 1 : Introduction, Installation, Connexion, Dashboard & Navigation

**Prepare par :** ExplorIA
**Destine a :** Clement Kabongo - AEMI / Forrest Groupe
**Date :** Fevrier 2026
**Version :** 1.0

---

# Table des matieres - Partie 1

1. [Introduction & Accueil](#1-introduction--accueil)
2. [Installation de l'Application (PWA)](#2-installation-de-lapplication-pwa)
   - 2.1 [Sur Android (avec Chrome)](#21-sur-android-avec-chrome)
   - 2.2 [Sur iPhone / iPad (avec Safari)](#22-sur-iphone--ipad-avec-safari)
   - 2.3 [Sur Ordinateur (Chrome / Edge)](#23-sur-ordinateur-chrome--edge)
   - 2.4 [Qu'est-ce qu'une PWA ?](#24-quest-ce-quune-pwa-)
3. [Connexion & Identifiants](#3-connexion--identifiants)
   - 3.1 [La page de connexion](#31-la-page-de-connexion)
   - 3.2 [Les comptes disponibles](#32-les-comptes-disponibles)
   - 3.3 [Niveaux d'acces](#33-niveaux-dacces)
   - 3.4 [Securite & sessions](#34-securite--sessions)
   - 3.5 [Comment tester les deux vues](#35-comment-tester-les-deux-vues)
4. [Dashboard Administrateur - Vue d'Ensemble](#4-dashboard-administrateur---vue-densemble)
   - 4.1 [Les cartes KPI en haut de page](#41-les-cartes-kpi-en-haut-de-page)
   - 4.2 [La carte interactive des equipements](#42-la-carte-interactive-des-equipements)
   - 4.3 [Etat du parc de generateurs](#43-etat-du-parc-de-generateurs)
   - 4.4 [Actions rapides](#44-actions-rapides)
   - 4.5 [Activite recente](#45-activite-recente)
   - 4.6 [Alertes & rappels](#46-alertes--rappels)
   - 4.7 [Graphiques de tendance et analyse](#47-graphiques-de-tendance-et-analyse)
   - 4.8 [Mode sombre](#48-mode-sombre)
   - 4.9 [Systeme de notifications](#49-systeme-de-notifications)
   - 4.10 [Design responsive](#410-design-responsive)
5. [Navigation & Structure](#5-navigation--structure)
   - 5.1 [La barre laterale (Sidebar)](#51-la-barre-laterale-sidebar)
   - 5.2 [Le selecteur de contexte metier](#52-le-selecteur-de-contexte-metier)
   - 5.3 [Liste de tous les modules](#53-liste-de-tous-les-modules)
   - 5.4 [Navigation entre les modules](#54-navigation-entre-les-modules)
   - 5.5 [Comportement sur mobile](#55-comportement-sur-mobile)
   - 5.6 [Le module ExplorIA](#56-le-module-exploria)

---

# 1. Introduction & Accueil

Bonjour Clement, j'espere que vous allez bien. Je voulais vous presenter la v1 de l'application AEMI GMAO. Le but va vraiment etre d'avoir votre retour de maniere detaillee pour voir ce que je peux ameliorer.

Ce document est le premier d'une serie qui va couvrir en detail chaque aspect de l'application. Je vais prendre le temps de tout vous expliquer de maniere simple, avec des exemples, pour que vous puissiez bien comprendre ce qui a ete fait et surtout pour que vous puissiez me donner votre avis sur chaque partie.

## Qu'est-ce que l'application AEMI GMAO ?

AEMI GMAO est une application de **Gestion de Maintenance Assistee par Ordinateur** (c'est ce que veut dire le sigle GMAO). En termes simples, c'est un outil qui va permettre a votre equipe de gerer toute la maintenance des groupes electrogenes en RDC (Republique Democratique du Congo) de maniere organisee et centralisee.

Aujourd'hui, quand il y a un generateur en panne chez un client, il faut coordonner beaucoup de choses : savoir quel technicien est disponible, quelle est la priorite de la panne, est-ce qu'on a les pieces de rechange en stock, est-ce qu'il faut un vehicule pour se deplacer, etc. Toutes ces informations sont souvent dispersees entre des appels telephoniques, des messages WhatsApp, des fiches papier... L'idee de cette application, c'est de centraliser tout ca dans un seul endroit accessible depuis un telephone ou un ordinateur.

Voici ce que l'application permet de faire, de maniere generale :

- **Gerer les interventions** : Creer, planifier, assigner et suivre chaque intervention de maintenance du debut a la fin. Que ce soit un entretien de routine (vidange aux 250 heures, 500 heures, 1000 heures), une reparation d'urgence, un constat, une installation ou une manutention.

- **Suivre les equipements** : Avoir une fiche complete pour chaque groupe electrogene avec sa marque, son modele, son numero de serie, ses heures de fonctionnement, son historique de maintenance, sa localisation GPS, et meme les photos.

- **Gerer les clients** : Chaque client a sa fiche avec ses sites, ses contacts, ses equipements et l'historique de toutes les interventions qu'on a faites chez lui.

- **Planifier le travail** : Un calendrier et un tableau Kanban (un tableau avec des colonnes ou on peut deplacer les taches) pour organiser et visualiser le planning de la semaine.

- **Gerer la facturation** : Suivre les offres envoyees aux clients, les factures, les paiements, le chiffre d'affaires.

- **Gerer l'atelier** : Pour les travaux qui se font en atelier (reparation de moteurs, alternateurs, transformateurs), avec des ordres de travail et un suivi des etapes.

- **Gerer la logistique** : Les pieces de rechange, le stock, les commandes, les demandes de materiel.

- **Gerer le charroi** : Les vehicules de l'entreprise, leur etat, qui les utilise, quand est prevu le prochain entretien.

- **Voir les rapports** : Des graphiques et des tableaux qui donnent une vue d'ensemble sur l'activite : combien d'interventions ce mois-ci, quel est le taux de completion, quelles sont les pannes les plus frequentes, etc.

- **Voir la carte** : Une carte interactive qui montre ou se trouvent tous les generateurs, avec des couleurs differentes selon leur etat (en marche, en panne, en entretien...).

- **Vue technicien mobile** : Les techniciens sur le terrain ont leur propre interface, simplifiee et optimisee pour le telephone. Ils voient leurs taches assignees, peuvent demarrer une intervention, prendre des photos, remplir des checklists, faire signer le client, etc.

## A propos des donnees actuelles

Un point que je tiens a preciser : pour le moment, **la majorite des donnees que vous verrez dans l'application sont des donnees fictives** (des donnees de demonstration). C'est normal, c'est fait expres pour pouvoir vous montrer comment l'application fonctionne avec des exemples. Vous allez voir des noms de clients comme "Rawbank", "Vodacom Congo", "Brassimba" -- ce sont des exemples pour illustrer le fonctionnement.

Cela dit, il y a une partie qui est deja en mode production : **la partie technicien**. Quand vous (en tant qu'administrateur) creez une intervention et que vous l'assignez a un technicien, ce technicien va bien voir cette tache apparaitre sur son telephone dans sa vue mobile. Ce lien entre l'admin et le technicien fonctionne deja en temps reel.

## La base de donnees

L'application est connectee a une vraie base de donnees **Supabase**. Supabase, c'est un service en ligne qui fait office de base de donnees et de systeme d'authentification (c'est-a-dire le systeme qui verifie les mots de passe et gere les sessions des utilisateurs). Tout ce qui est stocke (les interventions, les equipements, les clients, les comptes utilisateurs) est dans cette base de donnees en ligne, ce qui veut dire que les donnees sont accessibles depuis n'importe quel appareil connecte a Internet.

Pour cette v1, l'application fonctionne aussi en mode "demo" -- c'est-a-dire que meme si la connexion a Supabase n'est pas configuree, vous pouvez quand meme utiliser l'application avec les donnees de demonstration. C'est ce qui permet de tester facilement sans avoir besoin de configurer quoi que ce soit.

## Qui est ExplorIA ?

**ExplorIA** est l'agence qui a concu et developpe cette application pour AEMI / Forrest Groupe. Vous trouverez d'ailleurs un lien vers le site d'ExplorIA directement dans l'application (dans le menu de navigation), qui presente l'agence et ses services. On en reparlera plus en detail dans la section Navigation.

## Apercu de tous les modules

Pour vous donner une vue d'ensemble avant de plonger dans les details, voici la liste de tous les modules disponibles dans l'application :

| Module | Description rapide |
|--------|-------------------|
| **Dashboard** | Page d'accueil avec les indicateurs cles, la carte, les alertes |
| **Interventions** | Liste et detail de toutes les interventions de maintenance |
| **Equipements GE** | Inventaire des groupes electrogenes avec fiches detaillees |
| **Planning** | Calendrier mensuel + tableau Kanban pour organiser le travail |
| **Clients** | Gestion des clients, sites, contacts |
| **Equipes** | Gestion des techniciens, superviseurs, chauffeurs |
| **Facturation** | Offres, factures, suivi des paiements |
| **Carte** | Carte interactive avec tous les equipements geolocalises |
| **Reporting** | Rapports et analyses graphiques |
| **Atelier** | Ordres de travail, inventaire pieces, planning atelier |
| **Logistique** | Charroi (vehicules), magasin (stock), demandes de materiel |
| **Parametres** | Configuration du profil, notifications, preferences |
| **Vue Technicien** | Interface mobile pour les techniciens sur le terrain |

Dans ce premier document, on va se concentrer sur les 5 premiers points : l'installation, la connexion, le dashboard principal et la navigation. Les modules individuels seront detailles dans les parties suivantes.

---

# 2. Installation de l'Application (PWA)

Avant de pouvoir utiliser l'application, il faut y acceder. L'application AEMI GMAO est accessible via un navigateur web, mais elle peut aussi etre installee sur votre telephone ou votre ordinateur pour fonctionner comme une application native. C'est ce qu'on appelle une **PWA** (Progressive Web App).

L'adresse de l'application est : **https://aemi-gmao.vercel.app**

Vous pouvez tout simplement ouvrir cette adresse dans votre navigateur et utiliser l'application directement. Mais je vous recommande de l'installer sur votre appareil, ca sera beaucoup plus pratique au quotidien. Voici comment faire selon votre appareil.

---

## 2.1 Sur Android (avec Chrome)

Si vous utilisez un telephone ou une tablette Android, voici les etapes pour installer l'application. Je vais detailler chaque etape pour que ce soit le plus clair possible.

### Etape 1 : Ouvrir Chrome

Ouvrez le navigateur **Google Chrome** sur votre telephone Android. C'est important que ce soit Chrome, car c'est le navigateur qui gere le mieux les PWA sur Android. Si vous utilisez un autre navigateur (comme Samsung Internet ou Firefox), ca peut aussi fonctionner, mais Chrome est le plus fiable pour ca.

### Etape 2 : Aller sur le site

Dans la barre d'adresse en haut de Chrome, tapez l'adresse suivante :

```
https://aemi-gmao.vercel.app
```

Appuyez sur Entrer pour charger la page. Vous allez voir la page de connexion de l'application AEMI GMAO apparaitre.

### Etape 3 : La banniere d'installation automatique

Sur beaucoup de telephones Android, quand vous visitez une PWA pour la premiere fois, Chrome va automatiquement afficher une petite banniere en bas de l'ecran qui dit quelque chose comme **"Ajouter AEMI GMAO a l'ecran d'accueil"** ou **"Installer AEMI"**. Si vous voyez cette banniere :

1. Appuyez simplement sur **"Installer"** ou **"Ajouter"**
2. Une petite fenetre de confirmation va apparaitre
3. Appuyez a nouveau sur **"Installer"**
4. C'est fait !

### Etape 3 (alternative) : Si la banniere n'apparait pas

Si la banniere n'apparait pas automatiquement (ca arrive parfois), pas de panique. Voici comment faire manuellement :

1. Appuyez sur les **trois petits points** (le menu) en haut a droite de Chrome. C'est l'icone avec trois points alignes verticalement.
2. Dans le menu qui s'ouvre, cherchez l'option qui dit **"Installer l'application"** ou **"Ajouter a l'ecran d'accueil"**. Le texte exact peut varier selon la version de Chrome et la langue de votre telephone.
3. Appuyez dessus.
4. Une fenetre de confirmation va apparaitre avec le nom "AEMI GMAO" et l'icone de l'application. Vous pouvez modifier le nom si vous le souhaitez, mais je recommande de laisser "AEMI GMAO".
5. Appuyez sur **"Installer"** ou **"Ajouter"**.

### Etape 4 : L'icone apparait sur votre ecran d'accueil

Apres l'installation, l'icone AEMI GMAO va apparaitre sur votre ecran d'accueil, exactement comme n'importe quelle autre application que vous auriez telechargee depuis le Google Play Store. Vous la trouverez probablement sur la derniere page de votre ecran d'accueil, ou dans votre tiroir d'applications.

### Etape 5 : Ouvrir l'application

Quand vous appuyez sur l'icone AEMI GMAO sur votre ecran d'accueil, l'application va s'ouvrir **en plein ecran**, sans la barre d'adresse de Chrome, sans les boutons de navigation du navigateur. Ca ressemble vraiment a une application native que vous auriez telechargee depuis le Play Store. La barre de navigation du telephone (les boutons en bas) sera toujours la, mais le reste de l'ecran sera entierement dedie a l'application.

L'experience est la meme que si c'etait une application telechargee, sauf que :
- Elle ne prend presque pas de place sur votre telephone (pas besoin de telecharger 100 Mo comme certaines applications)
- Elle se met a jour automatiquement (pas besoin d'aller sur le Play Store pour les mises a jour)
- Elle a besoin d'une connexion Internet pour fonctionner (comme la plupart des applications de gestion)

### Remarque pour les techniciens

C'est particulierement utile pour les techniciens qui sont sur le terrain. Ils installent l'application sur leur telephone, et ensuite ils n'ont qu'a appuyer sur l'icone pour avoir directement acces a leurs interventions du jour. Pas besoin de se souvenir de l'adresse du site, pas besoin d'ouvrir Chrome d'abord -- c'est direct.

---

## 2.2 Sur iPhone / iPad (avec Safari)

Si vous utilisez un iPhone ou un iPad, la procedure est un petit peu differente car Apple fait les choses a sa maniere. Le point le plus important a retenir ici est que **l'installation doit se faire depuis Safari**. Ca ne fonctionne pas depuis Chrome sur iPhone (meme si Chrome est installe sur votre iPhone, Apple ne lui permet pas d'installer des PWA). Donc il faut bien utiliser **Safari**, le navigateur qui est deja installe par defaut sur votre iPhone.

### Etape 1 : Ouvrir Safari

Trouvez l'icone de **Safari** sur votre iPhone ou iPad. C'est l'icone qui ressemble a une boussole bleue et blanche. Si vous ne la trouvez pas, vous pouvez la chercher en balayant vers le bas sur votre ecran d'accueil pour ouvrir la recherche, et taper "Safari".

### Etape 2 : Aller sur le site

Dans la barre d'adresse en haut (ou en bas selon votre version d'iOS), tapez :

```
https://aemi-gmao.vercel.app
```

Appuyez sur "Aller" (ou le bouton bleu sur le clavier) pour charger la page. Vous devriez voir la page de connexion de l'application AEMI GMAO.

### Etape 3 : Appuyer sur le bouton de partage

C'est la partie specifique a Apple. En bas de l'ecran Safari (ou en haut selon la version), vous allez voir une icone qui ressemble a un **carre avec une fleche qui pointe vers le haut**. C'est le bouton de partage d'Apple. Appuyez dessus.

Si vous etes sur un iPad, ce bouton peut se trouver en haut a droite de la barre d'adresse au lieu d'etre en bas.

### Etape 4 : Trouver "Sur l'ecran d'accueil"

Quand vous appuyez sur le bouton de partage, un menu va apparaitre avec plein d'options (envoyer par message, envoyer par mail, copier le lien, etc.). Vous devez **faire defiler vers le bas** dans ce menu pour trouver l'option qui dit :

**"Sur l'ecran d'accueil"** (en francais) ou **"Add to Home Screen"** (en anglais)

Cette option est representee par une petite icone avec un "+" dans un carre. Si vous ne la voyez pas tout de suite, continuez a faire defiler vers le bas. Elle est parfois cachee assez loin dans la liste.

### Etape 5 : Nommer et ajouter

Une fois que vous avez appuye sur "Sur l'ecran d'accueil", un nouvel ecran va apparaitre qui vous montre :
- Le nom de l'application : **AEMI GMAO** (vous pouvez le modifier si vous voulez, mais je recommande de le laisser comme ca)
- L'adresse du site
- Un apercu de l'icone

Appuyez sur **"Ajouter"** en haut a droite de cet ecran.

### Etape 6 : L'application est installee

L'icone AEMI GMAO va maintenant apparaitre sur votre ecran d'accueil, parmi vos autres applications. Quand vous l'ouvrez, l'application se lance en **plein ecran** -- pas de barre d'adresse Safari, pas de boutons de navigation du navigateur. C'est une experience en plein ecran qui ressemble a une application native telecharges depuis l'App Store.

Sur iPhone, la barre du haut (avec l'heure, le reseau, la batterie) reste visible, mais tout le reste de l'ecran est utilise par l'application AEMI GMAO.

### Pourquoi Safari et pas Chrome ?

C'est une question qu'on me pose souvent. Sur iPhone, Apple oblige toutes les applications de navigateur (Chrome, Firefox, etc.) a utiliser le moteur web de Safari en coulisses. Mais seul Safari a le droit d'installer des applications web sur l'ecran d'accueil. C'est une restriction d'Apple, pas un choix de notre part. Donc meme si vous preferez Chrome au quotidien, pour cette etape d'installation il faut passer par Safari.

---

## 2.3 Sur Ordinateur (Chrome / Edge)

Si vous travaillez depuis un ordinateur (Windows, Mac ou Linux), vous pouvez aussi installer l'application comme un programme sur votre bureau. C'est pratique car ca vous permet d'avoir l'application dans votre barre des taches et de l'ouvrir d'un seul clic.

### Avec Google Chrome

1. Ouvrez **Google Chrome** sur votre ordinateur
2. Allez sur **https://aemi-gmao.vercel.app**
3. Regardez dans la barre d'adresse (a droite) : vous devriez voir une petite icone qui ressemble a un **ecran avec une fleche vers le bas**, ou un petit **"+"**. C'est l'icone d'installation.
4. Cliquez dessus
5. Une fenetre de confirmation apparait : cliquez sur **"Installer"**
6. L'application va s'ouvrir dans sa propre fenetre, separee de Chrome

Si vous ne voyez pas l'icone d'installation dans la barre d'adresse, vous pouvez aussi :
1. Cliquer sur les **trois petits points** en haut a droite de Chrome (le menu)
2. Chercher **"Installer AEMI GMAO..."** ou **"Plus d'outils" > "Creer un raccourci..."**
3. Cocher "Ouvrir dans une fenetre" si l'option est proposee
4. Cliquer sur **"Installer"** ou **"Creer"**

### Avec Microsoft Edge

La procedure est tres similaire avec Edge :
1. Ouvrez **Microsoft Edge**
2. Allez sur **https://aemi-gmao.vercel.app**
3. Cliquez sur les **trois petits points** en haut a droite
4. Cherchez **"Applications" > "Installer AEMI GMAO"** ou **"Installer ce site en tant qu'application"**
5. Confirmez en cliquant sur **"Installer"**

### Apres l'installation sur ordinateur

Une fois installee, l'application AEMI GMAO :
- Apparait comme un programme dans votre **barre des taches** (Windows) ou dans votre **Dock** (Mac)
- Peut etre epinglee a la barre des taches pour un acces rapide
- S'ouvre dans sa propre fenetre, sans les onglets et la barre d'adresse du navigateur
- Peut etre retrouvee dans le menu Demarrer (Windows) ou dans le Launchpad (Mac)

C'est comme si vous aviez installe un vrai logiciel, mais en realite c'est toujours l'application web qui tourne. L'avantage, c'est que les mises a jour se font automatiquement sans que vous ayez a telecharger quoi que ce soit.

---

## 2.4 Qu'est-ce qu'une PWA ?

Pour ceux qui sont curieux, je vais expliquer simplement ce qu'est une PWA.

**PWA** signifie **Progressive Web App**, ce qui se traduit par "Application Web Progressive". C'est une technologie qui permet de transformer un site web en quelque chose qui se comporte comme une application classique.

En gros, c'est le meilleur des deux mondes :

| Avantage | Application classique (Play Store / App Store) | PWA (notre cas) |
|----------|------------------------------------------------|-----------------|
| Installation | Telecharger depuis un store, souvent lourd | Installation legere, en un clic |
| Mises a jour | Doivent etre telechargees manuellement | Automatiques, transparentes |
| Espace disque | Peut prendre 50 Mo a 500 Mo | Quelques Mo seulement |
| Acces hors ligne | Oui (si l'app le supporte) | Partiellement (les pages deja visitees) |
| Plein ecran | Oui | Oui |
| Notifications | Oui | Oui (sur Android et ordinateur) |
| Disponible partout | Non (Android OU iPhone) | Oui (partout ou il y a un navigateur) |
| Cout de developpement | Elevee (2 apps a maintenir) | Plus economique (1 seule base de code) |

Pour AEMI GMAO, ca veut dire que la meme application fonctionne sur le telephone Android du technicien sur le terrain a Lubumbashi, sur l'iPhone de Clement a Kinshasa, et sur l'ordinateur de bureau au siege. Pas besoin de developper et maintenir 3 versions differentes.

La couleur de theme de l'application quand elle est installee est un bleu fonce (**#2857a4**), qui correspond a l'identite visuelle d'AEMI. Quand vous ouvrez l'application en mode PWA, la barre de statut de votre telephone prendra cette couleur bleue.

L'application est aussi configuree pour fonctionner dans n'importe quelle orientation (portrait ou paysage), ce qui est pratique sur tablette ou quand un technicien tourne son telephone pour avoir une vue plus large.

### Le bouton "Installer l'App" dans l'application

Il y a aussi un bouton vert **"Installer l'App"** directement dans la barre laterale de l'application (en bas a gauche). Si vous etes connecte et que vous n'avez pas encore installe la PWA, ce bouton sera visible et vous permettra de lancer l'installation sans avoir a passer par le menu du navigateur. C'est fait pour simplifier les choses, surtout pour les techniciens qui ne sont pas forcement a l'aise avec les menus du navigateur.

Une fois l'application installee, ce bouton change et affiche **"App installee"** avec une coche verte, pour confirmer que tout est en ordre.

Sur iPhone, comme Apple ne permet pas de declencher l'installation automatiquement, le bouton affiche un message explicatif qui guide l'utilisateur : "Sur iPhone : 1. Appuyez sur le bouton Partager en bas, 2. Choisissez 'Sur l'ecran d'accueil', 3. Appuyez sur 'Ajouter'".

---

# 3. Connexion & Identifiants

Maintenant que l'application est installee (ou que vous y accedez via votre navigateur), voyons comment se connecter.

## 3.1 La page de connexion

Quand vous ouvrez l'application pour la premiere fois (ou apres vous etre deconnecte), vous arrivez sur la **page de connexion**. Voici ce que vous y voyez :

### Description visuelle de la page

La page a un fond clair et lumineux avec un leger degrade. Au centre de l'ecran, vous trouvez :

1. **Le logo AEMI** en haut, dans un petit carre blanc avec des bords arrondis et une ombre legere. En dessous du logo, vous avez le texte "AEMI GMAO" et juste en dessous en plus petit : "Gestion de Maintenance Assistee par Ordinateur".

2. **Le formulaire de connexion** dans un cadre blanc (une "carte" comme on dit en design). Ce formulaire contient :
   - Un champ **Email** : c'est la ou vous tapez votre adresse email. Le champ a un placeholder qui dit "votre@email.cd" pour vous donner une idee du format attendu.
   - Un champ **Mot de passe** : avec des etoiles (ou des points) qui masquent ce que vous tapez. Il y a aussi un petit icone d'oeil a droite du champ : si vous cliquez dessus, ca affiche le mot de passe en clair pour que vous puissiez verifier ce que vous avez tape. Cliquez a nouveau pour le masquer. C'est pratique quand on n'est pas sur d'avoir tape le bon mot de passe.
   - Un bouton **"Se connecter"** en bleu, avec une petite icone de fleche. Quand vous cliquez dessus, le bouton change de texte pour afficher "Connexion..." pendant que le systeme verifie vos identifiants.

3. **Les boutons d'acces rapide** en dessous du formulaire. C'est une fonctionnalite tres pratique pour la phase de test. Vous avez 3 petits boutons cote a cote :
   - **Admin** (Clement K.) avec les initiales "CK" sur un fond bleu
   - **Tech 1** (Patrick I.) avec les initiales "PI" sur un fond vert
   - **Tech 2** (J-Pierre T.) avec les initiales "JT" sur un fond jaune/ambre

   En appuyant sur un de ces boutons, vous etes connecte automatiquement avec le compte correspondant, sans avoir a taper l'email et le mot de passe. C'est vraiment fait pour faciliter les tests : vous pouvez passer d'un compte a l'autre rapidement pour voir les differentes vues.

4. **Le copyright** tout en bas : "AEMI - Forrest Groupe" avec l'annee en cours.

### En cas d'erreur de connexion

Si vous tapez un mauvais email ou un mauvais mot de passe, un message d'erreur apparait en haut du formulaire dans un cadre rouge clair : **"Email ou mot de passe incorrect"**. Ce message est accompagne d'une icone de triangle d'avertissement pour attirer votre attention.

---

## 3.2 Les comptes disponibles

Pour cette version de demonstration, il y a **3 comptes utilisateurs** deja crees. Voici les identifiants :

| Email | Mot de passe | Role | Nom complet | Acces |
|-------|-------------|------|-------------|-------|
| `admin@aemi.cd` | `aemi2026` | Administrateur | Clement Kabongo | Tout le dashboard admin, tous les modules |
| `tech1@aemi.cd` | `aemi2026` | Technicien | Patrick Ilunga | Vue mobile technicien uniquement |
| `tech2@aemi.cd` | `aemi2026` | Technicien | Jean-Pierre Tshombe | Vue mobile technicien uniquement |

Quelques precisions :

- **Le mot de passe est le meme pour les 3 comptes** : `aemi2026`. C'est fait expres pour simplifier les tests. En production, chaque utilisateur aura bien evidemment son propre mot de passe.

- **L'email se termine par @aemi.cd** : C'est un format d'email professionnel qui correspond au domaine AEMI en RDC. En production, les vrais emails des utilisateurs seront utilises.

- **Clement Kabongo** est le compte administrateur. C'est le compte qui a acces a tout : le tableau de bord, les interventions, les equipements, les clients, la facturation, les rapports, etc. C'est le compte que vous utiliserez principalement, Clement.

- **Patrick Ilunga** est un technicien fictif. Il a des competences en "GE Caterpillar" et "Electricite BT" (Basse Tension). Son numero de telephone est +243 81 000 0004.

- **Jean-Pierre Tshombe** est un autre technicien fictif. Il a des competences en "GE Perkins", "GE Cummins" et "Mecanique". Son numero de telephone est +243 81 000 0005.

---

## 3.3 Niveaux d'acces

L'application a un systeme de roles qui determine ce que chaque utilisateur peut voir et faire. Voici les roles prevus dans le systeme :

| Role | Description | Ce qu'il voit |
|------|-------------|---------------|
| **Administrateur** | Le gestionnaire principal (vous, Clement) | Tout : dashboard complet, tous les modules, toutes les donnees, possibilite de creer/modifier/supprimer |
| **Superviseur** | Un responsable d'equipe sur le terrain | La plupart des modules, mais avec certaines restrictions sur les parametres et la facturation |
| **Technicien** | Un technicien de maintenance sur le terrain | Uniquement la vue mobile avec ses interventions assignees |
| **Chauffeur** | Un chauffeur de vehicule | Sa vue specifique avec les missions de transport |
| **Agent Administratif** | Un agent au bureau | Les modules administratifs (facturation, clients, reporting) |

Pour cette v1, les deux roles principaux qui sont pleinement fonctionnels sont **Administrateur** et **Technicien**.

### Ce que voit l'Administrateur

Quand vous vous connectez avec le compte `admin@aemi.cd`, vous arrivez sur le **dashboard administrateur complet**. C'est la vue "bureau" de l'application, concu pour etre utilise sur un ecran d'ordinateur ou une tablette. Vous avez acces a :

- La barre laterale de navigation avec tous les modules
- Le tableau de bord avec les KPI, les graphiques, la carte
- Toutes les pages de gestion (interventions, equipements, clients, etc.)
- Les parametres de l'application
- Et meme la vue technicien (pour pouvoir tester ce que voient les techniciens)

### Ce que voit le Technicien

Quand vous vous connectez avec `tech1@aemi.cd` ou `tech2@aemi.cd`, vous arrivez sur la **vue mobile technicien**. C'est une interface completement differente, optimisee pour un telephone portable. Le technicien voit :

- Un en-tete avec son nom et la date du jour, un indicateur GPS (vert si le GPS est actif, rouge sinon)
- Des statistiques du jour : combien d'interventions terminees, combien d'heures travaillees, combien de taches restantes
- La liste de ses interventions, organisee en sections :
  - **Intervention en cours** (si une intervention est demarree) : un bandeau bleu bien visible en haut avec le nom du client, le chronometre du temps ecoule, un bouton pour ouvrir l'itineraire dans Google Maps
  - **Urgentes / En retard** : les interventions qui sont en retard ou marquees comme urgentes, avec un indicateur rouge du nombre de jours de retard
  - **Aujourd'hui** : les interventions prevues pour aujourd'hui
  - **A venir** : les interventions planifiees pour les prochains jours

Chaque carte d'intervention montre :
- La priorite (basse, normale, haute, urgente) avec un code couleur
- Le type d'intervention (entretien, reparation, constat, etc.)
- Le nom du client
- Les informations sur l'equipement (marque, modele, puissance)
- L'adresse du site
- La date et l'heure prevues
- Le statut actuel
- Des boutons d'action rapide : appeler le client, ouvrir l'itineraire dans Google Maps

Le technicien **ne voit pas** le dashboard administrateur, les modules de facturation, les rapports, les parametres generaux, etc. Il a une vue epuree et centree sur ses taches.

---

## 3.4 Securite & sessions

Quelques mots sur la securite du systeme d'authentification :

### Supabase Auth

Le systeme de connexion utilise **Supabase Auth**, qui est un service d'authentification professionnel. Ca veut dire que :
- Les mots de passe ne sont jamais stockes en clair : ils sont "haches" (transformes en une chaine de caracteres illisible) avant d'etre enregistres
- La communication entre l'application et le serveur est chiffree (HTTPS)
- Les tentatives de connexion sont surveillees pour prevenir les attaques

### Sessions persistantes

Une fois que vous vous etes connecte, **votre session est maintenue**. Ca veut dire que si vous fermez l'application et que vous la rouvrez plus tard (meme le lendemain), vous serez toujours connecte. Pas besoin de retaper votre email et mot de passe a chaque fois.

La session est stockee de maniere securisee dans votre navigateur (ou dans l'application installee). Elle reste active tant que vous ne vous deconnectez pas manuellement.

### Se deconnecter

Pour vous deconnecter, il y a un petit bouton avec une icone de "sortie" (une porte avec une fleche) dans le coin inferieur gauche de la barre laterale, a cote de votre nom et de votre role. Cliquez dessus et vous serez deconnecte et renvoye vers la page de connexion.

---

## 3.5 Comment tester les deux vues

Je vous recommande de tester les deux vues (admin et technicien) pour bien comprendre comment l'application fonctionne dans les deux cas. Voici comment faire facilement :

### Methode 1 : Utiliser les boutons d'acces rapide

C'est la methode la plus simple :
1. Sur la page de connexion, appuyez sur le bouton **"Admin"** pour vous connecter en tant qu'administrateur
2. Explorez le dashboard, creez une intervention, assignez-la a un technicien
3. Deconnectez-vous (bouton en bas a gauche de la barre laterale)
4. Sur la page de connexion, appuyez sur le bouton **"Tech 1"** ou **"Tech 2"**
5. Vous verrez la vue technicien avec les interventions qui ont ete assignees

### Methode 2 : Depuis le dashboard admin

Quand vous etes connecte en tant qu'administrateur, il y a un bouton **"Vue Technicien"** en haut a droite du dashboard (avec une icone de telephone). En cliquant dessus, vous pouvez voir a quoi ressemble la vue mobile du technicien, directement depuis votre session admin. C'est pratique pour verifier rapidement.

### Methode 3 : Deux navigateurs

Si vous voulez voir les deux vues en meme temps :
1. Ouvrez l'application dans **Chrome** et connectez-vous en tant qu'admin
2. Ouvrez l'application dans un **autre navigateur** (Edge, Firefox) ou dans une **fenetre de navigation privee** et connectez-vous en tant que technicien
3. Vous pouvez maintenant voir les deux ecrans cote a cote

Cette methode est utile pour verifier en temps reel que quand l'admin assigne une tache, elle apparait bien du cote du technicien.

---

# 4. Dashboard Administrateur - Vue d'Ensemble

Quand vous vous connectez en tant qu'administrateur, la premiere page que vous voyez est le **Tableau de Bord** (Dashboard). C'est la page principale de l'application, celle qui vous donne une vue d'ensemble de toute l'activite de maintenance. Prenons le temps de detailler chaque element de cette page.

Le dashboard vous accueille avec un message : **"Bienvenue, Clement Kabongo"** (ou le nom de l'utilisateur connecte). En dessous, la date du jour. C'est un petit detail, mais ca permet de confirmer rapidement que vous etes connecte avec le bon compte.

A droite du titre, vous avez un bouton **"Vue Technicien"** avec une icone de smartphone. Comme explique plus haut, ce bouton vous permet de basculer vers la vue mobile pour voir ce que voient les techniciens.

---

## 4.1 Les cartes KPI en haut de page

La premiere chose que vous voyez sur le dashboard, ce sont les **4 cartes KPI** alignees en haut. "KPI" signifie "Key Performance Indicator", ou en francais "Indicateur Cle de Performance". En gros, ce sont les 4 chiffres les plus importants a surveiller.

Les 4 cartes sont disposees en ligne sur un grand ecran, ou en grille de 2x2 sur un ecran plus petit. Voici le detail de chacune :

### Carte 1 : Total Interventions

- **Icone** : Un outil (clef) sur un fond bleu clair
- **Chiffre** : Le nombre total d'interventions dans le systeme
- **Sous-texte** : Un pourcentage de variation par rapport au mois dernier (par exemple "+12% vs mois dernier") avec une petite fleche verte qui indique la tendance a la hausse

Cette carte vous dit en un coup d'oeil combien d'interventions sont enregistrees dans le systeme. Ca inclut les interventions passees, en cours et a venir.

### Carte 2 : Montant Facture

- **Icone** : Un signe dollar sur un fond vert clair
- **Chiffre** : Le montant total facture, affiche en Francs Congolais (FC). Par exemple : "8.550.000 FC"
- **Sous-texte** : Un pourcentage de variation ("+8% vs mois dernier")

Cette carte montre le chiffre d'affaires genere par les interventions. C'est le total de toutes les interventions qui ont ete facturees. Le montant est formate avec le separateur de milliers francais (point ou espace) pour faciliter la lecture des grands nombres.

### Carte 3 : Taux de Completion

- **Icone** : Une horloge sur un fond jaune/ambre clair
- **Chiffre** : Un pourcentage, par exemple "75%"
- **Barre de progression** : En dessous du chiffre, une barre horizontale qui se remplit en vert proportionnellement au pourcentage. Si le taux est de 75%, la barre est remplie aux trois quarts.

Cette carte vous dit quel pourcentage des interventions ont ete terminees par rapport au total. C'est un indicateur de productivite : plus le chiffre est haut, mieux c'est. Le calcul est simple : (nombre d'interventions terminees / nombre total d'interventions) x 100.

### Carte 4 : Alertes Actives

- **Icone** : Un triangle d'avertissement sur un fond rouge clair (ou gris si pas d'alerte)
- **Chiffre** : Le nombre d'interventions en retard (c'est-a-dire dont la date prevue est passee et qui ne sont pas encore terminees)
- **Sous-texte** : Le nombre d'interventions en attente de facturation

Cette carte change de couleur selon la situation :
- Si tout va bien (0 alerte), elle reste dans des tons neutres
- Si il y a des interventions en retard, le cadre prend une teinte rouge pale et le chiffre s'affiche en rouge pour attirer l'attention

C'est la carte la plus "alarmante" : si vous voyez un chiffre rouge la, ca veut dire qu'il y a des interventions qui auraient du etre faites mais qui ne l'ont pas ete. Il faut agir.

---

## 4.2 La carte interactive des equipements

Juste en dessous des cartes KPI, il y a une grande **carte interactive** qui prend les deux tiers de la largeur de l'ecran. C'est une carte geographique (type Google Maps) centree sur la RDC, qui montre l'emplacement de tous les groupes electrogenes enregistres dans le systeme.

### Les marqueurs sur la carte

Chaque generateur est represente par un point de couleur sur la carte. La couleur du point indique l'etat du generateur :

| Couleur | Signification |
|---------|--------------|
| Vert | Le generateur est operationnel, tout va bien |
| Rouge | Le generateur est en panne, il faut intervenir |
| Orange/Jaune | Le generateur a besoin d'un entretien (seuil de maintenance approche) |
| Gris | Le generateur est hors service |

Au-dessus de la carte, il y a une legende qui reprend ces couleurs avec le nombre de generateurs dans chaque etat. Par exemple : "Operationnel (12) - En panne (3) - Entretien (5) - Hors service (1)".

### Interaction avec la carte

Vous pouvez :
- **Zoomer** et **dezoomer** avec la molette de la souris (ou en pincant avec deux doigts sur un ecran tactile)
- **Deplacer** la carte en cliquant et en faisant glisser
- **Cliquer sur un marqueur** pour voir les details du generateur : son nom, sa marque, son modele, sa puissance, ses heures de fonctionnement, et la date de la derniere intervention

Cette carte est utile pour avoir une vue geographique de votre parc de generateurs. En un coup d'oeil, vous pouvez voir ou sont concentres les problemes (les points rouges) et quelles zones sont bien couvertes.

---

## 4.3 Etat du parc de generateurs

A droite de la carte (ou en dessous sur un ecran plus petit), il y a un panneau qui resume l'**etat du parc** de generateurs. C'est une liste simple avec :

- **Operationnel** : nombre de generateurs qui fonctionnent normalement (en vert)
- **En panne** : nombre de generateurs en panne (en rouge)
- **Entretien** : nombre de generateurs qui necessitent un entretien (en orange)
- **Hors service** : nombre de generateurs retires du service (en gris)
- **Total equipements** : le nombre total de generateurs dans le systeme

Chaque ligne est cliquable et a une couleur de fond qui correspond a l'etat. C'est un resume rapide et visuel de la sante de votre parc.

Par exemple, si vous voyez :
```
Operationnel : 12
En panne : 3
Entretien : 5
Hors service : 1
Total : 21
```

Ca vous dit que sur vos 21 generateurs, 12 fonctionnent bien, 3 sont en panne (il faut les reparer), 5 ont besoin d'un entretien bientot, et 1 a ete mis de cote.

---

## 4.4 Actions rapides

En dessous de la carte et du panneau d'etat du parc, il y a une rangee de **4 boutons d'action rapide**. Ce sont des raccourcis pour acceder rapidement aux taches les plus courantes :

| Bouton | Icone | Couleur | Action |
|--------|-------|---------|--------|
| **Nouvelle Intervention** | + | Bleu | Ouvre la page des interventions pour en creer une nouvelle |
| **Voir Equipements** | Engrenage | Vert | Ouvre la liste de tous les equipements |
| **Voir Clients** | Batiment | Violet | Ouvre la liste des clients |
| **Planning** | Calendrier | Jaune/Ambre | Ouvre le planning |

Ces boutons sont la pour gagner du temps. Au lieu de chercher dans le menu de navigation, vous pouvez directement cliquer sur l'action que vous voulez faire. Ils sont disposes en 4 colonnes sur un grand ecran et en 2 colonnes de 2 sur un ecran plus petit.

---

## 4.5 Activite recente

La section suivante du dashboard montre l'**activite recente**. C'est une liste des 8 dernieres interventions, classees par date. Cette section prend les deux tiers de la largeur de l'ecran.

Chaque ligne d'intervention montre :

- **Une icone coloree a gauche** qui indique le type d'intervention :
  - Rouge pour les reparations
  - Bleu pour les entretiens
  - Orange/Ambre pour les constats
  - Gris pour les autres types

- **Le nom du client** en texte normal
- **Le type d'intervention et le nom de l'equipement** en texte plus petit en dessous

- **Le statut** a droite, sous forme de badge colore :
  - Vert pour "Terminee" / "Validee" / "Facturee"
  - Orange/Ambre pour "En cours" / "Sur site"
  - Bleu pour "Creee" / "Planifiee" / "Affectee"

- **La date** en petit texte sous le statut

- **Un triangle d'avertissement rouge** si l'intervention est en retard

- **Une petite fleche** a droite pour indiquer que la ligne est cliquable

En cliquant sur une ligne, vous accedez directement a la fiche detaillee de cette intervention. C'est un moyen rapide de voir ce qui se passe et de plonger dans les details si necessaire.

En haut a droite de cette section, il y a un lien **"Tout voir"** qui vous amene a la page complete des interventions avec tous les filtres et options de tri.

Si il n'y a aucune intervention dans le systeme, la section affiche un message "Aucune intervention" avec une icone d'outil grisee.

---

## 4.6 Alertes & rappels

A droite de l'activite recente (ou en dessous sur petit ecran), il y a le panneau **Alertes & Rappels**. C'est une colonne qui regroupe toutes les alertes qui necessitent votre attention. Les alertes sont generees automatiquement par le systeme en fonction des donnees.

Voici les types d'alertes que vous pouvez voir :

### Interventions en retard

Si des interventions ont depasse leur date prevue sans avoir ete terminees, une alerte rouge apparait avec le nombre d'interventions concernees. Par exemple :

> **3 en retard**
> Interventions depassees a traiter

En cliquant dessus, vous etes redirige vers la page des interventions filtree sur les interventions en retard.

### Equipements en panne

Si des generateurs sont en statut "En panne", une alerte rouge apparait :

> **2 en panne**
> Equipements necessitant une reparation

### Equipements necessitant un entretien

Si des generateurs approchent de leur seuil de maintenance (nombre d'heures de fonctionnement), une alerte orange apparait :

> **5 entretien**
> Equipements necessitant un entretien

### Interventions dans les 48h

Si des interventions sont planifiees dans les prochaines 48 heures, une alerte bleue apparait :

> **2 dans 48h**
> Interventions a preparer

C'est un rappel pour s'assurer que tout est pret (pieces de rechange, vehicule, technicien disponible) avant l'intervention.

### Facturation en attente

Si des interventions sont terminees mais pas encore facturees, une alerte violette apparait :

> **4 a facturer**
> Interventions non facturees

### Quand tout va bien

Si il n'y a aucune alerte active (pas d'intervention en retard, pas de panne, pas d'entretien en attente), le panneau affiche un message vert rassurant :

> (coche verte) **Tout est en ordre**
> Aucune alerte active

---

## 4.7 Graphiques de tendance et analyse

En bas du dashboard, il y a deux graphiques cote a cote qui donnent une vue analytique de l'activite.

### Graphique 1 : Tendance & Chiffre Facture

Ce graphique combine deux types de donnees sur les 6 derniers mois :

- **Une ligne bleue** qui montre le nombre d'interventions par mois. Ca permet de voir si l'activite augmente ou diminue au fil du temps.
- **Des barres vertes** qui montrent le montant facture par mois en Francs Congolais. Ca donne une idee du chiffre d'affaires genere.

Les mois affiches vont d'aout a janvier (6 mois). L'axe de gauche correspond au nombre d'interventions, l'axe de droite correspond aux montants factures.

En survolant (ou en touchant) un point du graphique, une infobulle apparait avec les valeurs exactes pour ce mois.

### Graphique 2 : Causes des Pannes

Ce graphique en forme de **donut** (un camembert avec un trou au milieu) montre la repartition des causes de pannes. Il ne prend en compte que les interventions de type "reparation" qui ont une cause de panne renseignee.

Chaque part du donut represente une cause de panne, avec un pourcentage. Par exemple :
- Surchauffe : 35%
- Probleme electrique : 25%
- Usure mecanique : 20%
- Manque de carburant : 12%
- Autre : 8%

Ce graphique est utile pour identifier les problemes recurrents. Si vous voyez que 35% des pannes sont dues a la surchauffe, ca peut indiquer un probleme de maintenance preventive (les entretiens ne sont peut-etre pas faits assez souvent, ou les systemes de refroidissement ne sont pas verifies).

Si il n'y a pas assez de donnees de panne, le graphique affiche un message "Aucune donnee de panne disponible".

---

## 4.8 Mode sombre

L'application dispose d'un **mode sombre** (dark mode) qui change les couleurs de l'interface pour un fond fonce au lieu d'un fond clair. C'est utile quand on travaille le soir ou la nuit, ou tout simplement si vous preferez un look plus sombre.

Le mode sombre peut etre active depuis la page **Parametres** de l'application. Quand il est active :
- Le fond blanc devient un gris tres fonce
- Les textes noirs deviennent blancs ou gris clair
- Les cartes et les panneaux prennent des tons sombres
- Les couleurs d'accent (bleu, vert, rouge) restent visibles mais avec des nuances adaptees
- Les graphiques s'adaptent automatiquement aux couleurs sombres

Le choix du mode (clair ou sombre) est sauvegarde dans votre navigateur, donc il est conserve meme si vous fermez l'application.

---

## 4.9 Systeme de notifications

L'application a un systeme de notifications integre qui vous alerte quand quelque chose d'important se passe. Vous pouvez acceder aux notifications depuis la **cloche** dans la barre laterale (en bas, a cote de "Notifications").

Les notifications sont organisees par categories :

| Categorie | Couleur | Exemples |
|-----------|---------|----------|
| **Urgences** | Rouge | Intervention en retard, equipement en panne |
| **Maintenance** | Orange/Ambre | Entretien requis, intervention assignee, intervention dans les 48h |
| **Logistique** | Bleu | Stock bas, demande de pieces |
| **Facturation** | Violet | Facture en attente, paiement recu |
| **Informations** | Gris | Resume journalier, rapport hebdomadaire |

Chaque notification a :
- Un niveau de priorite (critique, haute, moyenne, basse) avec un point de couleur
- Un titre
- Une description
- L'heure ou la date de creation (affichee en temps relatif : "Il y a 5 min", "Il y a 2h", "Hier", etc.)
- Un lien pour aller directement a l'element concerne

Les notifications sont generees automatiquement a partir des donnees du systeme. Par exemple, si un generateur atteint ses 250 heures de fonctionnement et qu'un entretien est prevu a 250 heures, une notification sera creee pour prevenir l'administrateur.

Il y a aussi un badge de comptage sur l'icone de la cloche qui indique le nombre de notifications non lues.

Dans les **Parametres**, vous pouvez configurer quelles notifications vous voulez recevoir ou non. Par exemple, vous pouvez desactiver les notifications de rapport hebdomadaire si vous n'en avez pas besoin, ou activer les alertes de stock bas si vous voulez etre prevenu quand une piece de rechange est en quantite insuffisante.

---

## 4.10 Design responsive

Un point que je voulais souligner : l'application est concu pour fonctionner sur tous les types d'ecrans. C'est ce qu'on appelle le "responsive design".

### Sur un grand ecran (ordinateur de bureau, ecran 15 pouces et plus)

- La barre laterale est toujours visible a gauche
- Le contenu s'affiche avec plusieurs colonnes (les cartes KPI sur une seule ligne, la carte a cote du panneau d'etat du parc, etc.)
- Les graphiques sont cote a cote
- Tout est bien espace et lisible

### Sur un ecran moyen (tablette, petit ordinateur portable)

- La barre laterale peut etre reduite (les textes disparaissent, seules les icones restent) pour donner plus de place au contenu
- Les cartes KPI passent sur 2 lignes de 2
- Les sections qui etaient cote a cote s'empilent les unes sous les autres
- Le contenu reste lisible et fonctionnel

### Sur un petit ecran (telephone)

- La barre laterale est cachee par defaut. Pour y acceder, vous appuyez sur l'icone "hamburger" (trois traits horizontaux) en haut a gauche
- La barre laterale s'ouvre alors en superposition avec un fond assombri
- Les cartes KPI sont sur 2 colonnes
- Tout s'empile verticalement
- Les boutons et les textes sont suffisamment grands pour etre lisibles et cliquables avec le doigt
- Il y a un en-tete fixe en haut avec le logo AEMI GMAO et le bouton de menu

Le but, c'est que que vous soyez au bureau devant votre ordinateur ou dans un vehicule avec votre telephone, l'application reste utilisable et agreable.

---

# 5. Navigation & Structure

Maintenant qu'on a vu le dashboard en detail, parlons de la navigation. Comment se deplacer dans l'application, ou trouver chaque module, et comment l'interface est organisee.

## 5.1 La barre laterale (Sidebar)

La barre laterale est l'element central de la navigation. C'est la colonne a gauche de l'ecran qui contient tous les liens vers les differents modules de l'application. Voici sa structure de haut en bas :

### Le logo AEMI GMAO

Tout en haut de la barre laterale, vous voyez le **logo AEMI** suivi du texte "AEMI" en gras et "GMAO" en lettres plus petites et espacees. C'est l'identite de l'application.

A cote du logo (ou a la place si la barre est reduite), il y a un **bouton avec une fleche** pour replier ou deplier la barre laterale. Quand vous cliquez sur ce bouton :
- Si la barre est depliee (textes + icones), elle se replie pour ne montrer que les icones. Ca donne plus de place au contenu principal.
- Si la barre est repliee (icones seulement), elle se deplie pour montrer les textes.

C'est pratique quand vous connaissez deja les icones par coeur et que vous voulez plus d'espace pour le contenu.

### Le selecteur de contexte metier (juste en dessous du logo)

C'est un element important de l'application. On va en parler en detail juste apres (section 5.2).

### Les liens de navigation

La liste des modules, chacun avec une icone et un texte. Le module actif (la page ou vous etes actuellement) est mis en valeur avec un fond bleu degrade et un texte blanc. Les autres modules sont en gris et prennent une couleur plus foncee quand vous passez la souris dessus.

### Notifications et Parametres

En bas de la liste de navigation, avant les informations utilisateur, il y a :
- **Notifications** : avec l'icone de cloche et le badge de comptage
- **Parametres** : avec l'icone de roue dentee

### Le bouton "Installer l'App"

Un bouton vert avec l'icone de telechargement. Si l'application est deja installee, il affiche "App installee" avec une coche.

### Les informations utilisateur

Tout en bas de la barre laterale, vous voyez :
- Vos **initiales** dans un cercle bleu (par exemple "CK" pour Clement Kabongo)
- Votre **nom complet**
- Votre **role** (Administrateur, Technicien, etc.)
- Un bouton de **deconnexion** (icone de porte avec une fleche rouge)

---

## 5.2 Le selecteur de contexte metier

C'est une fonctionnalite qui merite qu'on s'y attarde. L'application AEMI GMAO ne gere pas seulement la maintenance des groupes electrogenes. Elle couvre en fait **3 contextes metier** differents :

### 1. Maintenance GE (Groupes Electrogenes)

C'est le contexte principal et celui qui est le plus developpe dans cette v1. Il couvre :
- Les interventions de maintenance sur le terrain
- Le suivi des groupes electrogenes
- La gestion des clients et des sites
- La planification et le planning
- La facturation

L'icone est un eclair jaune sur fond bleu.

### 2. Atelier

C'est le contexte pour les travaux en atelier : reparation de moteurs, alternateurs, transformateurs. Quand vous basculez vers ce contexte, les modules de la barre laterale changent pour montrer :
- Tableau de Bord (atelier)
- Ordres de Travail
- Inventaire
- Planning Atelier
- Techniciens

L'icone est une usine violette sur fond violet clair.

### 3. Logistique

C'est le contexte pour la gestion logistique : le parc de vehicules (charroi), le magasin de pieces de rechange, et les demandes de materiel. Quand vous basculez vers ce contexte, les modules changent pour :
- Tableau de Bord (logistique)
- Charroi
- Magasin
- Demandes

L'icone est un camion vert sur fond vert clair.

### Comment basculer entre les contextes

Le selecteur de contexte est le petit encadre juste sous le logo dans la barre laterale. Il montre le contexte actuel (par defaut "Maintenance GE"). Pour changer :

1. Cliquez sur le selecteur
2. Un menu deroulant s'ouvre avec les 3 contextes disponibles
3. Cliquez sur le contexte que vous voulez
4. La barre laterale se met a jour immediatement avec les modules correspondants

Le contexte actif est mis en surbrillance dans le menu deroulant. C'est un systeme fluide : pas besoin de recharger la page, tout change instantanement.

---

## 5.3 Liste de tous les modules

Voici la liste complete de tous les modules accessibles dans l'application, organises par contexte metier.

### Contexte "Maintenance GE" (le principal)

| Module | Icone | Chemin | Description |
|--------|-------|--------|-------------|
| **Tableau de Bord** | Grille de 4 carres | `/` | Page d'accueil avec KPI, carte, alertes, graphiques |
| **Interventions** | Clef/outil | `/interventions` | Liste de toutes les interventions, creation, detail, suivi |
| **Equipements GE** | Engrenage | `/equipments` | Inventaire des groupes electrogenes, fiches detaillees |
| **Planning** | Calendrier | `/planning` | Calendrier mensuel + tableau Kanban drag & drop |
| **Clients** | Batiment | `/clients` | Liste des clients, sites, contacts, historique |
| **Equipes** | Personnes | `/teams` | Gestion des techniciens, superviseurs, chauffeurs |
| **Facturation** | Ticket/recu | `/billing` | Offres, factures, suivi des paiements, chiffre d'affaires |
| **Carte** | Carte/pin | `/map` | Carte interactive avec tous les equipements |
| **Reporting** | Graphique barres | `/reporting` | Rapports et analyses, graphiques avances |

Plus en bas de la barre laterale :
| Module | Icone | Chemin | Description |
|--------|-------|--------|-------------|
| **Notifications** | Cloche | `/notifications` | Centre de notifications |
| **Parametres** | Roue dentee | `/settings` | Profil, preferences, notifications, securite |

### Contexte "Atelier"

| Module | Icone | Chemin | Description |
|--------|-------|--------|-------------|
| **Tableau de Bord** | Grille | `/atelier` | Vue d'ensemble de l'activite atelier |
| **Ordres de Travail** | Clipboard | `/atelier/work-orders` | Liste des ordres de travail, suivi des etapes |
| **Inventaire** | Boite/package | `/atelier/inventory` | Stock de pieces de rechange, gestion des entrees/sorties |
| **Planning Atelier** | Calendrier | `/atelier/planning` | Planning des travaux en atelier |
| **Techniciens** | Personnes | `/atelier/technicians` | Equipe de l'atelier |

### Contexte "Logistique"

| Module | Icone | Chemin | Description |
|--------|-------|--------|-------------|
| **Tableau de Bord** | Grille | `/logistique` | Vue d'ensemble de la logistique |
| **Charroi** | Camion | `/logistique/charroi` | Parc de vehicules, etat, affectation, entretien |
| **Magasin** | Entrepot | `/logistique/magasin` | Stock de pieces et consommables |
| **Demandes** | Clipboard | `/logistique/demandes` | Demandes de materiel et de vehicules |

### Pages specifiques au technicien

| Page | Chemin | Description |
|------|--------|-------------|
| **Vue principale** | `/technician` | Liste des interventions assignees au technicien |
| **Mode intervention** | `/technician/intervention/:id` | Interface de travail sur une intervention (checklist, photos, etc.) |
| **Historique** | `/technician/history` | Historique des interventions terminees |
| **Profil** | `/technician/profile` | Profil du technicien |

---

## 5.4 Navigation entre les modules

Naviguer entre les modules est tres simple :

1. **Cliquez sur un module dans la barre laterale** : C'est la methode principale. Vous cliquez sur "Interventions", la page des interventions s'affiche. Vous cliquez sur "Clients", la page des clients s'affiche. Le module actif est toujours mis en surbrillance dans la barre laterale pour que vous sachiez ou vous etes.

2. **Utilisez les liens dans les pages** : Beaucoup de pages contiennent des liens vers d'autres modules. Par exemple, sur la fiche d'un client, vous pouvez voir ses equipements et cliquer sur un equipement pour aller directement a sa fiche. Ou sur la fiche d'une intervention, vous pouvez cliquer sur le nom du client pour aller a sa fiche client.

3. **Utilisez les boutons d'action rapide** : Sur le dashboard, les 4 boutons d'action rapide vous amenent directement aux modules les plus utilises.

4. **Utilisez le bouton "retour" du navigateur** : Comme dans n'importe quel site web, vous pouvez utiliser le bouton "retour" de votre navigateur (ou le geste "balayer vers la droite" sur telephone) pour revenir a la page precedente.

### Les pages de detail

Certains modules ont des **pages de detail** qui s'ouvrent quand vous cliquez sur un element specifique. Par exemple :

- Si vous etes sur la page **Interventions** (qui liste toutes les interventions) et que vous cliquez sur une intervention, vous arrivez sur la page de **detail de cette intervention** (`/interventions/INV-001` par exemple). Cette page montre toutes les informations sur cette intervention specifique.

- Si vous etes sur la page **Equipements** et que vous cliquez sur un generateur, vous arrivez sur la page de **detail de cet equipement** (`/equipments/GE-001`).

- Si vous etes sur la page **Clients** et que vous cliquez sur un client, vous arrivez sur la page de **detail de ce client** (`/clients/CL-001`).

C'est un schema de navigation classique : liste > detail. On navigue d'une vue d'ensemble vers une vue specifique.

---

## 5.5 Comportement sur mobile

Comme mentionne dans la section sur le design responsive, la navigation s'adapte sur les petits ecrans.

### Sur telephone (vue admin)

Si un administrateur ouvre l'application sur son telephone (ce qui est tout a fait possible meme si la vue admin est principalement concu pour le bureau), voici ce qui change :

1. La barre laterale est **cachee par defaut**. A la place, il y a un **en-tete fixe** en haut de l'ecran avec :
   - Un bouton "hamburger" (trois traits) a gauche pour ouvrir la barre laterale
   - Le texte "AEMI GMAO" au centre

2. Quand vous appuyez sur le bouton hamburger, la barre laterale **s'ouvre en superposition** sur le contenu. Un fond sombre semi-transparent apparait derriere pour indiquer que c'est un panneau en superposition. Vous pouvez :
   - Cliquer sur un module pour naviguer (la barre laterale se ferme automatiquement)
   - Cliquer sur le fond sombre pour fermer la barre laterale sans naviguer
   - Appuyer sur le bouton "X" qui remplace le bouton hamburger pour fermer

3. Le contenu de chaque page s'empile verticalement au lieu d'etre en colonnes. Les cartes KPI sont 2 par ligne, les sections qui etaient cote a cote passent les unes sous les autres, etc.

### Sur telephone (vue technicien)

La vue technicien est **nativement concu pour le telephone**. Elle a sa propre mise en page (MobileLayout) qui est differente de la mise en page admin :

- Un en-tete fixe en haut avec le logo AEMI, le nom du technicien, la date, l'indicateur GPS et un bouton de rafraichissement
- Le contenu principal qui defile en dessous
- Une barre de navigation en bas de l'ecran (comme dans une application mobile classique) avec des onglets pour : Taches, Historique, Profil

La vue technicien n'a pas de barre laterale. C'est une interface completement differente, pensee pour etre utilisee avec une seule main sur un telephone de chantier.

---

## 5.6 Le module ExplorIA

Il y a un element dans l'application qui merite une mention speciale : le lien vers **ExplorIA**, l'agence qui a developpe l'application.

ExplorIA est l'agence web et technologique derriere le developpement de AEMI GMAO. Si vous cherchez dans l'application, vous trouverez un lien ou un module qui presente ExplorIA et ses services.

Pour la petite anecdote technique, le site de presentation d'ExplorIA dans l'application a ete concu avec un style **neo-brutaliste** (un style de design moderne qui utilise des bordures marquees, des ombres portees, et des elements graphiques expressifs). Il est compose d'au moins 5 sections detaillees, avec des animations fluides et des micro-interactions. Il est entierement responsive (il s'adapte a tous les ecrans) et a ete pense pour donner une impression professionnelle et serieuse, tout en ayant des petits details surprenants (des "easter eggs") qui rendent la navigation agreable.

Le prompt qui a ete utilise pour generer ce site etait :

> *"create a nice looking saas, neobrutalist, atleast 5 sections, detailed, animated, should look professional and serious saas make it fluid responsive with micro interactions and easter eggs that make user awe with the details 1. Use tailwind 2. Make sure each section is long and detailed, don't make a generic shitty website, I need production ready"*

Ce site utilise **Tailwind CSS** pour le style, ce qui est la meme technologie utilisee pour l'ensemble de l'application AEMI GMAO. Il a ete concu pour etre fluide, reactif, et pour donner une bonne premiere impression aux visiteurs qui souhaitent en savoir plus sur l'agence derriere le projet.

---

# Fin de la Partie 1

Voila Clement, c'est tout pour cette premiere partie. On a couvert :

1. **L'introduction** : ce qu'est l'application, a quoi elle sert, comment elle est structuree
2. **L'installation** : comment mettre l'application sur votre telephone ou votre ordinateur, que ce soit Android, iPhone ou PC
3. **La connexion** : les identifiants de test, les differents roles, comment passer d'un compte a l'autre
4. **Le dashboard** : chaque element du tableau de bord en detail (KPI, carte, graphiques, alertes)
5. **La navigation** : la barre laterale, les contextes metier, tous les modules disponibles

Dans les parties suivantes, on va entrer dans le detail de chaque module individuellement : les interventions, les equipements, les clients, le planning, la facturation, l'atelier, la logistique, le reporting, etc.

N'hesitez pas a me faire vos retours sur cette premiere partie. Si quelque chose n'est pas clair, si vous voulez que j'approfondisse un point, ou si vous avez des suggestions de modification, je suis a votre ecoute.

---

*Document prepare par ExplorIA pour AEMI / Forrest Groupe*
*Version 1.0 - Fevrier 2026*
*Confidentiel - Usage interne uniquement*
# AEMI GMAO - Documentation de Presentation - PARTIE 2

## Modules d'Administration : Interventions, Clients, Equipements & Planning

**Prepare par :** ExplorIA
**Destinataire :** Clement
**Application :** AEMI GMAO - https://aemi-gmao.vercel.app
**Date :** Fevrier 2026
**Version :** 2.0

---

> Clement, cette deuxieme partie de la documentation se concentre sur les modules que vous utiliserez au quotidien pour gerer les operations d'AEMI. On va passer en revue chaque ecran, chaque bouton, chaque fonctionnalite, avec des exemples tires des donnees de demonstration. L'objectif est que vous puissiez utiliser l'application de maniere autonome apres avoir lu ce document.

---

# 6. Module Interventions

Le module Interventions est le coeur de l'application AEMI GMAO. C'est ici que tout se passe : creation des missions, suivi en temps reel, validation, et facturation. Chaque intervention represente une mission sur le terrain -- qu'il s'agisse d'un entretien preventif, d'une reparation d'urgence, d'un diagnostic, ou d'une installation de groupe electrogene.

Ce module est concu pour vous donner une vision complete de toutes les operations en cours et passees, et pour faciliter la coordination entre l'equipe administrative (vous, Clement), les superviseurs, les techniciens sur le terrain, et les chauffeurs.

---

## 6.1 Vue d'ensemble : Liste des Interventions

Quand vous cliquez sur "Interventions" dans le menu de gauche, vous arrivez sur la page principale du module. Cette page est organisee en trois zones distinctes :

1. **L'en-tete** avec le titre et le bouton de creation
2. **Les cartes KPI** qui donnent un apercu rapide de la situation
3. **Le tableau** avec la liste de toutes les interventions

### 6.1.1 Les Cartes KPI (Indicateurs Rapides)

En haut de la page, trois cartes vous donnent un resume instantane :

| Carte | Couleur | Ce qu'elle montre | Exemple |
|-------|---------|-------------------|---------|
| **En retard** | Rouge | Nombre d'interventions dont la date prevue est depassee et qui ne sont pas encore terminees | 1 intervention en retard |
| **En cours** | Orange/Ambre | Nombre d'interventions actuellement en cours de traitement sur le terrain | 3 interventions en cours |
| **Total** | Bleu | Nombre total d'interventions dans le systeme | 13 interventions au total |

Ces cartes sont cliquables. Par exemple, si vous cliquez sur "En retard", le tableau se filtre automatiquement pour ne montrer que les interventions en retard. Vous cliquez a nouveau pour revenir a l'affichage complet.

**Exemple pratique :** Clement, imaginez qu'un lundi matin vous ouvrez l'application. Vous voyez "2" en rouge sur la carte "En retard". Vous cliquez dessus et vous decouvrez que la reparation chez Brasserie de Kinshasa et le diagnostic chez Hotel du Fleuve n'ont pas ete traites. Vous pouvez alors agir immediatement.

### 6.1.2 La Barre de Recherche et les Filtres

Juste en dessous des cartes KPI, vous avez une barre de recherche et trois menus deroulants pour filtrer les interventions.

**La barre de recherche** permet de chercher par :
- Nom du client (ex : taper "Brasserie" pour trouver les interventions de la Brasserie de Kinshasa)
- Description de l'intervention (ex : taper "batterie" pour trouver les interventions liees a la batterie)
- Identifiant de l'intervention (ex : taper les premiers caracteres de l'ID)
- Nom du technicien assigne (ex : taper "Patrick" pour voir les missions de Patrick Ilunga)

**Les menus deroulants :**

| Filtre | Options disponibles | Utilite |
|--------|-------------------|---------|
| **Statut** | Tous les statuts, Creee, Planifiee, Affectee, En route, Sur site, En cours, En attente, Terminee, Validee, A facturer, Facturee | Filtrer par etape du workflow |
| **Priorite** | Toutes, Basse, Normale, Haute, Urgente | Voir uniquement les urgences, par exemple |
| **Type** | Tous, Manutention, Installation, Constat, Entretien, Reparation | Filtrer par nature de l'intervention |

**Exemple pratique :** Vous voulez voir toutes les reparations urgentes qui ne sont pas encore terminees. Vous selectionnez "Reparation" dans le filtre Type, "Urgente" dans Priorite, et vous pouvez encore affiner en cherchant un client specifique dans la barre de recherche.

### 6.1.3 Le Tableau des Interventions

Le tableau est la partie principale de la page. Voici les colonnes affichees :

| Colonne | Description | Exemple |
|---------|-------------|---------|
| **ID** | Identifiant unique (8 premiers caracteres) | `a3f2b8c1` |
| **Client** | Nom du client concerne | Brasserie de Kinshasa |
| **Type** | Nature de l'intervention (badge avec bordure) | Reparation, Entretien, Installation... |
| **Priorite** | Niveau d'urgence (badge colore) | Urgente (rouge), Haute (orange), Normale (bleu), Basse (gris) |
| **Statut** | Etape actuelle dans le workflow (badge colore) | Creee, En cours, Terminee... |
| **Techniciens** | Prenom(s) du ou des techniciens assignes | Patrick, Jean-Pierre |
| **Date prevue** | Date planifiee pour l'intervention | 15/02/2026 |
| **Description** | Texte descriptif (tronque si trop long) | Panne totale - le groupe ne demarre plus... |
| **Actions** | Bouton poubelle pour supprimer | Icone poubelle |

**Le code couleur des priorites :**

| Priorite | Couleur du badge | Signification |
|----------|-----------------|---------------|
| Urgente | Rouge avec fond rouge clair | Intervention a traiter immediatement, production impactee |
| Haute | Orange avec fond orange clair | Intervention prioritaire, a planifier dans les 24-48h |
| Normale | Bleu avec fond bleu clair | Intervention standard, a planifier dans la semaine |
| Basse | Gris avec fond gris clair | Intervention non urgente, peut attendre |

**Le code couleur des statuts :**

| Statut | Couleur | Signification |
|--------|---------|---------------|
| Creee | Gris | L'intervention vient d'etre creee, pas encore planifiee |
| Planifiee | Bleu | Une date et une heure ont ete definies |
| Affectee | Indigo/Violet | Un ou plusieurs techniciens ont ete assignes |
| En route | Cyan | Le technicien est en route vers le site |
| Sur site | Bleu-vert | Le technicien est arrive sur le site client |
| En cours | Ambre/Orange | Les travaux sont en cours |
| En attente | Orange | L'intervention est en pause (attente de piece, decision client...) |
| Terminee | Vert | Le technicien a fini le travail |
| Validee | Vert fonce | L'administrateur a valide le rapport |
| A facturer | Violet | L'intervention est validee et attend d'etre facturee |
| Facturee | Gris ardoise | La facture a ete emise |

**Les interventions en retard** sont mises en evidence avec un fond rouge clair dans le tableau. Vous les repererez immediatement.

### 6.1.4 Le Tri des Colonnes

Vous pouvez trier le tableau en cliquant sur les en-tetes de certaines colonnes. Les colonnes triables sont :

- **Type** : tri alphabetique par type d'intervention
- **Priorite** : tri par niveau de priorite
- **Statut** : tri par etape du workflow
- **Date prevue** : tri chronologique (par defaut, les plus recentes d'abord)

Un petit indicateur (fleche vers le haut ou vers le bas) apparait a cote de la colonne sur laquelle vous triez. Cliquez une fois pour trier dans un sens, cliquez a nouveau pour inverser l'ordre.

### 6.1.5 La Pagination

En bas du tableau, vous avez les controles de pagination :

- Le nombre total d'elements affiches (ex : "1-10 sur 13")
- Le nombre d'elements par page (par defaut 10, modifiable)
- Des boutons pour naviguer entre les pages (page precedente, page suivante)

Si vous avez 25 interventions et que vous affichez 10 par page, vous aurez 3 pages. Les boutons "precedent" et "suivant" permettent de naviguer facilement.

### 6.1.6 Navigation vers le Detail

Chaque ligne du tableau est cliquable. En cliquant sur une intervention, vous etes redirige vers la page de detail de cette intervention (voir section 6.3). C'est le moyen principal pour acceder aux informations completes d'une intervention.

---

## 6.2 Creer une Intervention

### 6.2.1 Ouvrir le Formulaire

Pour creer une nouvelle intervention :

1. Rendez-vous sur la page "Interventions"
2. Cliquez sur le bouton **"Nouvelle Intervention"** en haut a droite (bouton bleu avec un "+")
3. Une fenetre de dialogue s'ouvre avec le formulaire de creation

### 6.2.2 Remplir le Formulaire - Etape par Etape

Le formulaire de creation comporte plusieurs champs organises en sections :

**Section 1 : Client et Equipement (2 champs cote a cote)**

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Client** | Menu deroulant | Selectionnez le client parmi la liste | Oui |
| **Equipement** | Menu deroulant | Selectionnez le groupe electrogene concerne | Oui |

Quand vous selectionnez un client, la liste des equipements se met a jour automatiquement pour ne montrer que les groupes electrogenes de ce client.

**Exemple :** Si vous selectionnez "Brasserie de Kinshasa", le menu Equipement vous proposera "Groupe Electrogene Principal (Caterpillar C15, 500 kVA)" et "Generateur Backup (Perkins 4000 Series, 600 kVA)".

**Section 2 : Type, Priorite, Date (3 champs cote a cote)**

| Champ | Type | Options | Obligatoire |
|-------|------|---------|-------------|
| **Type** | Menu deroulant | Manutention, Installation, Constat, Entretien, Reparation | Oui |
| **Priorite** | Menu deroulant | Basse, Normale, Haute, Urgente | Oui (Normale par defaut) |
| **Date prevue** | Selecteur de date | Calendrier | Oui (date du jour par defaut) |

**Section 3 : Heure et Duree (2 champs cote a cote)**

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Heure prevue** | Selecteur d'heure | Heure de debut prevue (format HH:MM) | Non |
| **Duree estimee (min)** | Champ numerique | Duree prevue en minutes (ex : 120 pour 2h) | Non |

**Section 4 : Description**

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Description** | Zone de texte | Decrivez l'intervention, les symptomes, le contexte | Non mais recommande |

C'est ici que vous ecrivez ce que le technicien doit savoir. Soyez precis.

**Exemple de bonne description :** "Le client signale un bruit anormal au demarrage depuis 3 jours. Le groupe fonctionne mais avec un rendement diminue. Le client a note une fumee noire plus dense que d'habitude. Acces par le portail principal, demander Joseph Mukendi."

**Section 5 : Techniciens assignes**

Cette section affiche la liste des techniciens disponibles avec des cases a cocher. Pour chaque technicien, vous voyez :
- Son nom complet
- Ses competences (ex : "GE Caterpillar, Electricite BT")

Vous pouvez selectionner un ou plusieurs techniciens. Si vous selectionnez au moins un technicien, l'intervention passera automatiquement au statut "Affectee" au lieu de "Creee".

**Liste des techniciens de demo :**

| Technicien | Competences |
|-----------|-------------|
| Dieudonne Mutombo | GE Caterpillar, GE Perkins, Diagnostic |
| Patrick Ilunga | GE Caterpillar, Electricite BT |
| Jean-Pierre Tshombe | GE Perkins, GE Cummins, Mecanique |
| Francois Lukusa | GE Volvo, GE MTU, Installation |

Si vous assignez Patrick Ilunga et Jean-Pierre Tshombe, un petit texte vert apparait : "2 technicien(s) selectionne(s) - statut auto: Affectee".

### 6.2.3 Valider la Creation

Une fois le formulaire rempli, cliquez sur le bouton **"Creer l'intervention"** en bas de la fenetre.

L'intervention apparait alors dans le tableau avec :
- Le statut "Creee" si aucun technicien n'a ete assigne
- Le statut "Affectee" si vous avez assigne des techniciens

### 6.2.4 Exemple Complet de Creation

Voici un scenario complet, Clement. Imaginons qu'on vous appelle pour une panne urgente :

1. **Vous recevez un appel** de Jean-Marie Lumumba (Directeur Technique de la Brasserie de Kinshasa) : le groupe electrogene principal ne demarre plus, la production est a l'arret.

2. **Vous ouvrez l'application** et cliquez sur "Nouvelle Intervention"

3. **Vous remplissez le formulaire :**
   - Client : Brasserie de Kinshasa
   - Equipement : Groupe Electrogene Principal (BK-GE-001)
   - Type : Reparation
   - Priorite : Urgente
   - Date prevue : Aujourd'hui
   - Heure prevue : 10:00
   - Duree estimee : 180 (3 heures)
   - Description : "Panne totale - le groupe ne demarre plus. Production a l'arret depuis 2h. Le client signale que le demarreur ne tourne pas du tout. Batterie possiblement HS. Contacter Joseph Mukendi a l'arrivee."
   - Techniciens : Patrick Ilunga (competences Caterpillar) + Dieudonne Mutombo (superviseur)

4. **Vous cliquez sur "Creer l'intervention"**

5. L'intervention apparait dans le tableau avec un badge rouge "Urgente" et un statut violet "Affectee". Les techniciens recevront une notification sur leur application mobile.

---

## 6.3 Page de Detail d'une Intervention

Quand vous cliquez sur une ligne du tableau, vous arrivez sur la page de detail. C'est la page la plus riche de l'application.

### 6.3.1 L'En-tete de la Page

En haut de la page, vous trouvez :

- Un **fil d'ariane** : Interventions / a3f2b8c1 (pour naviguer facilement)
- Un **bouton retour** (fleche vers la gauche)
- Le **numero de l'intervention** : Intervention #a3f2b8c1
- Le **badge de statut** actuel (avec la couleur correspondante)
- Un **badge "En retard"** rouge si l'intervention est depassee
- Le **type** et la **priorite** en sous-titre (ex : "Reparation - Urgente")
- Deux boutons d'action :
  - **"Avancer le statut"** : pour faire passer l'intervention a l'etape suivante
  - **"Exporter PDF"** : pour generer un rapport PDF de l'intervention

### 6.3.2 La Frise Chronologique des Statuts

Juste en dessous de l'en-tete, une frise horizontale montre toutes les etapes du workflow :

```
Creee → Planifiee → Affectee → En route → Sur site → En cours → En attente → Terminee → Validee → A facturer → Facturee
```

Chaque etape est representee par un bloc colore :
- Les etapes passees sont en **vert** avec une coche
- L'etape actuelle est **mise en evidence** avec un anneau de couleur et un point
- Les etapes futures sont en **gris** avec un cercle vide

Cette frise vous permet de voir en un coup d'oeil ou en est l'intervention dans son cycle de vie.

### 6.3.3 Les Onglets de la Page de Detail

La page de detail est organisee en **5 onglets** :

| Onglet | Icone | Contenu |
|--------|-------|---------|
| **Details** | Document | Toutes les informations de l'intervention |
| **Checklist** | Coche | La liste de verification ISO remplie par le technicien |
| **Photos** | Appareil photo | Photos avant, pendant, et apres l'intervention |
| **Resultat** | Stylo | Diagnostic, travaux realises, recommandations, signature |
| **Historique** | Horloge | Timeline de tous les evenements |

---

#### Onglet "Details"

C'est l'onglet principal. Il est divise en deux colonnes :

**Colonne gauche (2/3 de la largeur) :**

1. **Carte "Description & Notes"** : affiche la description de l'intervention, les notes du superviseur, le diagnostic, les travaux realises, les recommandations, et la cause de la panne. Chaque bloc a un fond de couleur different :
   - Description : fond blanc
   - Notes superviseur : fond bleu clair
   - Diagnostic : fond orange clair
   - Travaux realises : fond vert clair
   - Recommandations : fond violet clair
   - Cause de la panne : fond rouge clair

2. **Carte "Equipement"** : informations sur le groupe electrogene concerne. En cliquant dessus, vous etes redirige vers la fiche technique de l'equipement.

   | Information | Exemple |
   |-------------|---------|
   | Nom | Groupe Electrogene Principal |
   | Marque / Modele | Caterpillar C15 |
   | Puissance | 500 kVA |
   | Compteur | 4750h |
   | Heures debut | 4750h (si renseigne) |
   | Heures fin | 4780h (si renseigne) |

3. **Carte "Pieces Necessaires"** (si applicable) : liste des pieces demandees avec quantite et statut de reservation.

**Colonne droite (1/3 de la largeur) :**

1. **Carte "Client & Site"** : affiche le nom du client, le site, l'adresse, et un lien Google Maps. En cliquant, vous pouvez naviguer vers la fiche client. Si le site a des coordonnees GPS, un lien "Ouvrir dans Google Maps" est disponible.

   Vous y trouverez aussi le contact principal du client avec son numero de telephone (cliquable pour appeler directement).

2. **Carte "Equipe Assignee"** : liste des techniciens assignes avec :
   - Initiales (dans un cercle colore)
   - Nom complet
   - Competences
   - Bouton telephone (pour appeler directement)
   - Bouton "Modifier" pour changer l'assignation

   Si aucun technicien n'est assigne, un message "Aucun technicien assigne" apparait avec un bouton "Assigner des techniciens".

3. **Carte "Planification"** : affiche les informations de planning :

   | Information | Valeur |
   |-------------|--------|
   | Date prevue | 15/02/2026 |
   | Heure | 08:00 |
   | Duree estimee | 3h |
   | Logistique | Pret / En attente / Non requis |
   | Transport | Pret / En attente / Non requis |

4. **Carte "Facturation"** : statut de facturation et montant si renseigne.

   | Information | Valeur |
   |-------------|--------|
   | Statut | Non facture / Facture / Paye |
   | Montant | 2 500 000 FC |

---

#### Onglet "Checklist"

La checklist est un element central du processus qualite. Elle est basee sur les standards ISO et varie selon le type d'intervention.

**En haut de la carte**, vous voyez une barre de progression et un compteur (ex : "7/10" signifie 7 elements coches sur 10).

**Chaque element de la checklist affiche :**
- Une icone verte (coche) si l'element est fait, ou rouge (cercle) si pas encore fait
- Le libelle de l'element (ex : "Niveau d'huile verifie")
- La categorie (ex : "Fluides", "Filtres", "Mecanique")
- Un badge "Requis" si l'element est obligatoire
- Un commentaire du technicien (en italique) si renseigne
- Un bouton photo si le technicien a pris une photo pour cet element

**Checklists selon le type d'intervention :**

**Checklist Entretien (Maintenance) :**

| # | Element | Categorie | Obligatoire |
|---|---------|-----------|-------------|
| 1 | Niveau d'huile verifie | Fluides | Oui |
| 2 | Filtres a air changes | Filtres | Oui |
| 3 | Filtres a huile changes | Filtres | Oui |
| 4 | Filtres a carburant verifies | Filtres | Oui |
| 5 | Tension courroies controlee | Mecanique | Oui |
| 6 | Tension batterie OK (>=12.4V) | Electrique | Oui |
| 7 | Niveau liquide refroidissement verifie | Fluides | Oui |
| 8 | Test de demarrage effectue | Fonctionnel | Oui |
| 9 | Releve compteur horaire note | Mesures | Oui |
| 10 | Nettoyage general effectue | General | Non |

**Checklist Reparation :**

| # | Element | Obligatoire |
|---|---------|-------------|
| 1 | Diagnostic effectue | Oui |
| 2 | Cause de la panne identifiee | Oui |
| 3 | Pieces remplacees documentees | Oui |
| 4 | Test de fonctionnement reussi | Oui |
| 5 | Client informe | Oui |

**Checklist Diagnostic (Constat) :**

| # | Element | Obligatoire |
|---|---------|-------------|
| 1 | Inspection visuelle complete | Oui |
| 2 | Releve compteur horaire | Oui |
| 3 | Test demarrage | Oui |
| 4 | Mesures electriques (tension, frequence) | Oui |
| 5 | Verification niveaux fluides | Oui |
| 6 | Photos avant/apres | Oui |
| 7 | Rapport remis au client | Oui |

**Checklist Installation :**

| # | Element | Obligatoire |
|---|---------|-------------|
| 1 | Emplacement verifie et conforme | Oui |
| 2 | Groupe positionne et cale | Oui |
| 3 | Raccordements electriques effectues | Oui |
| 4 | Raccordements carburant effectues | Oui |
| 5 | Mise a la terre verifiee | Oui |
| 6 | Remplissage fluides effectue | Oui |
| 7 | Test de mise en service reussi | Oui |
| 8 | Formation utilisateur dispensee | Non |
| 9 | Documentation remise au client | Oui |

**Section "Problemes Signales"** (si applicable) :

En dessous de la checklist, le technicien peut signaler des problemes rencontres pendant l'intervention. Chaque probleme a :
- Un niveau de criticite (Critique, Moyen, Mineur) avec un code couleur (rouge, orange, jaune)
- Une categorie
- Une description
- Eventuellement une photo

---

#### Onglet "Photos"

Cet onglet est organise en trois sections cote a cote :

| Section | Icone | Couleur | Description |
|---------|-------|---------|-------------|
| **Photos Avant** | Appareil photo bleu | Bleu | Photos de l'etat initial du groupe avant intervention |
| **Photos Pendant** | Cle orange | Orange | Photos prises pendant les travaux |
| **Photos Apres** | Coche verte | Vert | Photos de l'etat final apres intervention |

Chaque section affiche une grille de vignettes (2 colonnes). En cliquant sur une photo, elle s'ouvre en grand dans une fenetre modale.

Si aucune photo n'a ete prise, un espace vide avec un message "Aucune photo" est affiche.

En dessous des trois sections de photos, deux cartes supplementaires s'affichent :

- **Fiche d'Intervention** : photo de la fiche papier d'intervention (si le technicien l'a photographiee)
- **Signature Client** : signature du client capturee sur l'ecran tactile du telephone du technicien. Si la signature est presente, un message "Signe par le client" apparait en vert.

---

#### Onglet "Resultat"

Cet onglet regroupe les conclusions de l'intervention :

**Carte "Resume de l'Intervention" :**

| Section | Fond | Description |
|---------|------|-------------|
| **Travaux Realises** | Vert clair | Description detaillee de ce que le technicien a fait |
| **Diagnostic** | Orange clair | Analyse de la situation |
| **Recommandations** | Violet clair | Ce que le technicien recommande pour la suite |
| **Cause de la Panne** | Rouge clair | Si c'est une reparation, la cause identifiee |

Si un champ n'est pas encore renseigne, le texte "Pas encore renseigne par le technicien" apparait.

**Carte "Suivi Temps & Compteurs" :**

Quatre blocs d'information :

| Bloc | Description | Exemple |
|------|-------------|---------|
| Depart | Heure de depart de l'atelier | 07:15 |
| Arrivee | Heure d'arrivee sur site | 08:30 |
| Compteur Debut | Heures du groupe au debut de l'intervention | 4750h |
| Compteur Fin | Heures du groupe a la fin de l'intervention | 4780h |

Si l'intervention est terminee, la duree totale est calculee et affichee en vert (ex : "3.5h").

**Carte "Etat de Completion" :**

Un tableau de bord montrant ce qui est fait et ce qui reste :

| Element | Statut | Badge |
|---------|--------|-------|
| Checklist | 7/10 | Orange si incomplete, vert si complete |
| Photos | 5 photos | Vert si >0, gris sinon |
| Signature | Signe / Non signe | Vert si signe, rouge sinon |
| Fiche intervention | Archivee / Non | Vert si archivee, gris sinon |
| Travaux decrits | Oui / Non | Vert si oui, gris sinon |

---

#### Onglet "Historique"

L'historique affiche une timeline verticale de tous les evenements lies a l'intervention, dans l'ordre chronologique :

| Evenement | Icone | Couleur | Exemple de date |
|-----------|-------|---------|-----------------|
| Intervention creee | Document | Gris | 12 fevrier 2026, 09:15 |
| Planifiee | Calendrier | Bleu | 12 fevrier 2026, 09:30 |
| Assignee a Patrick Ilunga, Dieudonne Mutombo | Personne | Indigo | 12 fevrier 2026, 10:00 |
| Depart vers le site | Camion | Cyan | 13 fevrier 2026, 07:15 |
| Arrivee sur site | Pin | Bleu-vert | 13 fevrier 2026, 08:30 |
| Debut des travaux | Lecture | Ambre | 13 fevrier 2026, 08:45 |
| Intervention terminee | Coche | Vert | 13 fevrier 2026, 12:15 |
| Validee par Dieudonne Mutombo | Oeil | Vert emeraude | 13 fevrier 2026, 14:00 |
| Facturee - 2 500 000 FC | Dollar | Violet | 14 fevrier 2026, 10:00 |

Chaque evenement montre la date et l'heure exactes, ce qui permet de tracer precisement le deroulement de l'intervention.

---

## 6.4 Modifier et Supprimer une Intervention

### 6.4.1 Modifier le Statut

Sur la page de detail, le bouton **"Avancer le statut"** permet de faire passer l'intervention a l'etape suivante.

En cliquant sur ce bouton :
1. Une fenetre de dialogue s'ouvre
2. Un menu deroulant propose les statuts suivants possibles
3. Vous pouvez ajouter une note optionnelle
4. Cliquez sur "Confirmer" pour valider le changement

Les transitions possibles dependent du statut actuel :

| Statut actuel | Statuts suivants possibles |
|---------------|---------------------------|
| Creee | Planifiee |
| Planifiee | Affectee |
| Affectee | En route |
| En route | Sur site |
| Sur site | En cours |
| En cours | En attente, Terminee |
| En attente | En cours |
| Terminee | Validee |
| Validee | A facturer |
| A facturer | Facturee |

Certaines transitions declenchent des actions automatiques :
- Passer a "En cours" enregistre la date/heure de debut
- Passer a "Terminee" enregistre la date/heure de fin
- Passer a "Validee" enregistre qui a valide et quand

### 6.4.2 Modifier l'Assignation des Techniciens

Sur la page de detail, dans la carte "Equipe Assignee", cliquez sur le bouton **"Modifier"** :

1. Une fenetre de dialogue s'ouvre
2. La liste des techniciens disponibles s'affiche avec des cases a cocher
3. Les techniciens deja assignes sont pre-coches
4. Cochez ou decochez selon vos besoins
5. Cliquez sur "Confirmer l'assignation"

Si l'intervention etait au statut "Creee" ou "Planifiee" et que vous assignez des techniciens, le statut passera automatiquement a "Affectee".

### 6.4.3 Supprimer une Intervention

Pour supprimer une intervention :

1. Dans le tableau de la liste des interventions, cliquez sur l'icone **poubelle** dans la colonne Actions
2. Une fenetre de confirmation apparait : "Supprimer cette intervention - Cette action est irreversible. Le rapport et l'historique seront perdus."
3. Cliquez sur **"Supprimer"** (bouton rouge) pour confirmer, ou **"Annuler"** pour revenir en arriere

Attention : la suppression est definitive. Toutes les donnees de l'intervention (checklist, photos, signature, historique) seront perdues.

### 6.4.4 Exporter en PDF

Sur la page de detail, le bouton **"Exporter PDF"** genere un document PDF contenant toutes les informations de l'intervention : les details, la checklist, le resultat, les informations client et equipement.

Ce PDF peut etre envoye au client, archive, ou imprime pour les dossiers papier.

---

## 6.5 Workflow Complet d'une Intervention

Voici le cycle de vie complet d'une intervention, du debut a la fin, avec un exemple detaille utilisant les donnees de demonstration.

### Scenario : Maintenance Preventive 250h - Ambassade de France

**Contexte :** Le generateur Perkins 2000 Series de l'Ambassade de France a Kinshasa approche des 250 heures de fonctionnement. Une maintenance preventive doit etre planifiee.

---

**Etape 1 : Creation de l'intervention (Statut : Creee)**

*Qui : Clement (administrateur)*

Clement ouvre l'application et cree une nouvelle intervention :
- Client : Ambassade de France
- Equipement : Generateur Secours (PER-2020-2K-005678)
- Type : Entretien
- Priorite : Haute (le client est une ambassade, la fiabilite est importante)
- Date prevue : Demain
- Heure : 08:00
- Duree estimee : 180 min (3 heures)
- Description : "Maintenance preventive 250h programmee. Verifier niveaux fluides, changer filtres, controler batterie. Penser a apporter filtres Perkins references PER-CH11038 et PER-2654407."

L'intervention apparait dans le tableau avec le statut gris "Creee".

---

**Etape 2 : Planification et Assignation (Statut : Planifiee puis Affectee)**

*Qui : Clement (administrateur)*

Clement ouvre le detail de l'intervention et :
1. Clique sur "Avancer le statut" pour passer a "Planifiee"
2. Clique sur "Modifier" dans la carte "Equipe Assignee"
3. Selectionne Patrick Ilunga (competences : GE Caterpillar, mais aussi forme Perkins)
4. Selectionne Michel Kalala comme chauffeur (dans les parametres de logistique)

Le statut passe automatiquement a "Affectee" (badge violet).

---

**Etape 3 : Le technicien prend connaissance de la mission**

*Qui : Patrick Ilunga (technicien, application mobile)*

Patrick ouvre son application mobile et voit la nouvelle intervention assignee. Il consulte les details : client, adresse, equipement, description. Il se prepare en verifiant qu'il a les pieces necessaires dans son stock.

---

**Etape 4 : Depart vers le site (Statut : En route)**

*Qui : Patrick Ilunga (via application mobile)*

Le lendemain matin, Patrick monte dans le vehicule avec Michel (chauffeur). Il glisse le statut sur "En route" dans son application mobile. L'heure de depart est automatiquement enregistree : 07:30.

---

**Etape 5 : Arrivee sur site (Statut : Sur site)**

*Qui : Patrick Ilunga (via application mobile)*

A 08:15, Patrick arrive a l'Ambassade de France. Il passe le controle de securite (piece d'identite obligatoire, comme indique dans les contraintes d'acces du site). Il glisse le statut sur "Sur site". L'heure d'arrivee est enregistree.

---

**Etape 6 : Debut des travaux (Statut : En cours)**

*Qui : Patrick Ilunga (via application mobile)*

Patrick commence par prendre des photos de l'etat initial du generateur (photos "Avant"). Il note le compteur horaire actuel : 2340h. Il passe le statut a "En cours".

Il remplit ensuite la checklist point par point :
- Niveau d'huile verifie (coche)
- Filtres a air changes (coche, il prend une photo du filtre use)
- Filtres a huile changes (coche)
- Filtres a carburant verifies (coche)
- Tension courroies controlee (coche, il note "Legere usure cote moteur")
- Tension batterie OK (coche, il mesure 12.8V)
- Niveau liquide refroidissement verifie (coche)
- Test de demarrage effectue (coche)
- Releve compteur horaire note (coche, 2340h)
- Nettoyage general effectue (coche)

Il prend des photos pendant les travaux (photos "Pendant") et des photos de l'etat final (photos "Apres").

---

**Etape 7 : Fin des travaux et signature (Statut : Terminee)**

*Qui : Patrick Ilunga (via application mobile)*

Patrick remplit la section "Resultat" :
- Travaux realises : "Vidange huile moteur effectuee (35L Shell Rimula R4 15W-40). Remplacement filtre a air ref PER-CH11038. Remplacement filtre a huile ref PER-2654407. Courroies controlees - usure legere cote moteur, remplacement a prevoir sous 100h. Batterie OK a 12.8V. Test de demarrage reussi."
- Recommandations : "Prevoir remplacement courroie dans les 100 prochaines heures. Prochain entretien a 2500h."

Il fait signer Pierre Dubois (Attache Technique de l'ambassade) sur l'ecran tactile de son telephone. La signature est enregistree.

Il prend une photo de la fiche d'intervention papier.

Il passe le statut a "Terminee". L'heure de fin est enregistree : 11:45.

---

**Etape 8 : Validation par l'administrateur (Statut : Validee)**

*Qui : Clement (administrateur)*

De retour au bureau, Clement ouvre le detail de l'intervention terminee. Il verifie :
- La checklist est complete (10/10)
- Les photos sont presentes (avant, pendant, apres)
- La signature du client est la
- Les travaux sont bien decrits

Tout est en ordre. Il clique sur "Avancer le statut" et selectionne "Validee". Le systeme enregistre que Clement a valide l'intervention et a quelle heure.

---

**Etape 9 : Facturation (Statut : A facturer puis Facturee)**

*Qui : Clement ou l'equipe administrative*

Clement passe le statut a "A facturer". L'equipe comptable prepare la facture dans le module Facturation (module couvert dans la Partie 3 de cette documentation).

Une fois la facture emise, le statut passe a "Facturee" et le cycle est termine.

---

### Resume du Workflow en Tableau

| Etape | Statut | Qui agit | Ou | Action principale |
|-------|--------|----------|-----|-------------------|
| 1 | Creee | Admin (Clement) | Application web | Creation de l'intervention |
| 2 | Planifiee | Admin | Application web | Definir date, heure, duree |
| 3 | Affectee | Admin | Application web | Assigner technicien(s) |
| 4 | En route | Technicien | Application mobile | Signaler le depart |
| 5 | Sur site | Technicien | Application mobile | Signaler l'arrivee |
| 6 | En cours | Technicien | Application mobile | Remplir checklist, photos |
| 7 | Terminee | Technicien | Application mobile | Rapport, signature client |
| 8 | Validee | Admin | Application web | Verifier et valider |
| 9 | A facturer | Admin | Application web | Preparer la facture |
| 10 | Facturee | Admin | Application web | Facture emise |

---

## 6.6 Les Differents Types d'Interventions

### 6.6.1 Entretien (Maintenance)

La maintenance preventive est le type d'intervention le plus courant. Elle est declenchee quand un groupe electrogene atteint un certain nombre d'heures de fonctionnement.

**Les seuils de maintenance :**

| Seuil | Designation | Operations typiques |
|-------|------------|---------------------|
| 250h | Entretien courant | Vidange huile, remplacement filtre a huile, verification courroies |
| 500h | Entretien intermediaire | Tout le 250h + remplacement filtre a air, filtre gasoil, verification alternateur |
| 1000h | Entretien majeur | Tout le 500h + remplacement liquide refroidissement, inspection complete moteur, calibration regulateur |

Quand une intervention de maintenance est creee, le champ "Type de maintenance" (250h, 500h, 1000h) est affiche dans les details et sur la frise.

### 6.6.2 Reparation

Les reparations sont declenchees suite a une panne ou un dysfonctionnement. Le technicien doit identifier la cause de la panne parmi les causes connues :

| Cause de panne | Description |
|----------------|-------------|
| Surchauffe moteur | Le moteur a depasse sa temperature normale de fonctionnement |
| Defaillance batterie | La batterie ne fournit plus assez de courant pour le demarrage |
| Filtre colmate | Un filtre (air, huile, carburant) est sature et bloque le flux |
| Fuite carburant | Une fuite est detectee dans le circuit carburant |
| Probleme demarreur | Le demarreur ne fonctionne plus correctement |
| Alternateur defectueux | L'alternateur ne produit plus de courant |
| Courroie usee | Une ou plusieurs courroies sont usees ou cassees |
| Capteur defaillant | Un capteur electronique ne fonctionne plus |
| Panne electrique | Probleme dans le circuit electrique du groupe |
| Manque huile | Le niveau d'huile est trop bas |

### 6.6.3 Constat (Diagnostic)

Un constat est une visite d'inspection pour evaluer l'etat d'un groupe electrogene sans forcement intervenir. Il aboutit a un rapport avec des recommandations.

### 6.6.4 Installation

Une installation concerne la mise en place d'un nouveau groupe electrogene sur un site client. C'est generalement une operation longue (une journee entiere) qui mobilise plusieurs techniciens.

### 6.6.5 Manutention

La manutention concerne le deplacement physique d'un groupe electrogene (ex : d'un site a un autre, ou dans un atelier).

---

## 6.7 Gestion de la Logistique et du Transport

Chaque intervention peut necessiter :

**Logistique (pieces et materiaux) :**
- Quand vous creez une intervention, vous pouvez activer l'option "Logistique necessaire"
- Le service logistique prepare les pieces (filtres, huile, courroies...)
- Quand tout est pret, le badge passe de "En attente" a "Pret"

**Transport (chauffeur et vehicule) :**
- Vous pouvez activer l'option "Chauffeur necessaire"
- Le chauffeur est assigne avec un vehicule
- Quand le chauffeur est disponible, le badge passe de "En attente" a "Pret"

Ces informations sont visibles dans la carte "Planification" de la page de detail.

---

# 7. Module Clients

Le module Clients vous permet de gerer l'ensemble des clients d'AEMI et leurs informations : coordonnees, contacts, sites, et historique des interventions.

---

## 7.1 Liste des Clients

En cliquant sur "Clients" dans le menu de gauche, vous arrivez sur la page principale du module.

### 7.1.1 Les Cartes KPI

En haut de la page, quatre cartes affichent les statistiques :

| Carte | Icone | Valeur de demo | Description |
|-------|-------|----------------|-------------|
| Total clients | Groupe de personnes | 6 | Nombre total de clients enregistres |
| Entreprises | Batiment | 6 | Nombre de comptes entreprise |
| Particuliers | Personne | 0 | Nombre de comptes particulier |
| Sites | Pin | 8 | Nombre total de sites clients |

### 7.1.2 La Barre de Recherche et les Filtres

La barre de recherche permet de chercher par :
- Nom du client (ex : "Mining" pour trouver Mining Corp International)
- Adresse (ex : "Lubumbashi" pour les clients de Lubumbashi)
- Type (ex : "company")

Les boutons de filtre par type :
- **Tous** : affiche tous les clients
- **Entreprise** : filtre uniquement les entreprises
- **Particulier** : filtre uniquement les particuliers

### 7.1.3 Le Tri

Vous pouvez trier la liste par :
- **Nom** : ordre alphabetique
- **Adresse** : ordre alphabetique par adresse
- **Type** : entreprise puis particulier (ou inversement)
- **Sites** : nombre de sites (du plus au moins, ou inversement)

### 7.1.4 L'Affichage en Cartes

Les clients sont affiches sous forme de cartes (et non de tableau). Chaque carte montre :

- Le **nom du client** en gras
- Un **badge "Entreprise" ou "Particulier"**
- Une icone **globe** si le client a acces au portail
- L'**adresse** du client
- Le nombre de **contacts** et de **sites**
- Un bouton **"Voir les contacts"** qui deplie la liste des contacts

### 7.1.5 Les Clients de Demonstration

Voici les clients presents dans la version de demonstration :

| Nom | Type | Adresse | Contacts | Sites | Portail |
|-----|------|---------|----------|-------|---------|
| Brasserie de Kinshasa | Entreprise | 123 Boulevard du 30 Juin, Gombe, Kinshasa | 2 | 2 | Oui |
| Ambassade de France | Entreprise | 97 Avenue de la Justice, Gombe, Kinshasa | 1 | 1 | Oui |
| Hotel du Fleuve | Entreprise | 45 Avenue du Port, Ngaliema, Kinshasa | 2 | 1 | Non |
| Mining Corp International | Entreprise | Zone Industrielle, Lubumbashi | 3 | 2 | Oui |
| Cimenterie Nationale | Entreprise | Route de Matadi, Bas-Congo | 1 | 1 | Non |
| Raffinerie Petroliere | Entreprise | Port de Moanda, Muanda | 2 | 1 | Oui |

### 7.1.6 Pagination

Comme pour les interventions, la pagination est disponible en bas de la liste avec 10 elements par page par defaut.

---

## 7.2 Creer un Client

### 7.2.1 Ouvrir le Formulaire

Cliquez sur le bouton **"Nouveau client"** en haut a droite de la page Clients.

### 7.2.2 Remplir le Formulaire - Etape par Etape

Le formulaire est divise en deux sections :

**Section 1 : Informations du client**

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Nom du client** | Texte | Nom de l'entreprise ou du particulier | Oui |
| **Type** | Menu deroulant | Entreprise ou Particulier | Oui |
| **Adresse** | Texte | Adresse complete | Non |
| **Acces portail client** | Interrupteur | Permettre au client de se connecter au portail | Non (desactive par defaut) |

L'interrupteur "Acces portail client" est un toggle on/off. Quand il est active, le client pourra se connecter au portail client pour suivre ses interventions et ses equipements.

**Section 2 : Contact principal (optionnel)**

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Nom** | Texte | Nom du contact principal | Non |
| **Fonction** | Texte | Fonction dans l'entreprise (ex : Directeur Technique) | Non |
| **Telephone** | Texte | Numero de telephone | Non |
| **Email** | Email | Adresse email | Non |

### 7.2.3 Valider la Creation

Cliquez sur **"Creer le client"** pour enregistrer. Le client apparait immediatement dans la liste.

### 7.2.4 Exemple de Creation

Vous recevez un nouveau client, une mine de cuivre a Kolwezi. Voici comment vous le creez :

1. Cliquez sur "Nouveau client"
2. Remplissez :
   - Nom : Kolwezi Copper Mining
   - Type : Entreprise
   - Adresse : Route de Likasi, Zone Miniere, Kolwezi
   - Acces portail : Active
   - Contact : David Thompson, Operations Director, +243 97 222 3333, d.thompson@kcmining.com
3. Cliquez sur "Creer le client"

Le nouveau client apparait dans la liste avec un badge "Entreprise" et l'icone globe (portail actif).

---

## 7.3 Detail d'un Client

En cliquant sur une carte client dans la liste, vous etes redirige vers la page de detail du client.

### 7.3.1 L'En-tete

L'en-tete affiche :
- Le fil d'ariane : Clients / Mining Corp International
- Le nom du client en grand
- Un badge "Entreprise" ou "Particulier"
- Un badge "Portail actif" si le client a acces au portail

### 7.3.2 Les Cartes KPI du Client

Six cartes de statistiques specifiques au client :

| Carte | Description | Exemple (Mining Corp) |
|-------|-------------|----------------------|
| Total equipements | Nombre de groupes electrogenes | 5 |
| Operationnels | Groupes en etat de marche | 3 |
| En panne | Groupes en panne | 1 |
| Total interventions | Nombre d'interventions | 4 |
| Interventions actives | Interventions non terminees | 2 |
| Total facture | Montant total des factures | 6 000 000 FC |

### 7.3.3 Les Onglets

La page de detail du client comporte plusieurs onglets :

**Onglet "Informations" :**

- Informations generales : nom, type, adresse
- Acces portail
- Date de creation du compte

**Onglet "Contacts" :**

Affiche tous les contacts du client sous forme de cartes :

| Nom | Fonction | Telephone | Email |
|-----|----------|-----------|-------|
| James Wilson | Operations Manager | +243 97 111 2222 | j.wilson@miningcorp.com |
| Albert Kasongo | Maintenance Manager | +243 97 111 3333 | a.kasongo@miningcorp.com |
| Sophie Tshilombo | Admin | +243 97 111 4444 | s.tshilombo@miningcorp.com |

Chaque contact a un bouton telephone et un bouton email pour un acces rapide.

**Onglet "Sites" :**

Liste des sites du client avec :

| Site | Adresse | Localite | Contraintes d'acces |
|------|---------|----------|---------------------|
| Mine Site Alpha | Zone Industrielle Nord | Lubumbashi | Zone industrielle, EPI obligatoires, escorte requise |
| Mine Site Beta | Zone Industrielle Sud | Lubumbashi | - |

Chaque site affiche aussi ses coordonnees GPS et un lien pour ouvrir Google Maps.

Les contacts specifiques au site sont aussi affiches. Par exemple, le Site Alpha a :
- Robert Mulongo : +243 97 000 0001
- Grace Ilunga : +243 97 000 0002

**Onglet "Equipements" :**

Liste des groupes electrogenes du client avec :

| Reference | Equipement | Marque/Modele | Puissance | Statut | Heures |
|-----------|-----------|---------------|-----------|--------|--------|
| MCI-ALPHA-001 | Groupe Industriel | Caterpillar C18 | 750 kVA | En panne | 5680h |
| MCI-ALPHA-002 | Groupe Secours Alpha | Cummins KTA50 | 1500 kVA | Operationnel | 2800h |
| MCI-ALPHA-003 | Groupe Mobile | Caterpillar C9 | 300 kVA | En intervention | 980h |
| MCI-BETA-001 | Groupe Principal Beta | Caterpillar C32 | 1100 kVA | Entretien requis | 4100h |
| MCI-BETA-002 | Groupe Secours Beta | Perkins 4000 Series | 800 kVA | Operationnel | 2100h |

En cliquant sur un equipement, vous etes redirige vers sa fiche technique complete.

**Onglet "Interventions" :**

Historique complet des interventions pour ce client, triees par date (les plus recentes en premier). Chaque intervention montre :
- Le type (Reparation, Entretien, etc.)
- Le statut
- La date prevue
- La description

En cliquant sur une intervention, vous etes redirige vers sa page de detail.

---

## 7.4 Gestion des Contacts

### 7.4.1 Contacts au Niveau Client

Chaque client peut avoir plusieurs contacts. Ces contacts sont les personnes avec qui AEMI communique pour ce client.

**Informations d'un contact :**

| Champ | Description | Exemple |
|-------|-------------|---------|
| Nom | Nom complet | Jean-Marie Lumumba |
| Fonction | Role dans l'entreprise | Directeur Technique |
| Telephone | Numero de telephone | +243 81 234 5678 |
| Email | Adresse email | jm.lumumba@bracongo.cd |

### 7.4.2 Contacts au Niveau Site

Chaque site peut aussi avoir ses propres contacts (distincts des contacts du client). Ce sont les personnes presentes sur le terrain que le technicien contactera en arrivant.

**Exemple pour la Brasserie de Kinshasa :**

*Contacts client :*
- Jean-Marie Lumumba (Directeur Technique) - pour les decisions
- Marie Kabila (Responsable Maintenance) - pour les aspects techniques

*Contact du site "Usine Principale Gombe" :*
- Joseph Mukendi - +243 81 111 0001 (la personne sur place qui accueille le technicien)

*Contact du site "Entrepot Limete" :*
- Pierre Kalala - +243 81 111 0002

Cette distinction est utile car le technicien a besoin du contact sur site (la personne qui ouvre le portail, qui montre le chemin), tandis que l'administrateur communique avec les contacts du client (pour les devis, factures, planification).

---

## 7.5 Gestion des Sites

### 7.5.1 Informations d'un Site

Chaque site a les informations suivantes :

| Champ | Description | Exemple |
|-------|-------------|---------|
| Nom | Nom du site | Mine Site Alpha |
| Adresse | Adresse physique | Zone Industrielle Nord |
| Localite | Ville ou zone | Lubumbashi |
| Coordonnees GPS | Latitude et longitude | -11.6647, 27.4794 |
| Contraintes d'acces | Informations pour le technicien | Zone industrielle, EPI obligatoires, escorte requise |
| Contacts sur site | Personnes a contacter sur place | Robert Mulongo, Grace Ilunga |

### 7.5.2 Les Sites de Demonstration

Voici la liste complete des sites presents dans la version de demonstration :

| Client | Site | Localite | Coordonnees | Contraintes |
|--------|------|----------|-------------|-------------|
| Brasserie de Kinshasa | Usine Principale Gombe | Gombe | -4.3217, 15.3125 | Acces par le portail principal, badge obligatoire |
| Brasserie de Kinshasa | Entrepot Limete | Limete | -4.3350, 15.3400 | - |
| Ambassade de France | Ambassade - Batiment Principal | Gombe | -4.3089, 15.2921 | Controle securite, piece d'identite obligatoire |
| Hotel du Fleuve | Hotel du Fleuve | Ngaliema | -4.3156, 15.2678 | - |
| Mining Corp International | Mine Site Alpha | Lubumbashi | -11.6647, 27.4794 | Zone industrielle, EPI obligatoires, escorte requise |
| Mining Corp International | Mine Site Beta | Lubumbashi | -11.6800, 27.4900 | - |
| Cimenterie Nationale | Cimenterie - Site Principal | Bas-Congo | -5.8544, 13.0458 | - |
| Raffinerie Petroliere | Raffinerie Port | Muanda | -5.9311, 12.3497 | Zone SEVESO, formation securite requise |

### 7.5.3 Les Contraintes d'Acces

Les contraintes d'acces sont des informations essentielles pour les techniciens. Elles decrivent ce qu'il faut savoir ou preparer avant d'arriver sur un site :

| Site | Contraintes | Ce que le technicien doit faire |
|------|------------|--------------------------------|
| Usine Principale Gombe | Badge obligatoire | Demander un badge visiteur a l'accueil |
| Ambassade de France | Controle securite, piece d'identite obligatoire | Apporter une piece d'identite valide, prevoir du temps |
| Mine Site Alpha | Zone industrielle, EPI obligatoires, escorte requise | Apporter casque, chaussures de securite, gilet. Attendre l'escorte a l'entree |
| Raffinerie Port | Zone SEVESO, formation securite requise | Avoir suivi la formation securite SEVESO avant la premiere visite |

Ces informations sont affichees dans l'application mobile du technicien quand il consulte les details de l'intervention.

---

## 7.6 Supprimer un Client

Pour supprimer un client :

1. Dans la liste des clients, cliquez sur l'icone **poubelle** sur la carte du client
2. Une fenetre de confirmation apparait : "Supprimer ce client - Cette action est irreversible. Toutes les donnees associees seront perdues."
3. Cliquez sur "Supprimer" pour confirmer

Attention : la suppression d'un client entrainera la perte de toutes les donnees associees (contacts, sites, equipements, interventions).

---

# 8. Module Equipements

Le module Equipements est le registre de tout le parc de groupes electrogenes geres par AEMI. Chaque equipement a une fiche technique complete avec son historique de maintenance.

---

## 8.1 Liste des Equipements

En cliquant sur "Equipements" dans le menu, vous arrivez sur la page principale.

### 8.1.1 Les Cartes KPI

Quatre cartes de statistiques en haut :

| Carte | Couleur | Valeur de demo | Description |
|-------|---------|----------------|-------------|
| Total equipements | Bleu | 11 | Nombre total de groupes electrogenes |
| Operationnels | Vert | 6 | Groupes en bon etat de fonctionnement |
| En panne | Rouge | 1 | Groupes en panne |
| Entretien requis | Orange | 2 | Groupes necessitant un entretien |

### 8.1.2 La Barre de Recherche et les Filtres

La barre de recherche permet de chercher par :
- Nom de l'equipement (ex : "Groupe Principal")
- Marque (ex : "Caterpillar")
- Modele (ex : "C15")
- Reference client (ex : "BK-GE-001")
- Nom du client (ex : "Brasserie")

Les boutons de filtre par statut :
- **Tous** : tous les equipements
- **Operationnel** : uniquement les groupes en fonctionnement
- **En panne** : uniquement les groupes en panne
- **Entretien requis** : groupes necessitant une maintenance
- **En intervention** : groupes actuellement en cours d'intervention
- **Hors service** : groupes mis hors service

### 8.1.3 Modes d'Affichage

Deux modes d'affichage sont disponibles, selectionnables avec les boutons en haut a droite :

**Mode Liste (par defaut) :**

Un tableau avec les colonnes suivantes :

| Colonne | Description | Exemple |
|---------|-------------|---------|
| Ref. Client | Reference donnee par le client | BK-GE-001 |
| Equipement | Nom + modele | Groupe Electrogene Principal / C15 |
| Marque | Fabricant | Caterpillar |
| Client | Nom du client proprietaire | Brasserie de Kinshasa |
| Heures | Compteur horaire avec barre de progression | 4750h (barre orange a 95%) |
| Statut | Badge colore | Operationnel (vert), En panne (rouge)... |
| Derniere intervention | Date de la derniere intervention | 15/01/2025 |
| Actions | Boutons "Fiche technique" et poubelle | - |

La barre de progression des heures change de couleur :
- **Vert** : le compteur est en dessous de 80% du seuil de maintenance
- **Orange** : le compteur est entre 80% et 100% du seuil
- **Rouge** : le seuil est depasse, l'entretien est en retard

**Mode Grille :**

Les equipements sont affiches sous forme de cartes avec :
- Nom et marque/modele
- Badge de statut
- Puissance (ex : 500 kVA)
- Compteur horaire avec barre de progression
- Reference client
- Nom du client et du site

Les colonnes triables sont :
- **Nom** : ordre alphabetique
- **Marque** : ordre alphabetique
- **Statut** : par type de statut
- **Heures** : par compteur horaire

### 8.1.4 Les Equipements de Demonstration

Voici la liste complete des equipements presents dans la version de demonstration :

| Ref. | Nom | Marque | Modele | Puissance | Client | Site | Statut | Heures |
|------|-----|--------|--------|-----------|--------|------|--------|--------|
| BK-GE-001 | Groupe Electrogene Principal | Caterpillar | C15 | 500 kVA | Brasserie de Kinshasa | Usine Principale Gombe | Entretien requis | 4750h |
| AMB-GE-01 | Generateur Secours | Perkins | 2000 Series | 350 kVA | Ambassade de France | Ambassade - Batiment Principal | Operationnel | 2340h |
| HDF-001 | Groupe Principal | Volvo Penta | TAD1345GE | 400 kVA | Hotel du Fleuve | Hotel du Fleuve | Operationnel | 3120h |
| MCI-ALPHA-001 | Groupe Industriel | Caterpillar | C18 | 750 kVA | Mining Corp International | Mine Site Alpha | En panne | 5680h |
| BK-GE-002 | Generateur Backup | Perkins | 4000 Series | 600 kVA | Brasserie de Kinshasa | Usine Principale Gombe | Operationnel | 1890h |
| CIMNAT-001 | Groupe de Secours | Cummins | QSX15 | 550 kVA | Cimenterie Nationale | Cimenterie - Site Principal | Hors service | 4200h |
| RAFPET-001 | Groupe Principal Raffinerie | MTU | 16V4000 DS | 2000 kVA | Raffinerie Petroliere | Raffinerie Port | Operationnel | 3500h |
| MCI-ALPHA-002 | Groupe Secours Alpha | Cummins | KTA50 | 1500 kVA | Mining Corp International | Mine Site Alpha | Operationnel | 2800h |
| MCI-BETA-001 | Groupe Principal Beta | Caterpillar | C32 | 1100 kVA | Mining Corp International | Mine Site Beta | Entretien requis | 4100h |
| MCI-BETA-002 | Groupe Secours Beta | Perkins | 4000 Series | 800 kVA | Mining Corp International | Mine Site Beta | Operationnel | 2100h |
| MCI-ALPHA-003 | Groupe Mobile | Caterpillar | C9 | 300 kVA | Mining Corp International | Mine Site Alpha | En intervention | 980h |

---

## 8.2 Fiche Equipement Detaillee

En cliquant sur un equipement dans la liste, vous ouvrez une fenetre modale avec un apercu. Pour acceder a la fiche complete, cliquez sur **"Voir fiche complete"** dans la modale, ou naviguez directement vers la page de detail.

### 8.2.1 L'En-tete de la Fiche

L'en-tete affiche :
- Le nom de l'equipement (ex : "Groupe Electrogene Principal")
- Le badge de statut (ex : "Entretien requis" en orange)
- La marque, le modele, la puissance (ex : "Caterpillar C15 - 500 kVA")
- La reference client (ex : "Ref: BK-GE-001")
- Deux boutons : "Creer Intervention" et "Exporter PDF"

### 8.2.2 Les Cartes KPI de l'Equipement

Quatre cartes en haut :

| Carte | Description | Exemple (BK-GE-001) |
|-------|-------------|---------------------|
| Compteur Horaire | Heures totales de fonctionnement | 4750h |
| Prochain Entretien | Heures restantes avant le prochain entretien | 250h restantes |
| Interventions | Nombre total d'interventions | 3 |
| Derniere Intervention | Date de la derniere intervention | 15/01/2025 |

La carte "Prochain Entretien" change de couleur selon l'urgence :
- Vert : plus de 25% du seuil restant
- Orange : entre 10% et 25% restant
- Rouge : moins de 10% restant ou seuil depasse

### 8.2.3 Les Onglets de la Fiche Technique

La fiche technique comporte **4 onglets** :

---

**Onglet "Fiche Technique" :**

Deux cartes cote a cote :

*Carte "Informations Generales" :*

| Champ | Valeur (BK-GE-001) |
|-------|---------------------|
| Marque | Caterpillar |
| Modele | C15 |
| N. Serie | CAT-2021-C15-001234 |
| Ref. Client | BK-GE-001 |
| Date Fabrication | 15/03/2021 |
| Mise en Service | 01/06/2021 |

*Carte "Specifications Techniques" :*

| Champ | Valeur (BK-GE-001) |
|-------|---------------------|
| Puissance | 500 kVA |
| Carburant | Diesel |
| Volume Reservoir | 1000L |
| Seuil Entretien | 250h |
| Compteur Actuel | 4750h |
| Prochain Entretien a | 5000h |

*Carte "Client & Localisation" :*

| Champ | Valeur |
|-------|--------|
| Client | Brasserie de Kinshasa |
| Site | Usine Principale Gombe |
| Adresse | 123 Boulevard du 30 Juin |
| Lien GPS | Voir sur la carte (Google Maps) |

*Carte "Documents" :*

Liste des documents attaches a l'equipement (fiches techniques, manuels, certificats). Si aucun document n'est enregistre, le message "Aucun document" est affiche.

---

**Onglet "Composants" :**

La liste de tous les composants et consommables du groupe electrogene. Chaque composant est affiche dans une carte avec :
- Une icone representative (moteur, filtre, courroie...)
- Le type de composant (en majuscules)
- La reference
- La marque (si renseignee)
- La quantite (si applicable)

**Composants du Caterpillar C15 (BK-GE-001) :**

| Type | Reference | Marque | Quantite |
|------|-----------|--------|----------|
| Moteur | C15-ATAAC | Caterpillar | - |
| Alternateur | LSA-50.2-L9 | Leroy Somer | - |
| Filtre a Air | CAT-1R-0750 | - | 2 |
| Filtre a Huile | CAT-1R-0739 | - | 1 |
| Filtre a Gasoil | CAT-1R-0753 | - | 2 |
| Courroie | K080830 | Gates | - |
| Huile Moteur | CAT DEO 15W-40 | - | 45L |
| Liquide Refroidissement | CAT ELC | - | 80L |

Ces references sont essentielles pour la preparation logistique des interventions. Quand un technicien prepare un entretien, il consulte cette liste pour savoir quels filtres et quelle quantite d'huile il faut.

---

**Onglet "Historique" :**

Liste de toutes les interventions passees et en cours pour cet equipement, triees par date (les plus recentes en premier).

Chaque intervention est affichee dans une ligne cliquable avec :
- Le type d'intervention (avec une icone coloree)
- Le type de maintenance si applicable (250h, 500h, 1000h)
- La description
- Le statut (badge colore)
- La date

En cliquant sur une intervention, vous etes redirige vers sa page de detail.

---

**Onglet "Maintenance" :**

Cet onglet est dedie au suivi de la maintenance preventive. Il est divise en deux parties :

*Partie gauche - Programme de Maintenance Preventive :*

Trois blocs pour les trois niveaux de maintenance :

| Seuil | Prochain a | Dans | Operations |
|-------|-----------|------|------------|
| **Entretien 250h** | 5000h | 250h | Vidange huile moteur, Remplacement filtre a huile, Verification courroies |
| **Entretien 500h** | 5000h | 250h | Tout entretien 250h + Remplacement filtre a air, Remplacement filtre gasoil, Verification alternateur |
| **Entretien 1000h** | 5000h | 250h | Tout entretien 500h + Remplacement liquide refroidissement, Inspection complete moteur, Calibration regulateur |

Si un entretien est proche (moins de 50h restantes), le bloc est mis en evidence avec un fond orange et un badge "Dans Xh" en orange.

*Partie droite - Suivi du Compteur :*

- Un grand affichage du compteur actuel (ex : 4750h)
- Une barre de progression visuelle (0h -> seuil)
- Un message d'etat : "OK", "Entretien bientot", ou "Entretien requis !"
- La liste des derniers entretiens effectues

---

## 8.3 Maintenance Preventive - Comment ca fonctionne

Le systeme de maintenance preventive est un des aspects les plus utiles de l'application. Voici comment il fonctionne en detail.

### 8.3.1 Le Compteur Horaire

Chaque groupe electrogene a un compteur d'heures de fonctionnement (horametre). Ce compteur est mis a jour :
- Manuellement par le technicien pendant une intervention (champs "Heures Debut" et "Heures Fin")
- Via les donnees enregistrees dans le systeme

### 8.3.2 Les Seuils de Maintenance

Chaque equipement a un seuil de maintenance configurable (par defaut 250h). Quand le compteur approche d'un multiple du seuil, le systeme genere une alerte.

**Exemple avec le Caterpillar C15 (BK-GE-001, seuil 250h) :**

| Compteur actuel | Prochain seuil | Heures restantes | Statut |
|----------------|---------------|-------------------|--------|
| 4750h | 5000h (250h x 20) | 250h | Entretien requis (orange) |

**Exemple avec le Perkins 2000 Series (AMB-GE-01, seuil 250h) :**

| Compteur actuel | Prochain seuil | Heures restantes | Statut |
|----------------|---------------|-------------------|--------|
| 2340h | 2500h (250h x 10) | 160h | OK (vert) |

### 8.3.3 Les Alertes

Quand le compteur depasse le seuil :
- Le statut de l'equipement passe a "Entretien requis"
- Le badge de l'equipement devient orange dans la liste
- La carte KPI "Entretien requis" se met a jour
- Sur le Dashboard (couvert dans la Partie 1), l'alerte est visible

### 8.3.4 Scenario Complet : Maintenance Preventive du MTU 16V4000

Le groupe MTU de la Raffinerie Petroliere a un compteur a 3500h et un seuil de 500h. Le prochain entretien est a 4000h, soit dans 500h.

1. **Le compteur atteint 3750h** (75% du seuil) : la barre de progression passe a l'orange dans la fiche technique. Le systeme n'alerte pas encore mais l'information est visible.

2. **Le compteur atteint 3950h** (50h restantes) : le bloc "Entretien 500h" dans l'onglet Maintenance passe en orange avec le badge "Dans 50h". C'est le moment de planifier.

3. **Clement voit l'alerte** et cree une intervention de type "Entretien" pour ce groupe, avec le sous-type "500h". Il assigne Francois Lukusa (competences : GE MTU, Installation).

4. **Le technicien effectue l'entretien** et met a jour le compteur : heures debut 3980h, heures fin 4000h.

5. **Le compteur est remis a zero** pour le cycle suivant : prochain entretien a 4500h.

---

## 8.4 Creer un Equipement

### 8.4.1 Ouvrir le Formulaire

Cliquez sur le bouton **"Ajouter un equipement"** en haut a droite de la page Equipements.

### 8.4.2 Remplir le Formulaire

Le formulaire contient les champs suivants :

| Champ | Type | Description | Obligatoire |
|-------|------|-------------|-------------|
| **Nom de l'equipement** | Texte | Nom descriptif | Oui |
| **Marque** | Texte | Fabricant (Caterpillar, Perkins, Cummins...) | Non |
| **Modele** | Texte | Reference du modele | Non |
| **Numero de serie** | Texte | Numero de serie unique | Non |
| **Puissance** | Texte | Puissance en kVA (ex : "500 kVA") | Non |
| **Carburant** | Menu deroulant | Diesel, Essence, ou Gaz | Oui |
| **Client** | Menu deroulant | Selectionnez le client proprietaire | Oui |
| **Site** | Menu deroulant | Selectionnez le site (filtre par client) | Oui |
| **Compteur horaire (h)** | Nombre | Heures actuelles au compteur | Non (0 par defaut) |
| **Seuil entretien (h)** | Nombre | Intervalle entre deux entretiens | Non (250 par defaut) |

Le menu "Site" se met a jour automatiquement quand vous selectionnez un client. Si le client n'a pas encore de site, le menu affiche "Aucun site pour ce client".

### 8.4.3 Exemple de Creation

Vous installez un nouveau generateur chez la Brasserie de Kinshasa :

1. Cliquez sur "Ajouter un equipement"
2. Remplissez :
   - Nom : Generateur Atelier
   - Marque : SDMO
   - Modele : J200K
   - Numero de serie : SDMO-2026-J200-001234
   - Puissance : 200 kVA
   - Carburant : Diesel
   - Client : Brasserie de Kinshasa
   - Site : Entrepot Limete
   - Compteur horaire : 0
   - Seuil entretien : 250
3. Cliquez sur "Creer l'equipement"

L'equipement apparait dans la liste avec le statut "Operationnel" et un compteur a 0h.

### 8.4.4 Modifier un Equipement

Pour modifier un equipement :

1. Dans la liste, cliquez sur un equipement pour ouvrir la modale
2. Dans la modale, cliquez sur le bouton **"Modifier"**
3. Le formulaire de modification s'ouvre avec les valeurs actuelles pre-remplies
4. Modifiez les champs souhaites
5. Cliquez sur **"Enregistrer les modifications"**

### 8.4.5 Supprimer un Equipement

Pour supprimer un equipement :
1. Cliquez sur l'icone poubelle (dans la liste en mode tableau, ou dans la carte en mode grille)
2. Confirmez la suppression dans la fenetre de dialogue

---

## 8.5 Lien entre Equipements et Interventions

Depuis la fiche d'un equipement, vous pouvez directement creer une intervention. Le bouton **"Creer Intervention"** vous redirige vers la page de creation d'intervention avec le client, le site et l'equipement pre-remplis.

Depuis la modale de detail, le bouton **"Creer une intervention"** fait la meme chose.

Cela accelere beaucoup le processus : quand vous voyez qu'un equipement a besoin d'entretien, vous pouvez creer l'intervention en un seul clic.

---

# 9. Module Planning

Le module Planning est votre outil de planification quotidien. Il vous offre deux vues complementaires : une vue Kanban et une vue calendrier hebdomadaire.

---

## 9.1 Presentation Generale

En cliquant sur "Planning" dans le menu, vous arrivez sur la page de planification. En haut, vous voyez :

- Le titre "Planning" avec le sous-titre "Planification et suivi des interventions"
- Deux boutons pour choisir le mode d'affichage :
  - **Kanban** (icone graphique a barres)
  - **Semaine** (icone calendrier)

### 9.1.1 Les Statistiques en Barre

Juste en dessous de l'en-tete, une barre horizontale de statistiques affiche :

| Carte | Couleur | Contenu | Exemple |
|-------|---------|---------|---------|
| A Planifier | Orange | Nombre d'interventions au statut "Creee" | 2 (15%) |
| Planifie | Bleu | Nombre d'interventions "Planifiee" ou "Affectee" | 3 (23%) |
| En Cours | Bleu | Nombre d'interventions "En route", "Sur site", "En cours", "En attente" | 4 (31%) |
| Termine | Vert | Nombre d'interventions "Terminee", "Validee", "A facturer", "Facturee" | 4 (31%) |
| Urgentes | Rouge (si > 0) | Nombre d'interventions avec priorite "Urgente" | 1 - Attention |

Chaque carte montre aussi le pourcentage par rapport au total.

---

## 9.2 Vue Kanban

La vue Kanban est un tableau a colonnes ou vous pouvez visualiser et deplacer les interventions d'un statut a l'autre par glisser-deposer (drag and drop).

### 9.2.1 Les Colonnes

Le tableau Kanban a **4 colonnes** :

| Colonne | Couleur | Statuts regroupes | Description |
|---------|---------|-------------------|-------------|
| **A Planifier** | Orange | Creee | Interventions recemment creees, pas encore planifiees |
| **Planifie** | Bleu | Planifiee, Affectee | Interventions planifiees et/ou assignees a un technicien |
| **En Cours** | Bleu | En route, Sur site, En cours, En attente | Interventions actuellement en traitement |
| **Termine** | Vert | Terminee, Validee, A facturer, Facturee | Interventions terminees |

Chaque colonne affiche un compteur (le nombre de cartes dans la colonne).

### 9.2.2 Les Cartes d'Intervention

Chaque intervention est representee par une carte dans la colonne correspondante. La carte affiche :

- Une **poignee de glissement** (6 points) a gauche pour attraper la carte
- Un **badge de type** (Reparation en rouge, Entretien en bleu, etc.)
- Un **icone d'alerte** si la priorite est "Urgente"
- La **description** (2 lignes maximum)
- La **date prevue** et l'heure si renseignee
- Un **badge de priorite** (Urgente, Haute, Normale, Basse)
- Un **badge de statut** detaille
- Le **nombre de techniciens** assignes, ou "Non assigne"
- Un **bouton oeil** pour voir le detail de l'intervention

### 9.2.3 Le Glisser-Deposer (Drag and Drop)

C'est la fonctionnalite principale de la vue Kanban. Voici comment l'utiliser :

**Pour deplacer une intervention d'une colonne a une autre :**

1. Survolez la poignee de glissement (les 6 points a gauche de la carte)
2. Cliquez et maintenez le bouton de la souris
3. Glissez la carte vers la colonne souhaitee
4. La colonne cible se met en evidence (bordure bleue, fond clair, texte "Deposer ici")
5. Relacher la carte dans la colonne cible

La carte de l'intervention suit votre curseur pendant le glissement, avec un leger angle (rotation de 2 degres) et une ombre pour montrer qu'elle est en mouvement.

**Quand vous deposez la carte :**
- Le statut de l'intervention est automatiquement mis a jour
- La carte se deplace dans la nouvelle colonne

**Correspondance des colonnes et des statuts :**

| Colonne de destination | Statut applique |
|------------------------|----------------|
| A Planifier | Creee |
| Planifie | Planifiee |
| En Cours | En cours |
| Termine | Terminee |

### 9.2.4 Exemple Pratique : Planifier la Semaine avec le Kanban

Clement, voici comment vous pourriez utiliser le Kanban un lundi matin :

**1. Etat initial :**
Vous ouvrez le Planning en vue Kanban et vous voyez :
- Colonne "A Planifier" : 2 cartes
  - Reparation urgente chez Brasserie de Kinshasa (panne totale)
  - Diagnostic chez Hotel du Fleuve (bruit anormal)
- Colonne "Planifie" : 2 cartes
  - Maintenance 250h a l'Ambassade de France (demain 08h, Patrick Ilunga assigne)
  - Maintenance 250h a Hotel du Fleuve (demain 14h, Jean-Pierre Tshombe assigne)
- Colonne "En Cours" : 3 cartes
  - Maintenance 500h chez Mining Corp (sur site Alpha, equipe en cours)
  - Reparation chez Brasserie de Kinshasa (fuite d'huile, Patrick en cours)
  - Installation chez Mining Corp (site Alpha, equipe de 3 en cours)
- Colonne "Termine" : 6 cartes
  - Diverses interventions terminees, validees, ou facturees

**2. Vous traitez les urgences :**
Vous glissez la carte "Reparation urgente chez Brasserie de Kinshasa" de la colonne "A Planifier" vers la colonne "Planifie". Le statut passe a "Planifiee". Vous allez ensuite dans le detail pour assigner un technicien.

**3. Vous organisez le diagnostic :**
La carte "Diagnostic Hotel du Fleuve" reste dans "A Planifier" car vous attendez de confirmer avec le client.

**4. Vous suivez les travaux en cours :**
Les 3 cartes dans "En Cours" sont gerees par les techniciens sur le terrain. Vous pouvez cliquer sur l'icone oeil pour voir le detail et verifier l'avancement.

---

## 9.3 Vue Calendrier (Semaine)

La vue calendrier affiche les interventions sur une grille hebdomadaire avec des creneaux horaires.

### 9.3.1 La Navigation

En haut de la vue calendrier, vous avez :
- Un bouton **"Sem. prec."** pour aller a la semaine precedente
- L'affichage de la semaine actuelle (ex : "10 fev. - 16 fev. 2026")
- Un bouton **"Sem. suiv."** pour aller a la semaine suivante

### 9.3.2 La Grille

La grille est organisee en :
- **Colonnes** : les 7 jours de la semaine (Lun, Mar, Mer, Jeu, Ven, Sam, Dim)
- **Lignes** : les creneaux horaires de 8h a 18h

Chaque colonne de jour affiche :
- L'abreviation du jour (Lun, Mar...)
- Le numero du jour (10, 11, 12...)
- Le nombre d'interventions du jour (badge, ex : "3 interv.")

Le jour actuel est mis en evidence avec un fond bleu clair.
Les weekends (samedi et dimanche) ont un fond gris leger.

### 9.3.3 Les Interventions dans la Grille

Les interventions sont placees dans la cellule correspondant a leur jour et heure prevus. Chaque intervention est un petit bloc colore selon sa priorite :

| Priorite | Style du bloc |
|----------|---------------|
| Urgente | Fond rouge clair, bordure rouge, texte rouge |
| Haute | Fond orange clair, bordure orange, texte orange |
| Normale | Fond bleu clair, bordure bleue, texte bleu |
| Basse | Fond gris, bordure grise, texte gris |

Chaque bloc affiche :
- Un point de couleur (correspondant a la priorite)
- Le type d'intervention (ex : "Entretien")
- La description (tronquee)
- L'heure prevue (ex : "08:00")
- La duree estimee (ex : "~3h")

En cliquant sur un bloc, vous etes redirige vers la page de detail de l'intervention.

### 9.3.4 La Legende

En bas de la grille, une legende rappelle le code couleur des priorites :
- Point rouge = Urgente
- Point orange = Haute
- Point bleu = Normale
- Point gris = Basse

### 9.3.5 Exemple Pratique : Visualiser la Semaine

Clement, voici a quoi ressemblerait votre semaine sur le calendrier :

**Lundi 10 fevrier 2026 :**

| Heure | Intervention |
|-------|-------------|
| 06:00 | Installation nouveau groupe mobile - Mining Corp - Site Alpha (bloc bleu) |
| 07:00 | Maintenance 500h - Mining Corp - Site Alpha (bloc bleu) |
| - | Reparation fuite d'huile - Brasserie de Kinshasa (bloc orange) |

**Mardi 11 fevrier 2026 :**

| Heure | Intervention |
|-------|-------------|
| 08:00 | Maintenance 250h - Ambassade de France (bloc orange, priorite haute) |
| 14:00 | Maintenance 250h - Hotel du Fleuve (bloc bleu, priorite normale) |

**Semaine suivante :**

| Heure | Intervention |
|-------|-------------|
| - | Diagnostic - Hotel du Fleuve (bloc bleu, pas d'heure fixee) |

Les jours sans intervention sont vides. Les creneaux horaires vides sont aussi visibles, ce qui vous aide a identifier les disponibilites pour planifier de nouvelles missions.

---

## 9.4 Comment Utiliser le Planning au Quotidien

Voici une routine type pour la gestion du planning, Clement :

### Le Matin (08h00 - 08h30) : Revue du Jour

1. **Ouvrez le Planning en vue Kanban**
2. **Verifiez la colonne "A Planifier"** : y a-t-il de nouvelles demandes ?
3. **Verifiez la colonne "En Cours"** : les techniciens sur le terrain ont-ils mis a jour les statuts ?
4. **Passez en vue Semaine** pour voir les interventions du jour
5. **Verifiez les alertes** : interventions en retard ? Urgences non traitees ?

### En Journee : Suivi des Operations

1. **Suivez les interventions en cours** en verifiant regulierement la colonne "En Cours" du Kanban
2. **Reagissez aux urgences** : si un client appelle pour une panne, creez l'intervention et glissez-la directement dans "Planifie" ou "En Cours"
3. **Validez les interventions terminees** : quand une carte arrive dans "Termine", ouvrez le detail et validez si tout est en ordre

### En Fin de Journee : Preparation du Lendemain

1. **Passez en vue Semaine** et naviguez au lendemain
2. **Verifiez** que les interventions du lendemain ont des techniciens assignes et que la logistique est prete
3. **Deplacez** les interventions non traitees du jour vers la bonne date

### En Fin de Semaine : Bilan et Planification

1. **Passez en vue Kanban** pour voir l'etat general
2. **Traitez les cartes restantes dans "A Planifier"**
3. **Naviguez a la semaine suivante en vue calendrier** pour preparer le planning
4. **Verifiez les seuils de maintenance** des equipements (module Equipements) et creez les interventions preventives necessaires

---

## 9.5 Differences entre Vue Kanban et Vue Calendrier

| Aspect | Vue Kanban | Vue Calendrier |
|--------|-----------|----------------|
| Organisation | Par statut (colonnes) | Par jour et heure (grille) |
| Utilite principale | Suivi du workflow, changement de statut | Planification temporelle, vision de la charge |
| Interaction | Glisser-deposer pour changer le statut | Clic pour voir le detail |
| Vision | Etat global de toutes les interventions | Charge de travail sur une semaine |
| Quand l'utiliser | Pour gerer les flux, traiter les urgences | Pour planifier, verifier les disponibilites |

Les deux vues sont complementaires. Utilisez le Kanban pour gerer le flux quotidien et le calendrier pour planifier la charge de la semaine.

---

# Resume de la Partie 2

Clement, voici un resume de tout ce qu'on a couvert dans cette partie :

| Module | Fonctionnalites principales | Nombre d'ecrans |
|--------|-----------------------------|-----------------|
| **Interventions** | Creation, detail (5 onglets), workflow complet, checklists ISO, photos, signature client, export PDF | 2 ecrans + 5 onglets |
| **Clients** | Creation, detail (contacts, sites, equipements, historique), recherche, filtres | 2 ecrans + 4 onglets |
| **Equipements** | Creation, modification, fiche technique detaillee, composants, historique, maintenance preventive | 2 ecrans + 4 onglets |
| **Planning** | Vue Kanban (drag & drop), vue calendrier hebdomadaire, statistiques | 1 ecran + 2 vues |

Ces quatre modules constituent le coeur operationnel de l'application AEMI GMAO. Ils couvrent l'ensemble du cycle de vie d'une intervention, de la demande client a la facturation.

Dans la **Partie 3**, nous couvrirons les modules complementaires : Equipes & Personnel, Logistique, Charroi (vehicules), Facturation, Reporting, Parametres, et l'application mobile technicien.

---

*Document prepare par ExplorIA - Fevrier 2026*
*Application AEMI GMAO : https://aemi-gmao.vercel.app*
# AEMI GMAO - Document de Presentation - PARTIE 3

**Application :** AEMI GMAO - Gestion de Maintenance Assistee par Ordinateur
**URL :** [https://aemi-gmao.vercel.app](https://aemi-gmao.vercel.app)
**Client :** Clement
**Agence :** ExplorIA
**Date :** Fevrier 2026

---

> Clement, cette troisieme partie couvre les modules complementaires de l'application : la facturation, l'atelier, la logistique, le charroi (flotte de vehicules), le reporting, les parametres, la carte interactive et l'inventaire. Chaque module est explique en detail avec des exemples tires des donnees de demonstration presentes dans l'application.

---

# 10. Module Facturation

Le module Facturation se trouve dans le menu lateral sous l'icone **DollarSign** avec le libelle "Facturation". C'est ici que vous gerez tout le cycle financier de vos interventions : de l'etablissement d'un devis jusqu'au suivi du paiement de la facture.

L'application utilise le Franc Congolais (CDF) comme monnaie, et applique un taux de TVA de **16%** pour calculer les montants TTC a partir des montants HT.

---

## 10.1. Les Devis (Offres)

### A quoi sert un devis ?

Avant de realiser une intervention, il est souvent necessaire d'envoyer un devis au client pour qu'il accepte le travail et le montant propose. Dans AEMI GMAO, un devis s'appelle une **Offre**. Chaque offre est liee a un client, un site, un equipement, et eventuellement a une intervention.

### La liste des devis

Quand vous ouvrez l'onglet **Devis** dans le module Facturation, vous voyez un tableau qui presente tous les devis enregistres dans le systeme. Voici les colonnes affichees :

| Colonne | Description |
|---------|-------------|
| **Objet** | Description courte du devis (ex: "Reparation urgente - Remplacement batterie et demarreur") |
| **Client** | Le nom du client concerne |
| **Montant HT** | Le montant hors taxes, en CDF |
| **Montant TTC** | Le montant toutes taxes comprises (HT + 16% TVA), en CDF |
| **Date de transmission** | La date a laquelle le devis a ete envoye au client |
| **Statut** | L'etat actuel du devis |

### Les statuts d'un devis

Un devis peut avoir trois statuts differents :

| Statut | Couleur du badge | Signification |
|--------|-----------------|---------------|
| **En attente** | Jaune/ambre | Le devis a ete envoye au client mais il n'a pas encore donne de reponse. On attend sa decision. |
| **Accepte** | Vert | Le client a approuve le devis. On peut planifier l'intervention et eventuellement generer une facture. |
| **Rejete** | Rouge | Le client a refuse le devis. Peut-etre que le montant etait trop eleve, ou que le client a choisi un autre prestataire. |

### Donnees de demonstration : les 4 devis

L'application contient 4 devis de demonstration pour vous montrer les differents cas de figure. Voici le detail :

**Devis 1 - En attente**

| Champ | Valeur |
|-------|--------|
| Objet | Reparation urgente - Remplacement batterie et demarreur |
| Client | Brasserie de Kinshasa |
| Site | Usine Principale Gombe |
| Equipement | Groupe Electrogene Principal (Caterpillar C15, 500 kVA) |
| Montant HT | 2 500 000 CDF |
| Montant TTC | 2 950 000 CDF |
| Statut | En attente |

Ce devis correspond a une situation urgente : le groupe electrogene principal de la Brasserie de Kinshasa ne demarre plus, la production est a l'arret. Le devis a ete transmis il y a quelques jours et on attend la reponse du client.

**Devis 2 - Accepte**

| Champ | Valeur |
|-------|--------|
| Objet | Maintenance preventive 250h |
| Client | Mining Corp International |
| Site | Mine Site Alpha, Lubumbashi |
| Equipement | Groupe Secours Alpha (Cummins KTA50, 1500 kVA) |
| Montant HT | 1 500 000 CDF |
| Montant TTC | 1 770 000 CDF |
| N Bon de commande | BC-MCI-2025-0045 |
| Statut | Accepte |
| Intervention liee | INT-7 (Maintenance preventive 250h terminee) |

Ce devis a ete accepte par Mining Corp International. Le client a meme fourni un numero de bon de commande (BC-MCI-2025-0045), ce qui est courant avec les grandes entreprises minieres. L'intervention associee est terminee et validee.

**Devis 3 - Accepte**

| Champ | Valeur |
|-------|--------|
| Objet | Reparation alternateur + pieces |
| Client | Cimenterie Nationale |
| Site | Cimenterie - Site Principal, Bas-Congo |
| Equipement | Groupe de Secours (Cummins QSX15, 550 kVA) |
| Montant HT | 4 500 000 CDF |
| Montant TTC | 5 310 000 CDF |
| N Bon de commande | BC-CIMNAT-2025-0012 |
| Statut | Accepte |
| Intervention liee | INT-8 (Reparation alternateur) |

C'est le devis le plus important en montant. La reparation d'un alternateur sur un groupe Cummins de 550 kVA demande des pieces couteuses. Le devis a ete accepte et une facture a ete generee.

**Devis 4 - Rejete**

| Champ | Valeur |
|-------|--------|
| Objet | Maintenance majeure 1000h |
| Client | Hotel du Fleuve |
| Site | Hotel du Fleuve, Ngaliema |
| Equipement | Groupe Principal (Volvo Penta TAD1345GE, 400 kVA) |
| Montant HT | 3 500 000 CDF |
| Montant TTC | 4 130 000 CDF |
| Statut | Rejete |

L'Hotel du Fleuve a refuse ce devis. Peut-etre que le montant de 3 500 000 CDF HT etait au-dessus de leur budget, ou qu'ils ont decide de reporter la maintenance majeure. Dans tous les cas, le devis reste dans le systeme pour reference.

### Creer un nouveau devis - etape par etape

Voici comment creer un nouveau devis dans l'application :

**Etape 1 : Ouvrir le formulaire**
- Allez dans le module Facturation
- Restez sur l'onglet "Devis"
- Cliquez sur le bouton **"+ Nouveau devis"** en haut a droite
- Une fenetre de dialogue s'ouvre avec le formulaire

**Etape 2 : Selectionner le client**
- Dans le menu deroulant "Client", choisissez le client concerne
- La liste propose tous les clients enregistres : Brasserie de Kinshasa, Ambassade de France, Hotel du Fleuve, Mining Corp International, Cimenterie Nationale, Raffinerie Petroliere

**Etape 3 : Decrire l'objet du devis**
- Dans le champ "Objet", ecrivez une description claire et courte
- Exemples :
  - "Maintenance preventive 500h - GE Caterpillar C18"
  - "Reparation demarreur + remplacement batterie"
  - "Installation nouveau groupe electrogene 300 kVA"

**Etape 4 : Saisir le montant**
- Entrez le **montant HT** (hors taxes) en CDF
- Le **montant TTC** est calcule automatiquement : Montant HT x 1.16
- Par exemple, si vous saisissez 2 000 000 CDF HT, le TTC affichera 2 320 000 CDF

**Etape 5 : Definir la date de transmission**
- Selectionnez la date a laquelle le devis sera envoye au client
- Par defaut, la date du jour est pre-remplie

**Etape 6 : Enregistrer**
- Cliquez sur le bouton "Creer"
- Le devis apparait dans la liste avec le statut "En attente"
- Une notification de confirmation s'affiche en bas de l'ecran

### Lier un devis a une intervention

Quand un devis est accepte et que l'intervention correspondante est realisee, le systeme permet de faire le lien entre les deux. Ce lien est important pour la tracabilite : on sait quel devis correspond a quelle intervention, et plus tard a quelle facture.

Dans les donnees de demonstration :
- Le devis OFF-2 (Maintenance preventive 250h) est lie a l'intervention INT-7
- Le devis OFF-3 (Reparation alternateur) est lie a l'intervention INT-8

Ce lien permet de suivre le parcours complet : demande client -> devis -> acceptation -> intervention -> facture -> paiement.

### Recherche et filtrage

En haut de la liste des devis, vous disposez de :
- Un **champ de recherche** pour filtrer par objet, client ou montant
- Un **filtre par statut** pour n'afficher que les devis en attente, acceptes ou rejetes

---

## 10.2. Les Factures

### A quoi sert une facture dans AEMI GMAO ?

Une fois qu'une intervention est terminee, validee, et que le devis a ete accepte, il faut envoyer une facture au client pour obtenir le paiement. Le module Factures permet de creer, suivre et gerer toutes les factures.

### La liste des factures

L'onglet **Factures** affiche un tableau avec les colonnes suivantes :

| Colonne | Description |
|---------|-------------|
| **Numero** | L'identifiant unique de la facture (ex: INV-1, INV-2) |
| **Client** | Le nom du client a facturer |
| **Objet** | La description du travail facture |
| **Date intervention** | La date a laquelle l'intervention a eu lieu |
| **Montant HT** | Le montant hors taxes |
| **Montant TTC** | Le montant toutes taxes comprises |
| **Date de transmission** | Quand la facture a ete envoyee |
| **Statut** | L'etat du paiement |

### Les statuts d'une facture

| Statut | Couleur du badge | Signification |
|--------|-----------------|---------------|
| **En attente** | Jaune/ambre | La facture a ete envoyee mais le paiement n'a pas encore ete recu. C'est le statut initial. |
| **Contestee** | Rouge | Le client a conteste la facture. Il peut y avoir un desaccord sur le montant, sur le travail effectue, ou une erreur. Il faut resoudre le probleme avec le client. |
| **Payee** | Vert | Le client a paye. La facture est cloturee. |

### Donnees de demonstration : les factures

L'application contient des factures de demonstration :

**Facture INV-1 - En attente**

| Champ | Valeur |
|-------|--------|
| Objet | Reparation alternateur + pieces |
| Client | Cimenterie Nationale |
| Devis associe | OFF-3 |
| N Bon de commande | BC-CIMNAT-2025-0012 |
| Intervention | INT-8 (Reparation alternateur) |
| Date intervention | La semaine derniere |
| Montant HT | 4 500 000 CDF |
| Montant TTC | 5 310 000 CDF |
| Statut | En attente |

Cette facture est liee au devis OFF-3 qui avait ete accepte par la Cimenterie Nationale. L'intervention de reparation de l'alternateur a ete effectuee, et la facture a ete envoyee hier. On attend le paiement.

**Facture INV-2 - Payee**

| Champ | Valeur |
|-------|--------|
| Objet | Maintenance 500h complete |
| Client | Raffinerie Petroliere |
| Devis associe | OFF-2 |
| N Bon de commande | BC-MCI-2025-0045 |
| Intervention | INT-10 (Maintenance complete) |
| Date intervention | Il y a deux semaines |
| Montant HT | 2 000 000 CDF |
| Montant TTC | 2 360 000 CDF |
| Date de paiement | Il y a trois jours |
| Statut | Payee |

Cette facture est un exemple de cycle complet : le devis a ete accepte, l'intervention realisee, la facture envoyee, et le paiement recu. Le montant de 2 360 000 CDF TTC a ete verse il y a trois jours.

### Creer une facture a partir d'un devis

La creation d'une facture suit generalement ce parcours :

**Etape 1 : Verifier que l'intervention est terminee et validee**
- L'intervention doit etre au statut "Validee" ou "A facturer"
- Le superviseur doit avoir valide le travail effectue

**Etape 2 : Ouvrir le formulaire de creation de facture**
- Dans l'onglet "Factures", cliquez sur **"+ Nouvelle facture"**
- Le formulaire s'ouvre

**Etape 3 : Remplir les informations**
- **Client** : selectionnez le client dans le menu deroulant
- **Objet** : decrivez le travail facture
- **Montant HT** : saisissez le montant hors taxes
- Le montant TTC est calcule automatiquement (HT x 1.16)
- **Date de transmission** : la date du jour par defaut
- **Numero de bon de commande** (si disponible) : les grands clients fournissent souvent un numero de BC

**Etape 4 : Lier au devis (facultatif)**
- Si un devis existe pour cette intervention, vous pouvez le lier
- Cela permet de garder la tracabilite complete

**Etape 5 : Enregistrer**
- Cliquez sur "Creer"
- La facture apparait avec le statut "En attente"

### Details d'une facture

Quand vous cliquez sur une facture dans la liste, vous accedez a ses details complets :

- Informations du client (nom, adresse, contacts)
- Description du travail effectue
- Dates (intervention, transmission, paiement eventuel)
- Montants (HT, TVA, TTC)
- Numero de bon de commande
- Lien vers le devis et l'intervention associes
- Historique des changements de statut

---

## 10.3. Rapprochement : le cycle complet Intervention - Devis - Facture

Le rapprochement est le fil conducteur entre les trois elements : l'intervention, le devis et la facture. Voici comment cela fonctionne dans la pratique :

### Le cycle de facturation complet

```
1. Demande du client
       |
       v
2. Creation d'un devis (Offre)
   Statut : En attente
       |
       v
3. Le client accepte le devis
   Statut : Accepte
   (Le client peut aussi fournir un numero de bon de commande)
       |
       v
4. L'intervention est planifiee et realisee
   Statuts : Creee -> Planifiee -> En cours -> Terminee -> Validee
       |
       v
5. Creation de la facture
   La facture reprend les montants du devis
   Statut : En attente
       |
       v
6. Envoi de la facture au client
   La date de transmission est enregistree
       |
       v
7. Le client paie
   Statut : Payee
   La date de paiement est enregistree
```

### Exemple de rapprochement avec les donnees de demo

Prenons l'exemple de la Cimenterie Nationale :

| Etape | Element | Detail |
|-------|---------|--------|
| 1 | Intervention INT-8 | Reparation alternateur - Cimenterie Nationale |
| 2 | Devis OFF-3 | Montant HT : 4 500 000 CDF, Statut : Accepte |
| 3 | Bon de commande | BC-CIMNAT-2025-0012 |
| 4 | Facture INV-1 | Montant TTC : 5 310 000 CDF, Statut : En attente |

Et pour la Raffinerie Petroliere :

| Etape | Element | Detail |
|-------|---------|--------|
| 1 | Intervention INT-10 | Maintenance 500h complete |
| 2 | Devis OFF-2 | Montant HT : 2 000 000 CDF, Statut : Accepte |
| 3 | Bon de commande | BC-MCI-2025-0045 |
| 4 | Facture INV-2 | Montant TTC : 2 360 000 CDF, Statut : Payee |

### Suivi du statut de paiement

Le module Facturation affiche des indicateurs en haut de la page pour suivre la situation financiere :

- **Montant total en attente** : somme des factures non payees
- **Montant total paye** : somme des factures reglees
- **Nombre de devis en attente** : combien de devis n'ont pas encore recu de reponse
- **Taux d'acceptation des devis** : pourcentage de devis acceptes par rapport au total

Ces indicateurs permettent d'avoir une vue rapide de la sante financiere de l'activite.

### Barre de progression

Pour chaque facture, une barre de progression visuelle montre ou en est le processus :

```
Devis envoye  -->  Devis accepte  -->  Facture envoyee  -->  Facture payee
   [ Jaune ]        [ Bleu ]           [ Orange ]          [ Vert ]
```

---

## 10.4. Export PDF des devis et factures

### Generer un PDF

L'application permet de generer des documents PDF pour les devis et les factures. C'est utile pour :
- Envoyer un devis professionnel au client par email
- Imprimer une facture pour les archives
- Garder une trace papier des transactions

### Comment generer un PDF

**Etape 1 :** Ouvrez le detail d'un devis ou d'une facture

**Etape 2 :** Cliquez sur le bouton **"Telecharger PDF"** (icone de telechargement)

**Etape 3 :** Le PDF est genere et telecharge automatiquement sur votre ordinateur

### Contenu du PDF

Le document PDF genere contient toutes les informations necessaires :

**En-tete du document :**
- Logo et nom de l'entreprise AEMI
- Numero du document (devis ou facture)
- Date d'emission

**Informations client :**
- Nom du client
- Adresse
- Personne de contact
- Telephone et email

**Corps du document :**
- Objet du devis ou de la facture
- Description detaillee du travail
- Reference de l'equipement concerne

**Montants :**
- Montant HT
- TVA (16%)
- Montant TTC
- Numero de bon de commande (si applicable)

**Pied de page :**
- Conditions de paiement
- Coordonnees bancaires
- Date de validite (pour les devis)

### Exemple de contenu PDF pour le devis OFF-3

```
DEVIS N  OFF-3
Date : [date de creation]

CLIENT :
Cimenterie Nationale
Route de Matadi, Bas-Congo
Contact : Francois Ngoma - Directeur Usine
Tel : +243 82 333 4444

OBJET :
Reparation alternateur + pieces

EQUIPEMENT :
Groupe de Secours - Cummins QSX15 (550 kVA)
N serie : CUM-2018-QSX-002345
Site : Cimenterie - Site Principal

MONTANT :
Montant HT :    4 500 000 CDF
TVA (16%) :       720 000 CDF
Montant TTC :   5 310 000 CDF

N Bon de commande : BC-CIMNAT-2025-0012
```

---

# 11. Module Atelier / Workshop

Le module Atelier est dedie a la gestion des reparations qui se font dans les locaux d'AEMI, par opposition aux interventions sur site. Quand un equipement est trop endommage pour etre repare sur place, ou quand une reparation necessite un outillage specifique, l'equipement est ramene a l'atelier.

Vous accedez a ce module via le menu lateral, sous l'icone **Factory** avec le libelle "Atelier".

---

## 11.1. Les Ordres de Travail (Work Orders)

### Qu'est-ce qu'un ordre de travail ?

Un ordre de travail est un document qui decrit le travail a effectuer sur un equipement en atelier. Il contient toutes les informations necessaires : quel equipement, quel client, quel probleme, quel technicien s'en occupe, quelles pieces sont necessaires, etc.

### Le tableau des ordres de travail

La page Atelier affiche un tableau avec les colonnes suivantes :

| Colonne | Description |
|---------|-------------|
| **N Ordre** | Numero unique de l'ordre (ex: AT-2026-001) |
| **Client** | Le nom du client proprietaire de l'equipement |
| **Type Equipement** | Moteur, Transformateur, Alternateur ou Autre |
| **Marque** | La marque de l'equipement (ABB, Schneider, Leroy-Somer, etc.) |
| **Modele** | Le modele exact |
| **Statut** | L'etat d'avancement du travail |
| **Priorite** | Basse, Normale, Haute ou Urgente |
| **Date reception** | Quand l'equipement est arrive a l'atelier |

### Le flux de statuts des ordres de travail

Un ordre de travail suit un parcours precis en 7 etapes. Chaque etape correspond a une phase du travail en atelier :

```
Receptionne -> Diagnostique -> Attente pieces -> En reparation -> Controle qualite -> Pret -> Livre
```

Voici le detail de chaque statut :

**1. Receptionne (received)**
- Couleur : Bleu
- L'equipement vient d'arriver a l'atelier
- Il a ete decharge et enregistre dans le systeme
- Un numero d'ordre de travail lui a ete attribue
- A ce stade, aucun technicien n'est encore affecte
- On prend des photos de l'etat de l'equipement a l'arrivee

**2. Diagnostique (diagnosed)**
- Couleur : Violet
- Un technicien a examine l'equipement
- Les problemes ont ete identifies et documentes
- Les notes de diagnostic sont redigees
- On sait maintenant ce qu'il faut reparer et quelles pieces seront necessaires
- Un devis peut etre envoye au client a ce stade

**3. Attente pieces (waiting_parts)**
- Couleur : Ambre/jaune
- Le diagnostic est fait, mais on attend des pieces de rechange
- Les pieces ont ete commandees aupres du fournisseur
- Ce statut est important car il explique un eventuel retard dans la reparation
- Le client est informe du delai

**4. En reparation (in_repair)**
- Couleur : Cyan
- Le technicien travaille activement sur l'equipement
- Les pieces sont disponibles
- Le travail est en cours : demontage, remplacement, remontage
- Les heures de main-d'oeuvre sont comptabilisees

**5. Controle qualite (quality_check)**
- Couleur : Indigo
- La reparation est terminee
- On verifie que tout fonctionne correctement
- Tests electriques, tests de charge, mesures d'isolation
- Si le controle revele un probleme, l'ordre repasse en reparation

**6. Pret (ready)**
- Couleur : Vert
- L'equipement a passe le controle qualite avec succes
- Il est pret a etre recupere par le client
- Le client est notifie
- Le cout final est calcule

**7. Livre (delivered)**
- Couleur : Gris
- L'equipement a ete rendu au client
- La date de livraison effective est enregistree
- L'ordre de travail est cloture

### Avancement visuel du statut

Dans l'application, quand vous ouvrez le detail d'un ordre de travail, vous voyez un **stepper horizontal** (barre d'avancement) qui montre visuellement ou en est l'equipement dans le parcours. Les etapes deja passees sont colorees, l'etape actuelle est mise en avant, et les etapes futures sont grisees.

Un bouton **"Avancer vers : [prochain statut]"** permet de faire passer l'ordre de travail a l'etape suivante en un clic.

### Les 7 ordres de travail de demonstration

Voici les 7 ordres de travail presents dans les donnees de demonstration. Ils illustrent chacun un statut different :

---

**Ordre AT-2026-001 - En reparation**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-001 |
| Client | Brasserie du Congo |
| Type | Moteur |
| Marque / Modele | ABB M3BP 315 |
| N Serie | ABB-2019-7845 |
| Puissance | 250 kW |
| Description | Moteur electrique - Bruit anormal, roulements a remplacer |
| Statut | En reparation |
| Priorite | Haute |
| Date reception | 28 janvier 2026 |
| Livraison estimee | 5 fevrier 2026 |
| Technicien | Patrick Mutombo |
| Poste de travail | Poste A1 |
| Notes diagnostic | Roulements avant et arriere uses. Isolation stator OK. |
| Pieces utilisees | 2x Roulement 6316-2Z (120 USD) |
| Heures main-d'oeuvre | 8 heures |
| Cout estime | 850 USD |

Ce moteur de la Brasserie du Congo faisait un bruit anormal. Le diagnostic a revele que les roulements avant et arriere etaient uses. Patrick Mutombo est en train de les remplacer au Poste A1. L'isolation du stator a ete verifiee et elle est bonne, donc pas besoin de rebobinage.

---

**Ordre AT-2026-002 - Diagnostique**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-002 |
| Client | SNEL |
| Type | Transformateur |
| Marque / Modele | Schneider Trihal 1000 |
| N Serie | SCH-2018-4521 |
| Puissance | 1000 kVA |
| Description | Transformateur sec - Test dielectrique annuel + nettoyage |
| Statut | Diagnostique |
| Priorite | Normale |
| Date reception | 30 janvier 2026 |
| Livraison estimee | 10 fevrier 2026 |
| Technicien | Jean-Marie Kasongo |
| Notes diagnostic | Isolation correcte. Nettoyage complet necessaire. |

Ce transformateur de la SNEL (Societe Nationale d'Electricite) est la pour son test dielectrique annuel. Le diagnostic montre que l'isolation est correcte, mais un nettoyage complet est necessaire. C'est un entretien de routine.

---

**Ordre AT-2026-003 - Attente pieces**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-003 |
| Client | Ciment du Katanga |
| Type | Alternateur |
| Marque / Modele | Leroy-Somer LSA 49.3 |
| N Serie | LS-2020-9632 |
| Puissance | 500 kVA |
| Description | Alternateur GE - Rebobinage stator complet |
| Statut | Attente pieces |
| Priorite | Urgente |
| Date reception | 25 janvier 2026 |
| Livraison estimee | 8 fevrier 2026 |
| Techniciens | Patrick Mutombo, Serge Mwamba |
| Poste de travail | Poste B2 |
| Notes diagnostic | Court-circuit inter-spires sur phase U. Rebobinage complet requis. |
| Heures main-d'oeuvre (deja) | 4 heures |
| Cout estime | 3 500 USD |

Cet alternateur de 500 kVA du Ciment du Katanga a un probleme grave : un court-circuit inter-spires sur la phase U. Le diagnostic a ete fait et il faut un rebobinage complet du stator. Le travail est urgent car sans cet alternateur, le groupe electrogene du client ne peut pas fonctionner. On attend les pieces (fil emaille, resine) pour demarrer le rebobinage. Deux techniciens sont affectes vu la complexite du travail.

---

**Ordre AT-2026-004 - Receptionne**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-004 |
| Client | Brasserie du Congo |
| Type | Moteur |
| Marque / Modele | WEG W22 355M |
| N Serie | WEG-2021-1254 |
| Puissance | 185 kW |
| Description | Moteur pompe - Defaut d'isolement |
| Statut | Receptionne |
| Priorite | Normale |
| Date reception | 2 fevrier 2026 |

Ce moteur vient d'arriver a l'atelier. Il n'a pas encore ete examine par un technicien. La description mentionne un defaut d'isolement, mais le diagnostic complet reste a faire.

---

**Ordre AT-2026-005 - Controle qualite**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-005 |
| Client | Gecamines |
| Type | Transformateur |
| Marque / Modele | ABB RESIBLOC |
| N Serie | ABB-2017-3698 |
| Puissance | 2500 kVA |
| Description | Transformateur resine - Reparation bobinage HT |
| Statut | Controle qualite |
| Priorite | Haute |
| Date reception | 15 janvier 2026 |
| Livraison estimee | 3 fevrier 2026 |
| Technicien | Jean-Marie Kasongo |
| Poste de travail | Poste C1 |
| Notes diagnostic | Bobinage HT phase V endommage. Reparation effectuee. |
| Notes reparation | Bobinage remplace. Tests dielectriques OK a 28kV. |
| Pieces utilisees | 50x Fil emaille 4mm (450 USD), 5x Resine epoxy (280 USD) |
| Heures main-d'oeuvre | 32 heures |
| Cout estime | 4 200 USD |
| Cout final | 4 350 USD |

C'est un gros travail : un transformateur de 2500 kVA de la Gecamines dont le bobinage haute tension de la phase V etait endommage. La reparation a necessite 32 heures de main-d'oeuvre et l'utilisation de fil emaille et de resine epoxy. Les tests dielectriques a 28 kV sont passes avec succes. L'equipement est maintenant en controle qualite final avant d'etre declare pret.

---

**Ordre AT-2026-006 - Pret**

| Champ | Valeur |
|-------|--------|
| N Ordre | AT-2026-006 |
| Client | Texaf |
| Type | Moteur |
| Marque / Modele | Siemens 1LG6 280 |
| N Serie | SIE-2019-8741 |
| Puissance | 90 kW |
| Description | Moteur ventilateur - Revision generale |
| Statut | Pret |
| Priorite | Basse |
| Date reception | 20 janvier 2026 |
| Livraison estimee | 1 fevrier 2026 |
| Livraison effective | 1 fevrier 2026 |
| Technicien | Serge Mwamba |
| Poste de travail | Poste A2 |
| Notes reparation | Revision complete effectuee. Roulements, joints et graissage. |
| Pieces utilisees | 2x Roulement 6314-2RS (95 USD), 2x Joint SPI 80x100x10 (25 USD), 1x Graisse SKF LGMT3 (45 USD) |
| Heures main-d'oeuvre | 12 heures |
| Cout estime | 650 USD |
| Cout final | 680 USD |

Ce moteur de ventilateur de Texaf a recu une revision generale. Roulements remplaces, joints changes, graissage effectue. Le travail est termine et l'equipement est pret a etre recupere par le client. Le cout final (680 USD) est legerement superieur a l'estimation (650 USD) en raison de pieces supplementaires.

---

**Note :** Le septieme ordre de travail (avec statut "Livre") correspondrait a un equipement deja rendu au client. Dans les donnees de demonstration, les 6 ordres ci-dessus couvrent les statuts les plus courants.

---

## 11.2. Creer un Ordre de Travail

### Le formulaire de creation

Pour creer un nouvel ordre de travail, cliquez sur **"+ Nouvel ordre"** en haut de la page. Le formulaire demande les informations suivantes :

**Informations client et equipement :**

| Champ | Description | Exemple |
|-------|-------------|---------|
| Client | Nom du client | Brasserie du Congo |
| Type d'equipement | Moteur, Transformateur, Alternateur ou Autre | Moteur |
| Marque | Fabricant de l'equipement | ABB |
| Modele | Reference du modele | M3BP 315 |
| N de serie | Numero de serie unique | ABB-2019-7845 |
| Puissance | Puissance nominale | 250 kW |
| Description | Description du probleme ou du travail a effectuer | Bruit anormal au demarrage, roulements suspects |

**Planification :**

| Champ | Description | Exemple |
|-------|-------------|---------|
| Priorite | Basse, Normale, Haute ou Urgente | Haute |
| Date estimee de livraison | Quand le client pourra recuperer l'equipement | 2026-02-15 |

### Affectation des techniciens

Apres la creation de l'ordre, vous pouvez affecter un ou plusieurs techniciens. L'atelier dispose de 4 techniciens specialises :

| Technicien | Specialisation | Poste | Disponibilite |
|------------|---------------|-------|---------------|
| Patrick Mutombo | Moteurs | Poste A1 | Occupe (2 ordres en cours) |
| Jean-Marie Kasongo | Transformateurs | Poste C1 | Occupe (2 ordres en cours) |
| Serge Mwamba | Alternateurs | Poste B2 | Occupe (2 ordres en cours) |
| Joseph Nkulu | General | Poste A2 | Disponible |

L'application montre la charge de travail de chaque technicien et sa disponibilite, ce qui aide a repartir le travail de maniere equilibree.

### Attribution d'un poste de travail

L'atelier est organise en postes de travail identifies :
- **Poste A1** : Principalement pour les moteurs
- **Poste A2** : Poste polyvalent
- **Poste B2** : Pour les alternateurs et gros equipements
- **Poste C1** : Pour les transformateurs

Chaque poste dispose de l'outillage adapte au type d'equipement qu'il traite.

---

## 11.3. Suivi en Atelier

### Notes de diagnostic

Quand un technicien examine un equipement, il redige des notes de diagnostic. Ces notes sont stockees dans l'ordre de travail et restent accessibles a tout moment. Exemples :

- "Roulements avant et arriere uses. Isolation stator OK." (AT-2026-001)
- "Isolation correcte. Nettoyage complet necessaire." (AT-2026-002)
- "Court-circuit inter-spires sur phase U. Rebobinage complet requis." (AT-2026-003)
- "Bobinage HT phase V endommage. Reparation effectuee." (AT-2026-005)

### Notes de reparation

Apres le travail, le technicien documente ce qui a ete fait :

- "Bobinage remplace. Tests dielectriques OK a 28kV." (AT-2026-005)
- "Revision complete effectuee. Roulements, joints et graissage." (AT-2026-006)

### Suivi des pieces utilisees

Pour chaque ordre de travail, l'application enregistre les pieces utilisees avec leur quantite et leur cout. Ces pieces sont liees a l'inventaire (module Inventaire/Magasin), ce qui permet de mettre a jour automatiquement les stocks.

Exemple pour l'ordre AT-2026-005 (Transformateur Gecamines) :

| Piece | Reference | Quantite | Cout unitaire | Total |
|-------|-----------|----------|---------------|-------|
| Fil emaille 4mm | FIL-EMAIL-4MM | 50 bobines | 9 USD | 450 USD |
| Resine epoxy 1kg | RES-EPOXY-1KG | 5 pots | 56 USD | 280 USD |
| **Total pieces** | | | | **730 USD** |

Exemple pour l'ordre AT-2026-006 (Moteur Texaf) :

| Piece | Reference | Quantite | Cout unitaire | Total |
|-------|-----------|----------|---------------|-------|
| Roulement 6314-2RS | RLT-6314-2RS | 2 pieces | 47,50 USD | 95 USD |
| Joint SPI 80x100x10 | JNT-SPI-80 | 2 pieces | 12,50 USD | 25 USD |
| Graisse SKF LGMT3 1kg | GRS-LGMT3-1KG | 1 pot | 45 USD | 45 USD |
| **Total pieces** | | | | **165 USD** |

### Suivi des heures de main-d'oeuvre

Le temps passe par les techniciens est enregistre en heures. Voici un recapitulatif des ordres de demonstration :

| Ordre | Heures | Technicien(s) |
|-------|--------|---------------|
| AT-2026-001 | 8 h | Patrick Mutombo |
| AT-2026-002 | 0 h (diagnostic seulement) | Jean-Marie Kasongo |
| AT-2026-003 | 4 h (en cours) | Patrick Mutombo, Serge Mwamba |
| AT-2026-004 | 0 h (vient d'arriver) | Non affecte |
| AT-2026-005 | 32 h | Jean-Marie Kasongo |
| AT-2026-006 | 12 h | Serge Mwamba |

### Estimation et cout final

L'application distingue deux montants :
- **Cout estime** : l'estimation faite au moment du diagnostic, avant de commencer le travail
- **Cout final** : le cout reel une fois le travail termine

| Ordre | Cout estime | Cout final | Ecart |
|-------|------------|------------|-------|
| AT-2026-001 | 850 USD | En cours | - |
| AT-2026-003 | 3 500 USD | En cours | - |
| AT-2026-005 | 4 200 USD | 4 350 USD | +150 USD (+3,6%) |
| AT-2026-006 | 650 USD | 680 USD | +30 USD (+4,6%) |

Dans les deux cas termines, le cout final est legerement superieur a l'estimation, ce qui est normal. L'ecart reste faible (moins de 5%).

### Documentation photographique

L'application permet de joindre des photos a chaque ordre de travail. En pratique, les techniciens prennent des photos :
- **A la reception** : pour documenter l'etat de l'equipement a l'arrivee
- **Pendant le diagnostic** : pour montrer les problemes trouves (roulements uses, fils brules, etc.)
- **Pendant la reparation** : pour documenter le travail en cours
- **Apres la reparation** : pour montrer le resultat final

Ces photos sont utiles pour le client (elles prouvent le travail effectue) et pour la base de connaissances de l'equipe.

---

## 11.4. Exemples detailles avec les donnees de demonstration

### Exemple 1 : Reparation moteur ABB pour Brasserie du Congo

**Contexte :** La Brasserie du Congo (aussi appelee Brasimba dans certaines references) a envoye un moteur electrique ABB M3BP 315 de 250 kW a l'atelier. Le moteur faisait un bruit anormal en fonctionnement.

**Deroulement :**
1. Le moteur arrive a l'atelier le 28 janvier 2026
2. Il est enregistre sous le numero AT-2026-001
3. Patrick Mutombo, specialiste moteurs au Poste A1, l'examine
4. Le diagnostic revele que les roulements avant et arriere sont uses, mais que l'isolation du stator est en bon etat (pas besoin de rebobinage)
5. Les roulements 6316-2Z sont disponibles en stock (8 en stock, 4 minimum)
6. Patrick demonte le moteur, remplace les deux roulements, remonte et realigne
7. Temps de travail : 8 heures
8. Cout des pieces : 120 USD (2 roulements a 60 USD piece)
9. Cout total estime : 850 USD (pieces + main-d'oeuvre + marge)
10. Date de livraison prevue : 5 fevrier 2026

### Exemple 2 : Diagnostic transformateur Schneider pour SNEL

**Contexte :** La SNEL envoie un transformateur sec Schneider Trihal de 1000 kVA pour son test dielectrique annuel. C'est un entretien de routine obligatoire pour les gros transformateurs.

**Deroulement :**
1. Le transformateur arrive le 30 janvier 2026
2. Enregistre sous AT-2026-002
3. Jean-Marie Kasongo, specialiste transformateurs, effectue les tests
4. Resultat : l'isolation est correcte, pas de defaut. Un nettoyage complet est necessaire (poussiere accumulee).
5. Le transformateur est au stade "Diagnostique" - le nettoyage sera planifie
6. Pas de pieces necessaires, juste de la main-d'oeuvre de nettoyage
7. Date de livraison prevue : 10 fevrier 2026

### Exemple 3 : Rebobinage alternateur Leroy-Somer pour Ciment du Katanga

**Contexte :** L'alternateur Leroy-Somer LSA 49.3 de 500 kVA du Ciment du Katanga (aussi appele TFM dans certaines references) a subi un court-circuit inter-spires. C'est un travail complexe et urgent.

**Deroulement :**
1. L'alternateur arrive le 25 janvier 2026
2. Enregistre sous AT-2026-003, priorite URGENTE
3. Le diagnostic revele un court-circuit inter-spires sur la phase U du stator
4. Un rebobinage complet est necessaire - c'est un travail qui prend plusieurs jours
5. Deux techniciens sont affectes : Patrick Mutombo et Serge Mwamba (specialiste alternateurs)
6. Le poste B2 est utilise car il a l'espace necessaire pour un equipement de cette taille
7. Les pieces necessaires (fil emaille 4mm et resine epoxy d'isolation) ont ete commandees
8. Statut actuel : "Attente pieces"
9. 4 heures de travail deja effectuees (demontage et preparation)
10. Cout estime : 3 500 USD
11. Date de livraison prevue : 8 fevrier 2026

Ce type de reparation est parmi les plus complexes et les plus couteuses que l'atelier traite. Le rebobinage d'un alternateur de 500 kVA demande une expertise pointue et un travail minutieux.

---

# 12. Module Logistique

Le module Logistique gere l'approvisionnement en pieces, outils et vehicules necessaires pour les interventions. Il fait le lien entre le magasin (inventaire), la flotte de vehicules, et les interventions planifiees.

Vous y accedez via le menu lateral sous l'icone **Truck** avec le libelle "Logistique".

---

## 12.1. Demandes Logistiques

### La liste des demandes

Le tableau des demandes logistiques affiche :

| Colonne | Description |
|---------|-------------|
| **Intervention** | L'intervention liee a cette demande |
| **Type** | Le type de demande : Pieces, Vehicule ou Outils |
| **Articles** | La liste des articles demandes |
| **Statut** | L'etat de la demande |
| **Date demande** | Quand la demande a ete faite |
| **Date besoin** | Pour quand les articles sont necessaires |
| **Notes** | Commentaires eventuels |

### Les types de demandes

| Type | Icone | Description | Exemple |
|------|-------|-------------|---------|
| **Pieces** | Orange | Pieces de rechange a preparer pour une intervention | Filtres, huile, roulements |
| **Vehicule** | Bleu | Un vehicule est necessaire pour se rendre sur le site | Pick-up pour transporter l'equipe et le materiel |
| **Outils** | Violet | Des outils specifiques sont requis | Cle dynamometrique, multimetre, etc. |

### Les statuts d'une demande logistique

Les demandes suivent un parcours en 4 etapes :

| Statut | Couleur | Description |
|--------|---------|-------------|
| **En attente** | Jaune/ambre | La demande a ete creee mais pas encore traitee. Le responsable logistique doit la prendre en charge. |
| **Reserve** | Bleu | Les articles ont ete identifies et reserves dans le stock. Ils ne seront pas utilises pour autre chose. |
| **Pret** | Vert | Tout est prepare. Les pieces sont emballees, le kit est pret a etre emporte par l'equipe technique. |
| **Livre** | Gris | Les articles ont ete remis a l'equipe technique. La demande est cloturee. |

Le flux d'avancement :
```
En attente  -->  Reserve  -->  Pret  -->  Livre
```

### Donnees de demonstration

**Demande LOG-1 - Pret**

| Champ | Valeur |
|-------|--------|
| Intervention | INT-2 (Maintenance preventive 250h - Ambassade de France) |
| Type | Pieces |
| Statut | Pret |
| Articles demandes | |

| Article | Reference | Quantite |
|---------|-----------|----------|
| Filtre a air | PER-CH11038 | 1 |
| Filtre a huile | PER-2654407 | 1 |
| Huile moteur 15W-40 | Shell Rimula R4 | 35 litres |

Cette demande est prete. Toutes les pieces necessaires pour la maintenance du groupe Perkins de l'Ambassade de France sont preparees et n'attendent plus que le depart de l'equipe technique.

**Demande LOG-2 - En attente (URGENT)**

| Champ | Valeur |
|-------|--------|
| Intervention | INT-1 (Panne totale - Brasserie de Kinshasa) |
| Type | Pieces |
| Statut | En attente |
| Notes | URGENT - Production arretee |
| Articles demandes | |

| Article | Reference | Quantite |
|---------|-----------|----------|
| Batterie 12V | CAT-1535123 | 1 |
| Cables demarrage | - | 1 jeu |

Cette demande est urgente : la Brasserie de Kinshasa est a l'arret complet. Il faut trouver une batterie 12V compatible avec le Caterpillar C15 et des cables de demarrage. La demande est encore en attente de traitement.

### Creer une demande logistique

**Etape 1 :** Dans le module Logistique, cliquez sur **"+ Nouvelle demande"**

**Etape 2 :** Selectionnez l'intervention concernee dans le menu deroulant

**Etape 3 :** Choisissez le type de demande (Pieces, Vehicule, Outils)

**Etape 4 :** Ajoutez les articles necessaires :
- Nom de l'article
- Reference (si connue)
- Quantite

**Etape 5 :** Indiquez la date a laquelle vous avez besoin des articles

**Etape 6 :** Ajoutez des notes si necessaire (par exemple "URGENT" ou "Verifier compatibilite avant envoi")

**Etape 7 :** Enregistrez la demande

### Lier une demande a une intervention

Chaque demande logistique est liee a une intervention. Cela permet de :
- Savoir quelles pieces ont ete commandees pour quelle intervention
- Verifier que la logistique est prete avant d'envoyer l'equipe sur site
- Calculer le cout total d'une intervention (pieces + main-d'oeuvre + transport)

Dans le detail d'une intervention, on voit si la logistique est prete ou non grace a deux indicateurs :
- **needsLogistics** : oui/non - est-ce que l'intervention necessite des pieces ou outils ?
- **logisticsReady** : oui/non - est-ce que tout est pret ?

Si la logistique n'est pas prete, l'intervention ne devrait pas demarrer.

---

## 12.2. Gestion des demandes

### Approuver ou rejeter une demande

Le responsable logistique peut :
- **Approuver** une demande : les articles sont marques comme "Reserves"
- **Rejeter** une demande : si les articles ne sont pas disponibles ou si la demande n'est pas justifiee

### Suivre la livraison

Une fois les articles prepares, le responsable logistique fait avancer le statut vers "Pret". L'equipe technique est notifiee que le kit est pret a etre recupere.

### Preparer des kits pour les interventions

Pour les maintenances planifiees, la logistique peut preparer des "kits" a l'avance. Par exemple, pour une maintenance 250h d'un groupe Perkins 2000 Series, le kit standard comprend :

| Article | Quantite |
|---------|----------|
| Filtre a air PER-CH11038 | 1 |
| Filtre a huile PER-2654407 | 1 |
| Filtre a carburant PER-26560163 | 1 |
| Huile Shell Rimula R4 15W-40 | 35 L |

Ces kits sont prepares la veille de l'intervention et poses dans la zone de depart de l'atelier.

### Vue d'ensemble de la logistique

Le tableau de bord logistique affiche des cartes de statistiques :
- Nombre total de demandes
- Demandes en attente (a traiter en priorite)
- Demandes en cours de preparation
- Demandes pretes (a livrer)

Des filtres permettent de trier par type (pieces, vehicule, outils) et par statut.

---

# 13. Module Charroi / Flotte de Vehicules

Le module Charroi gere la flotte de vehicules d'AEMI. Les vehicules sont essentiels pour transporter les techniciens et le materiel jusqu'aux sites d'intervention, souvent eloignes (Lubumbashi, Bas-Congo, Muanda...).

Vous y accedez via le menu lateral sous l'icone **Truck** (ou **Car**) avec le libelle "Charroi".

---

## 13.1. Liste des Vehicules

### Le tableau de la flotte

La page Charroi affiche un tableau avec les vehicules de la flotte. Voici les colonnes :

| Colonne | Description |
|---------|-------------|
| **Nom** | Le nom usuel du vehicule (ex: "Land Cruiser 1") |
| **Type** | La categorie du vehicule (Pick-up, SUV, Camionnette, etc.) |
| **Immatriculation** | La plaque d'immatriculation au format HK (Haut-Katanga) |
| **Marque** | Le constructeur (Toyota, Mitsubishi, etc.) |
| **Modele** | Le modele exact |
| **Statut** | L'etat actuel du vehicule |
| **Kilometrage** | Le compteur kilometrique |

### Les statuts d'un vehicule

| Statut | Couleur | Pastille | Description |
|--------|---------|----------|-------------|
| **Disponible** | Vert | Verte | Le vehicule est au depot, pret a partir. Il peut etre affecte a une mission. |
| **En utilisation** | Bleu | Bleue | Le vehicule est actuellement en mission. Un chauffeur est au volant. |
| **En maintenance** | Ambre | Ambre | Le vehicule est au garage pour un entretien ou une reparation. Il n'est pas disponible. |
| **Hors service** | Rouge | Rouge | Le vehicule est immobilise pour une longue duree (panne grave, attente de pieces importees, etc.). |

### Les 6 vehicules de demonstration

Voici la flotte de vehicules presente dans l'application :

**Vehicule 1 - Toyota Land Cruiser 79**

| Champ | Valeur |
|-------|--------|
| Nom | Land Cruiser 1 |
| Type | Pick-up |
| Immatriculation | HK 4521 AB |
| Marque | Toyota |
| Modele | Land Cruiser 79 |
| Annee | 2022 |
| Kilometrage | 45 200 km |
| Statut | En utilisation |
| Chauffeur affecte | Michel Kalala |
| Assurance expire le | 15 juin 2026 |
| Prochain entretien | 12 mars 2026 |

Le Land Cruiser 79 est le vehicule de reference pour les missions en terrain difficile. C'est un pick-up robuste, adapte aux routes non goudronnees qu'on trouve souvent en dehors des centres urbains en RDC. Il est actuellement en mission avec Michel Kalala au volant.

**Vehicule 2 - Mitsubishi L200**

| Champ | Valeur |
|-------|--------|
| Nom | L200 Equipe |
| Type | Pick-up double cabine |
| Immatriculation | HK 7832 CD |
| Marque | Mitsubishi |
| Modele | L200 |
| Annee | 2021 |
| Kilometrage | 67 800 km |
| Statut | Disponible |
| Chauffeur affecte | Andre Mbala |
| Assurance expire le | 20 avril 2026 |
| Prochain entretien | 25 fevrier 2026 |

Le L200 double cabine peut transporter 4 techniciens plus du materiel a l'arriere. Il est disponible pour la prochaine mission.

**Vehicule 3 - Toyota Hilux**

| Champ | Valeur |
|-------|--------|
| Nom | Hilux Logistique |
| Type | Pick-up |
| Immatriculation | HK 2156 EF |
| Marque | Toyota |
| Modele | Hilux |
| Annee | 2020 |
| Kilometrage | 89 500 km |
| Statut | En maintenance |
| Prochain entretien | En cours |

Ce Hilux est actuellement au garage pour son entretien regulier. Avec 89 500 km au compteur, il est important de bien l'entretenir.

**Vehicule 4 - Mitsubishi Pajero**

| Champ | Valeur |
|-------|--------|
| Nom | Pajero Direction |
| Type | SUV |
| Immatriculation | HK 9045 GH |
| Marque | Mitsubishi |
| Modele | Pajero |
| Annee | 2023 |
| Kilometrage | 23 100 km |
| Statut | Disponible |
| Assurance expire le | 10 aout 2026 |
| Prochain entretien | 15 mai 2026 |

Le Pajero est le vehicule de la direction, utilise pour les deplacements importants ou les visites de clients. Plus confortable que les pick-ups, il sert aussi pour les trajets longue distance.

**Vehicule 5 - Toyota Dyna**

| Champ | Valeur |
|-------|--------|
| Nom | Dyna Transport |
| Type | Camion leger |
| Immatriculation | HK 5578 IJ |
| Marque | Toyota |
| Modele | Dyna |
| Annee | 2019 |
| Kilometrage | 112 400 km |
| Statut | Disponible |
| Prochain entretien | 1 mars 2026 |

Le Dyna est un camion leger utilise pour transporter les groupes electrogenes ou les equipements lourds. Il est indispensable pour les installations et les manutentions.

**Vehicule 6 - Mitsubishi Canter**

| Champ | Valeur |
|-------|--------|
| Nom | Canter Atelier |
| Type | Camion |
| Immatriculation | HK 3367 KL |
| Marque | Mitsubishi |
| Modele | Canter |
| Annee | 2021 |
| Kilometrage | 54 300 km |
| Statut | Disponible |
| Prochain entretien | 20 avril 2026 |

Le Canter sert principalement pour les transports entre l'atelier et les sites clients. Il peut transporter des equipements de taille moyenne (moteurs, alternateurs).

### Resume de la flotte

| Statut | Nombre |
|--------|--------|
| Disponible | 4 |
| En utilisation | 1 |
| En maintenance | 1 |
| Hors service | 0 |
| **Total** | **6** |

---

## 13.2. Gestion de flotte

### Details d'un vehicule

Quand vous cliquez sur un vehicule dans la liste, une section de details se deplie. Elle affiche :

**Informations generales :**
- Marque et modele
- Annee de mise en circulation
- Numero d'immatriculation (format HK pour Haut-Katanga)
- Kilometrage actuel

**Chauffeur affecte :**
- Nom du chauffeur principal
- Telephone de contact
- Le chauffeur peut etre reassigne si necessaire

**Suivi d'assurance :**
- Date d'expiration de l'assurance
- Un avertissement s'affiche quand l'assurance arrive a echeance dans les 30 prochains jours
- Cela permet de renouveler l'assurance a temps

**Prochain entretien :**
- Date du prochain entretien programme
- Le type d'entretien (vidange, revision complete, etc.)
- Un avertissement quand la date approche

### Calendrier de disponibilite des vehicules

L'application permet de visualiser la disponibilite des vehicules sur une periode donnee. Cela aide a planifier les missions :
- Si deux interventions sont prevues le meme jour, on verifie qu'il y a assez de vehicules disponibles
- Si un vehicule part pour une longue mission (par exemple Lubumbashi, a 1 800 km de Kinshasa), il faut compter plusieurs jours d'indisponibilite

---

## 13.3. Demandes de Vehicule

### Comment demander un vehicule pour une intervention

Quand un superviseur planifie une intervention qui necessite un vehicule, il cree une demande de vehicule.

**Le formulaire de demande :**

| Champ | Description | Exemple |
|-------|-------------|---------|
| Destination | Ou le vehicule doit aller | Mine Site Alpha, Lubumbashi |
| Lieu de depart | D'ou part le vehicule | Atelier AEMI, Gombe |
| Type de vehicule | Quel type est necessaire | Pick-up, Camionnette, Camion |
| Date prevue | Quand le vehicule doit partir | 2026-02-16 |
| Heure prevue | A quelle heure | 07:30 |
| Notes | Informations complementaires | Trajet long - prevoir ravitaillement |

### Les statuts d'une demande de vehicule

| Statut | Couleur | Description |
|--------|---------|-------------|
| **En attente** | Ambre | La demande a ete soumise, le responsable charroi doit la traiter |
| **Confirme** | Bleu | Un vehicule et un chauffeur ont ete affectes |
| **En cours** | Cyan | Le vehicule est parti, la mission est en route |
| **Termine** | Vert | Le vehicule est rentre au depot |
| **Annule** | Rouge | La demande a ete annulee |

### Donnees de demonstration

**Demande VEH-1 - Confirmee**

| Champ | Valeur |
|-------|--------|
| Intervention | INT-2 (Maintenance Ambassade de France) |
| Chauffeur | Michel Kalala |
| Type vehicule | Pick-up |
| Depart | Atelier AEMI, Gombe |
| Destination | Ambassade de France, Gombe |
| Date | Demain |
| Heure | 07:30 |
| Statut | Confirme |

Un pick-up est reserve avec Michel Kalala pour emmener l'equipe technique a l'Ambassade de France demain matin a 7h30. Le trajet est court (Gombe a Gombe), donc le vehicule sera de retour dans la journee.

**Demande VEH-2 - En cours**

| Champ | Valeur |
|-------|--------|
| Intervention | INT-4 (Maintenance 500h Mining Corp) |
| Chauffeur | Michel Kalala |
| Type vehicule | Camionnette |
| Depart | Atelier AEMI, Gombe |
| Destination | Mine Site Alpha, Lubumbashi |
| Date | Aujourd'hui |
| Heure | 05:00 |
| Statut | En cours |
| Notes | Trajet long - prevoir ravitaillement |

Cette mission est en cours. Michel Kalala est parti a 5h du matin avec la camionnette pour emmener l'equipe jusqu'a Lubumbashi (environ 1 800 km depuis Kinshasa). La note rappelle de prevoir du carburant en route car les stations-service sont rares sur certains troncons.

### Affectation du chauffeur

L'application dispose de deux chauffeurs dans les donnees de demonstration :

| Chauffeur | Telephone | Statut |
|-----------|-----------|--------|
| Michel Kalala | +243 81 000 0003 | Actif |
| Andre Mbala | +243 81 000 0007 | Actif |

Quand une demande de vehicule est confirmee, un chauffeur est affecte. Le systeme montre la disponibilite de chaque chauffeur pour eviter les conflits (un chauffeur ne peut pas etre sur deux missions en meme temps).

### Suivi du trajet

Pour chaque demande, on enregistre :
- Le lieu de depart et la destination
- L'heure de depart prevue
- L'heure de depart effective
- L'heure d'arrivee
- Le kilometrage au depart et a l'arrivee

Cela permet de calculer la distance parcourue et de suivre la consommation de carburant.

---

# 14. Module Reporting et Analytiques

Le module Reporting est le centre d'analyse de l'application. Il transforme toutes les donnees brutes (interventions, equipements, factures) en graphiques et indicateurs faciles a lire.

Vous y accedez via le menu lateral sous l'icone **BarChart3** avec le libelle "Reporting".

---

## 14.1. Dashboard Analytique

### Vue d'ensemble

La page Reporting s'ouvre sur un tableau de bord analytique complet. En haut, un selecteur de periode permet de choisir la plage de temps analysee :

| Periode | Description |
|---------|-------------|
| Cette semaine | Du lundi au dimanche de la semaine en cours |
| Ce mois | Du 1er au dernier jour du mois en cours |
| 3 derniers mois | Les 90 derniers jours |
| Cette annee | Depuis le 1er janvier |
| Personnalise | Choisissez vos propres dates de debut et fin |

### Les cartes de KPIs (indicateurs cles)

En haut du tableau de bord, des cartes affichent les indicateurs principaux :

**Carte 1 : Total interventions**
- Nombre total d'interventions sur la periode selectionnee
- Avec les donnees de demo : environ 13 interventions
- Fleche vers le haut ou le bas pour montrer la tendance par rapport a la periode precedente

**Carte 2 : Interventions terminees**
- Nombre d'interventions qui ont atteint le statut "Terminee", "Validee", "A facturer" ou "Facturee"
- C'est un indicateur d'efficacite : combien de travaux ont ete menes a bien

**Carte 3 : Temps moyen d'intervention (MTTR)**
- Mean Time To Repair - le temps moyen entre le debut et la fin d'une intervention
- S'exprime en heures ou en jours
- Un MTTR bas signifie que les equipes sont rapides

**Carte 4 : Cout moyen par intervention**
- Le cout moyen des interventions facturees
- Avec les donnees de demo, les montants vont de 800 000 CDF a 4 500 000 CDF
- Utile pour estimer les budgets futurs

**Carte 5 : Taux operationnel**
- Pourcentage d'equipements actuellement en statut "Operationnel"
- Avec les donnees de demo : sur 11 equipements, certains sont en panne, en maintenance ou hors service

**Carte 6 : Interventions en retard**
- Nombre d'interventions dont la date prevue est depassee
- C'est un indicateur d'alerte : plus ce nombre est eleve, plus la situation est preoccupante

**Carte 7 : Heures compteur total**
- Somme des heures compteur de tous les equipements geres
- Donne une idee du volume total d'equipements suivis

### Graphique : Interventions par mois (barres)

Ce graphique en barres montre le nombre d'interventions par mois. Chaque barre represente un mois, et la hauteur indique le nombre d'interventions realisees.

Utilite : Ce graphique permet de voir les tendances saisonnieres. Par exemple, pendant la saison des pluies en RDC (octobre a avril), les pannes de groupes electrogenes peuvent augmenter a cause de l'humidite et des inondations.

Exemple de lecture :
```
Janvier 2026 : ████████ 8 interventions
Decembre 2025 : ██████ 6 interventions
Novembre 2025 : ████ 4 interventions
```

### Graphique : Repartition par statut (camembert)

Un graphique circulaire (pie chart) montre la repartition des interventions par statut :

| Statut | Couleur | Pourcentage (exemple) |
|--------|---------|----------------------|
| Creee | Gris | 15% |
| Planifiee | Bleu | 8% |
| Affectee | Indigo | 8% |
| En cours | Ambre | 23% |
| Terminee | Emeraude | 8% |
| A facturer | Violet | 8% |
| Facturee | Violet fonce | 23% |

Utilite : On voit immediatement combien d'interventions sont en cours, combien sont en attente de facturation, etc.

### Graphique : Repartition par priorite

Un deuxieme camembert montre la repartition par niveau de priorite :

| Priorite | Couleur | Pourcentage (exemple) |
|----------|---------|----------------------|
| Urgente | Rouge | 15% |
| Haute | Orange | 30% |
| Normale | Bleu | 40% |
| Basse | Gris | 15% |

Utilite : Si beaucoup d'interventions sont urgentes ou de haute priorite, cela peut indiquer un probleme de maintenance preventive insuffisante.

### Graphique : Repartition par type

Ce graphique montre les types d'intervention :

| Type | Pourcentage (exemple) |
|------|----------------------|
| Reparation | 46% |
| Entretien (maintenance) | 38% |
| Constat (diagnostic) | 8% |
| Installation | 8% |
| Manutention | 0% |

Utilite : Un ratio eleve de reparations par rapport aux maintenances preventives peut signifier qu'on ne fait pas assez de maintenance planifiee. L'objectif est d'augmenter les maintenances preventives pour reduire les reparations d'urgence.

### Graphique : Temps moyen d'intervention par type

Ce graphique compare le temps moyen par type d'intervention :

| Type | Temps moyen (exemple) |
|------|----------------------|
| Installation | 8 heures |
| Reparation | 4 heures |
| Maintenance 500h | 3 heures |
| Maintenance 250h | 2 heures |
| Diagnostic | 1,5 heures |

### Graphique : Top clients par nombre d'interventions

Ce graphique en barres horizontales classe les clients par nombre d'interventions :

| Rang | Client | Nombre |
|------|--------|--------|
| 1 | Brasserie de Kinshasa | 4 interventions |
| 2 | Mining Corp International | 3 interventions |
| 3 | Ambassade de France | 2 interventions |
| 4 | Cimenterie Nationale | 1 intervention |
| 5 | Raffinerie Petroliere | 1 intervention |
| 6 | Hotel du Fleuve | 1 intervention |

Utilite : On identifie rapidement les clients les plus actifs. Brasserie de Kinshasa est le client avec le plus d'interventions, ce qui peut justifier un contrat de maintenance annuel.

### Detail par clic

Quand vous cliquez sur une carte KPI ou sur une section d'un graphique, un panneau lateral s'ouvre a droite de l'ecran. Ce panneau affiche le detail des interventions concernees dans un tableau :

| Colonne | Contenu |
|---------|---------|
| Reference | Le numero de l'intervention |
| Client | Le nom du client |
| Type | Reparation, Maintenance, etc. |
| Statut | L'etat actuel |
| Priorite | Le niveau de priorite |
| Date | La date planifiee |

C'est tres utile pour comprendre les chiffres. Par exemple, si vous voyez "3 interventions en retard", vous pouvez cliquer pour voir exactement lesquelles et agir en consequence.

---

## 14.2. Export PDF des rapports

### Generer un rapport PDF

Le module Reporting permet d'exporter un rapport complet en PDF. Ce rapport est utile pour :
- Les reunions de direction
- Les rapports mensuels aux clients (notamment ceux qui ont 5 equipements ou plus, comme Mining Corp International)
- Les archives

### Comment generer le rapport

**Etape 1 :** Selectionnez la periode souhaitee (ce mois, trimestre, personnalise)

**Etape 2 :** Cliquez sur le bouton **"Telecharger PDF"** (icone Download)

**Etape 3 :** Le rapport est genere et telecharge

### Contenu du rapport PDF

Le rapport PDF contient :

**Page de garde :**
- Titre : "Rapport d'activite AEMI GMAO"
- Periode couverte
- Date de generation

**Resume executif :**
- Tableau des KPIs principaux
- Comparaison avec la periode precedente

**Graphiques inclus :**
- Interventions par mois
- Repartition par statut
- Repartition par priorite
- Repartition par type

**Tableaux detailles :**
- Liste des interventions de la periode
- Couts par client
- Performances par technicien

**Selection de periode :**

| Option | Dates couvertes |
|--------|----------------|
| Ce mois | 1er au dernier jour du mois en cours |
| Mois precedent | 1er au dernier jour du mois passe |
| Ce trimestre | 3 mois en cours |
| Personnalise | Dates libres (debut et fin) |

---

## 14.3. Export CSV

### Exporter en CSV pour Excel

L'application permet d'exporter les donnees brutes au format CSV (Comma-Separated Values), compatible avec Excel, Google Sheets et d'autres tableurs.

### A quoi ca sert ?

Le CSV est utile quand vous voulez :
- Faire vos propres analyses dans Excel
- Creer des tableaux croises dynamiques
- Partager des donnees avec un comptable ou un controleur de gestion
- Importer les donnees dans un autre logiciel

### Comment exporter

**Etape 1 :** Allez dans la section souhaitee (Interventions, Clients, Equipements, etc.)

**Etape 2 :** Cliquez sur le bouton d'export (icone Download ou "Exporter CSV")

**Etape 3 :** Le fichier CSV se telecharge

### Format du fichier CSV

Exemple de contenu pour un export d'interventions :

```
Numero;Client;Type;Statut;Priorite;Date;Montant;Technicien
INT-1;Brasserie de Kinshasa;Reparation;Creee;Urgente;2026-02-10;-;Dieudonne Mutombo
INT-2;Ambassade de France;Maintenance 250h;Planifiee;Haute;2026-02-16;-;Patrick Ilunga
INT-3;Hotel du Fleuve;Maintenance 250h;Affectee;Normale;2026-02-16;-;Jean-Pierre Tshombe
INT-4;Mining Corp International;Maintenance 500h;En cours;Normale;2026-02-15;-;Dieudonne Mutombo
INT-5;Brasserie de Kinshasa;Reparation;En cours;Haute;2026-02-15;-;Patrick Ilunga
INT-6;Ambassade de France;Reparation;Terminee;Haute;2026-02-08;2 500 000;Dieudonne Mutombo
```

Les colonnes sont separees par des points-virgules, ce qui fonctionne bien avec Excel en francais.

### Modules qui supportent l'export CSV

| Module | Donnees exportables |
|--------|-------------------|
| Interventions | Liste complete avec tous les champs |
| Clients | Liste des clients et contacts |
| Equipements | Parc d'equipements avec heures compteur |
| Facturation | Devis et factures |
| Atelier | Ordres de travail |
| Inventaire | Stock de pieces de rechange |

---

## 14.4. KPIs expliques

Voici une explication detaillee de chaque indicateur cle de performance present dans le module Reporting.

### KPI 1 : Taux de resolution

**Definition :** Pourcentage d'interventions terminees avec succes sur le total des interventions de la periode.

**Formule :**
```
Taux de resolution = (Interventions terminees / Total interventions) x 100
```

**Exemple avec les donnees de demo :**
- Total : 13 interventions
- Terminees (statut Terminee, Validee, A facturer, Facturee) : environ 6
- Taux : 6/13 = 46%

**Pourquoi c'est important :** Un taux de resolution eleve signifie que les interventions sont menees a terme dans les delais. Un taux bas peut indiquer des blocages (manque de pieces, manque de techniciens, problemes d'acces aux sites).

**Objectif recommande :** 80% ou plus sur une periode d'un mois.

---

### KPI 2 : Temps moyen de reponse

**Definition :** Le temps moyen entre la demande du client et le debut effectif de l'intervention.

**Formule :**
```
Temps moyen = Moyenne de (Date debut - Date demande client) pour toutes les interventions
```

**Exemple :**
- INT-1 : Demande il y a 3 jours, pas encore commencee -> En retard
- INT-4 : Demande il y a 3 jours, commencee aujourd'hui -> 3 jours de delai

**Pourquoi c'est important :** Les clients attendent une reactivite rapide, surtout pour les pannes urgentes. Un temps de reponse court est un signe de qualite de service.

**Objectif recommande :**
- Interventions urgentes : moins de 4 heures
- Interventions haute priorite : moins de 24 heures
- Interventions normales : moins de 72 heures
- Interventions basse priorite : moins de 7 jours

---

### KPI 3 : Interventions par technicien

**Definition :** Le nombre d'interventions traitees par chaque technicien sur la periode.

**Donnees de demo :**

| Technicien | Nombre d'interventions | Specialites |
|------------|----------------------|-------------|
| Dieudonne Mutombo (Superviseur) | 4 | GE Caterpillar, Perkins, Diagnostic |
| Patrick Ilunga | 3 | GE Caterpillar, Electricite BT |
| Jean-Pierre Tshombe | 2 | GE Perkins, Cummins, Mecanique |
| Francois Lukusa | 2 | GE Volvo, MTU, Installation |

**Pourquoi c'est important :** Cela permet de verifier que la charge de travail est bien repartie entre les techniciens. Si un technicien a beaucoup plus d'interventions que les autres, il risque d'etre surcharge et de faire des erreurs.

**Ce que ca revele aussi :** Les specialites de chaque technicien. Dieudonne Mutombo, en tant que superviseur, est present sur de nombreuses interventions car il accompagne et supervise les travaux.

---

### KPI 4 : Cout moyen par intervention

**Definition :** Le montant moyen facture par intervention.

**Formule :**
```
Cout moyen = Somme des montants factures / Nombre d'interventions facturees
```

**Donnees de demo :**

| Intervention | Montant |
|-------------|---------|
| INT-6 | 2 500 000 CDF |
| INT-7 | 1 500 000 CDF |
| INT-8 | 4 500 000 CDF |
| INT-10 | 2 000 000 CDF |
| INT-11 | 1 800 000 CDF |
| INT-12 | 800 000 CDF |
| **Moyenne** | **2 183 333 CDF** |

**Pourquoi c'est important :** Ce KPI aide a :
- Fixer les prix des devis (on sait combien coute une intervention en moyenne)
- Negocier les contrats de maintenance avec les clients
- Identifier les interventions anormalement couteuses
- Comparer les couts d'un mois a l'autre

---

### KPI 5 : Taux de pannes vs maintenance preventive

**Definition :** Le ratio entre les interventions de reparation (pannes) et les interventions de maintenance preventive.

**Donnees de demo :**
- Reparations : 6 interventions (46%)
- Maintenances preventives : 4 interventions (31%)
- Diagnostics : 1 intervention (8%)
- Installations : 1 intervention (8%)
- Autre : 1 intervention (8%)

**Pourquoi c'est important :** Idealement, la maintenance preventive devrait representer la majorite des interventions. Si les reparations d'urgence sont trop nombreuses, cela signifie que :
- Les maintenances preventives ne sont pas assez frequentes
- Les seuils de maintenance (250h, 500h, 1000h) ne sont pas respectes
- Certains equipements sont trop vieux et devraient etre remplaces

**Objectif recommande :** 60% de maintenances preventives, 30% de reparations, 10% de diagnostics et installations.

---

### KPI 6 : Causes de pannes (Pareto)

**Definition :** Les causes de pannes classees par frequence. Le principe de Pareto dit que 20% des causes expliquent 80% des pannes.

**Donnees de demo :**

| Cause | Nombre | Pourcentage cumule |
|-------|--------|--------------------|
| Defaillance batterie | 1 | 17% |
| Fuite carburant | 1 | 33% |
| Probleme demarreur | 1 | 50% |
| Alternateur defectueux | 1 | 67% |
| Surchauffe moteur | 1 | 83% |
| Filtre colmate | 1 | 100% |

**Pourquoi c'est important :** En identifiant les causes de pannes les plus frequentes, on peut mettre en place des actions preventives ciblees. Par exemple, si les filtres colmates sont la cause numero 1, on peut reduire l'intervalle entre les changements de filtres.

---

### KPI 7 : Disponibilite du parc

**Definition :** Le pourcentage d'equipements en etat de fonctionnement a un instant donne.

**Donnees de demo :**

| Statut | Nombre | Pourcentage |
|--------|--------|-------------|
| Operationnel | 6 | 55% |
| En panne | 1 | 9% |
| Maintenance requise | 2 | 18% |
| En intervention | 1 | 9% |
| Hors service | 1 | 9% |
| **Total** | **11** | **100%** |

Taux de disponibilite : 6/11 = 55%

**Pourquoi c'est important :** Pour les clients, un groupe electrogene en panne signifie un arret de production ou une perte de confort. Le taux de disponibilite est un indicateur direct de la qualite de service.

**Objectif recommande :** 85% ou plus.

---

# 15. Module Parametres

Le module Parametres vous permet de personnaliser votre experience dans l'application. Vous y accedez via l'icone **Settings** (engrenage) en bas du menu lateral.

---

## 15.1. Profil Utilisateur

### Modifier vos informations personnelles

L'onglet "Profil" affiche vos informations actuelles et vous permet de les modifier :

| Champ | Description | Exemple |
|-------|-------------|---------|
| **Nom complet** | Votre nom et prenom | Clement Kabongo |
| **Email** | Votre adresse email professionnelle | c.kabongo@aemi.cd |
| **Telephone** | Votre numero de telephone | +243 81 000 0001 |
| **Role** | Votre role dans l'application (non modifiable) | Administrateur |

**Pour modifier votre profil :**
1. Cliquez sur l'onglet "Profil"
2. Modifiez les champs souhaites
3. Cliquez sur le bouton "Enregistrer"
4. Un message de confirmation apparait

### Les roles disponibles

Votre role determine ce que vous pouvez voir et faire dans l'application :

| Role | Description |
|------|-------------|
| **Administrateur** | Acces complet a toutes les fonctionnalites. Peut creer des utilisateurs, modifier les parametres, valider les interventions. |
| **Superviseur** | Gere les equipes et les interventions. Peut planifier, affecter et valider les interventions. |
| **Technicien** | Voit ses interventions assignees. Peut mettre a jour le statut, remplir les checklists, prendre des photos. |
| **Chauffeur** | Voit les missions de transport assignees. Peut confirmer les departs et arrivees. |
| **Agent Administratif** | Gere la facturation et la documentation. Peut creer des devis et des factures. |

### Changer votre mot de passe

**Etape 1 :** Dans l'onglet "Securite" ou "Profil", trouvez la section "Mot de passe"

**Etape 2 :** Saisissez votre mot de passe actuel

**Etape 3 :** Saisissez votre nouveau mot de passe (minimum 8 caracteres recommandes)

**Etape 4 :** Confirmez le nouveau mot de passe en le retapant

**Etape 5 :** Cliquez sur "Mettre a jour le mot de passe"

Un bouton oeil permet d'afficher ou masquer les mots de passe pendant la saisie, ce qui est pratique pour verifier ce que vous tapez.

### Avatar

Votre avatar est affiche dans le menu lateral et dans les pages ou votre nom apparait (par exemple dans les interventions qui vous sont assignees). L'avatar utilise par defaut les initiales de votre nom sur un fond de couleur.

---

## 15.2. Preferences

### Notifications

L'onglet "Notifications" permet de configurer les alertes que vous recevez. Chaque type de notification peut etre active ou desactive independamment.

**Notifications d'urgence :**

| Notification | Description | Active par defaut |
|-------------|-------------|-------------------|
| Interventions en retard | Alerte quand une intervention depasse sa date prevue | Oui |
| Equipement en panne | Notification immediate en cas de panne | Oui |

**Notifications de maintenance :**

| Notification | Description | Active par defaut |
|-------------|-------------|-------------------|
| Intervention assignee | Quand une intervention vous est affectee | Oui |
| Entretien requis | Alerte quand un equipement approche du seuil de maintenance | Oui |
| Interventions a venir | Rappel pour les interventions dans les 48 prochaines heures | Oui |

**Notifications logistiques :**

| Notification | Description | Active par defaut |
|-------------|-------------|-------------------|
| Stock bas | Alerte quand une piece atteint le seuil minimum | Oui |

**Notifications de facturation :**

| Notification | Description | Active par defaut |
|-------------|-------------|-------------------|
| Facturation en attente | Rappel pour les interventions terminees non facturees | Oui |

**Notifications generales :**

| Notification | Description | Active par defaut |
|-------------|-------------|-------------------|
| Rappel journalier | Resume des taches du jour, envoye chaque matin | Non |
| Rapport hebdomadaire | Resume d'activite envoye chaque lundi | Non |

Pour activer ou desactiver une notification, utilisez l'interrupteur (toggle switch) a cote de chaque option. L'interrupteur est bleu quand la notification est active, et gris quand elle est desactivee.

---

## 15.3. Mode Sombre (Dark Mode)

### Qu'est-ce que le mode sombre ?

Le mode sombre (dark mode) change l'apparence de toute l'application : au lieu d'un fond blanc avec du texte noir, l'ecran affiche un fond sombre (gris fonce ou noir) avec du texte clair.

### Comment l'activer

1. Allez dans les Parametres
2. Dans la section "Apparence" ou "Theme", vous avez trois options :
   - **Clair** (Light) : fond blanc, texte noir - le mode par defaut
   - **Sombre** (Dark) : fond sombre, texte clair
   - **Systeme** : l'application suit le reglage de votre ordinateur ou telephone

3. Cliquez sur l'option souhaitee
4. Le changement est immediat - toute l'application change d'apparence

### Toutes les pages supportent le mode sombre

L'application a ete concue pour que le mode sombre fonctionne sur toutes les pages :
- Le tableau de bord (Dashboard)
- Les pages de liste (Interventions, Clients, Equipements)
- Les formulaires de creation et modification
- Les graphiques du module Reporting
- Les tableaux de donnees
- Les dialogues et panneaux lateraux
- Le menu de navigation

### Pourquoi utiliser le mode sombre ?

| Avantage | Explication |
|----------|-------------|
| **Travail de nuit** | Si vous travaillez tard ou tot le matin, le mode sombre reduit la fatigue oculaire. Un ecran blanc dans l'obscurite est agressif pour les yeux. |
| **Faible luminosite** | Dans un atelier ou un bureau peu eclaire, le mode sombre est plus confortable. |
| **Economie de batterie** | Sur les ecrans OLED (smartphones et certains ordinateurs portables), le mode sombre consomme moins de batterie car les pixels noirs sont eteints. |
| **Preference personnelle** | Beaucoup de professionnels preferent simplement l'apparence du mode sombre. |

### Comparaison visuelle

**Mode clair :**
- Fond de page : blanc (#FFFFFF)
- Texte principal : noir/gris fonce
- Cartes : fond blanc avec bordure grise legere
- Sidebar (menu lateral) : fond gris tres clair
- Graphiques : barres colorees sur fond blanc

**Mode sombre :**
- Fond de page : gris tres fonce (#1A1A2E ou similaire)
- Texte principal : blanc/gris clair
- Cartes : fond gris fonce avec bordure subtile
- Sidebar : fond noir ou gris tres fonce
- Graphiques : barres colorees sur fond sombre

Les couleurs des badges de statut (vert, rouge, ambre, bleu) restent reconnaissables dans les deux modes, avec des ajustements pour garantir la lisibilite.

---

# 16. Carte Interactive

La carte interactive est un outil visuel qui montre l'emplacement de tous les equipements geres par AEMI sur une carte geographique. C'est un moyen immediat de visualiser ou se trouvent les sites clients et les interventions en cours.

Vous y accedez via le menu lateral sous l'icone **MapPin** avec le libelle "Carte".

---

## 16.1. Vue Carte

### Technologie utilisee

La carte est basee sur **Leaflet**, une librairie de cartographie open source, avec les fonds de carte d'**OpenStreetMap**. Cela signifie que :
- La carte est gratuite (pas de frais de licence comme avec Google Maps)
- Les donnees cartographiques sont maintenues par une communaute mondiale
- La carte fonctionne meme avec une connexion internet limitee (les tuiles sont mises en cache)

### Ce que vous voyez sur la carte

Quand vous ouvrez la page Carte, vous voyez :

**La carte :**
- Centree sur la zone **Lubumbashi / Kolwezi** dans le **Haut-Katanga, RDC**
- Avec un niveau de zoom qui montre toute la zone d'activite
- Les routes principales, les villes et les reperes geographiques

**Les marqueurs :**
- Chaque equipement avec des coordonnees GPS est represente par un marqueur sur la carte
- La couleur du marqueur indique le statut de l'equipement :

| Couleur du marqueur | Statut | Signification |
|--------------------|--------|---------------|
| Vert | Operationnel | L'equipement fonctionne normalement |
| Rouge | En panne | L'equipement est en panne, intervention urgente possible |
| Ambre/Orange | Entretien requis | L'equipement approche de son seuil de maintenance |
| Bleu | En intervention | Un technicien travaille actuellement sur cet equipement |
| Gris | Hors service | L'equipement est hors service |

### Interagir avec la carte

**Cliquer sur un marqueur :**
Quand vous cliquez sur un marqueur, une info-bulle (popup) s'affiche avec les informations de l'equipement :
- Nom de l'equipement
- Client proprietaire
- Marque et modele
- Puissance
- Statut actuel
- Nombre d'heures au compteur
- Date de la derniere intervention

**Zoomer :**
- Utilisez la molette de la souris pour zoomer et dezoomer
- Ou utilisez les boutons + et - en haut a gauche de la carte
- Vous pouvez aussi zoomer en double-cliquant sur la carte

**Naviguer :**
- Cliquez et faites glisser la carte pour vous deplacer
- Sur mobile, utilisez deux doigts pour zoomer et un doigt pour deplacer

### Filtrer les marqueurs

A cote de la carte, des filtres sont disponibles :

**Filtre par statut :**
- Cliquez sur un badge de statut pour n'afficher que les equipements avec ce statut
- Par exemple, cliquez sur "En panne" pour voir uniquement les equipements en panne sur la carte

**Barre de recherche :**
- Tapez le nom d'un client, d'un equipement, d'une marque ou d'un modele
- Les marqueurs sont filtres en temps reel

**Compteurs de statut :**
Sous la barre de recherche, des compteurs montrent combien d'equipements ont chaque statut. Avec les donnees de demo :

| Statut | Nombre |
|--------|--------|
| Operationnel | 6 |
| En panne | 1 |
| Entretien requis / En intervention | 3 |
| Hors service | 1 |

### Emplacements des equipements de demonstration

Voici les coordonnees GPS des equipements dans les donnees de demo :

| Equipement | Client | Localisation | Latitude | Longitude |
|-----------|--------|-------------|----------|-----------|
| GE Principal (CAT C15) | Brasserie de Kinshasa | Gombe, Kinshasa | -4.3217 | 15.3125 |
| Generateur Secours (Perkins) | Ambassade de France | Gombe, Kinshasa | -4.3089 | 15.2921 |
| Groupe Principal (Volvo Penta) | Hotel du Fleuve | Ngaliema, Kinshasa | -4.3156 | 15.2678 |
| Groupe Industriel (CAT C18) | Mining Corp | Lubumbashi | -11.6647 | 27.4794 |
| Generateur Backup (Perkins 4000) | Brasserie de Kinshasa | Gombe, Kinshasa | -4.3220 | 15.3130 |
| Groupe de Secours (Cummins) | Cimenterie Nationale | Bas-Congo | -5.8544 | 13.0458 |
| Groupe Principal (MTU) | Raffinerie Petroliere | Muanda | -5.9311 | 12.3497 |
| Groupe Secours Alpha (Cummins) | Mining Corp | Lubumbashi | -11.6650 | 27.4800 |
| Groupe Principal Beta (CAT C32) | Mining Corp | Lubumbashi | -11.6800 | 27.4900 |
| Groupe Secours Beta (Perkins) | Mining Corp | Lubumbashi | -11.6810 | 27.4910 |
| Groupe Mobile (CAT C9) | Mining Corp | Lubumbashi | -11.6660 | 27.4810 |

On voit clairement deux zones d'activite principales :
- **Kinshasa** (au nord-ouest) : Brasserie de Kinshasa, Ambassade de France, Hotel du Fleuve
- **Lubumbashi** (au sud-est) : Mining Corp International (5 equipements sur 2 sites)

Plus au sud-ouest, on trouve la Cimenterie Nationale (Bas-Congo) et la Raffinerie Petroliere (Muanda).

---

## 16.2. Utilisation pratique

### Voir toutes les interventions actives sur la carte

En filtrant par statut "En intervention" ou "En panne", vous voyez immediatement ou se trouvent les situations qui necessitent de l'attention. Par exemple :

- Le marqueur rouge a Lubumbashi indique que le Groupe Industriel de Mining Corp (CAT C18, 750 kVA) est en panne
- Le marqueur bleu a Gombe indique qu'un technicien travaille sur le Groupe Mobile de Mining Corp

### Planifier les tournees des techniciens

La carte aide a optimiser les deplacements :

**Scenario :** Deux interventions sont prevues demain a Kinshasa
1. Maintenance a l'Ambassade de France (Gombe) - coordonnees : -4.3089, 15.2921
2. Maintenance a l'Hotel du Fleuve (Ngaliema) - coordonnees : -4.3156, 15.2678

Sur la carte, on voit que ces deux sites sont proches (tous les deux dans l'ouest de Kinshasa). Il est logique de programmer les deux interventions la meme journee pour le meme technicien, en commencant par l'Ambassade le matin et l'Hotel l'apres-midi.

### Identifier les zones avec beaucoup d'interventions

En regardant la carte, on identifie que la zone de **Lubumbashi** concentre le plus d'equipements (5 sur 11, soit 45% du parc). C'est normal car Mining Corp International est un gros client industriel.

Cela peut justifier :
- L'ouverture d'un depot de pieces a Lubumbashi
- L'affectation d'un technicien permanent sur place
- Un vehicule dedie pour cette zone

### Coordonnees GPS pour chaque site

Les coordonnees GPS de chaque site sont enregistrees dans le systeme. Cela permet :
- De partager un lien de localisation avec le chauffeur
- D'estimer le temps de trajet entre l'atelier et le site
- De calculer les distances pour les frais de deplacement

---

# 16.3. Inventaire / Magasin

Le module Inventaire (aussi appele Magasin) gere le stock de pieces de rechange et de consommables necessaires aux interventions et aux reparations en atelier.

Vous y accedez via le menu lateral sous l'icone **Package** avec le libelle "Inventaire".

---

### La liste des pieces

Le tableau de l'inventaire affiche toutes les pieces en stock :

| Colonne | Description |
|---------|-------------|
| **SKU** | Le code de reference unique de la piece (ex: RLT-6316-2Z) |
| **Nom** | Le nom descriptif de la piece |
| **Categorie** | Le type de piece (Filtre, Huile, Courroie, etc.) |
| **Quantite** | Le nombre d'unites en stock |
| **Stock Min** | Le seuil minimum en dessous duquel une alerte est declenchee |
| **Stock Max** | La quantite maximale a stocker |
| **Cout unitaire** | Le prix d'une unite |
| **Emplacement** | Ou la piece est rangee dans le magasin |
| **Fournisseur** | Le fournisseur habituel |
| **Statut** | OK, Stock bas, Rupture ou Surstock |

### Les categories de pieces

| Categorie | Libelle | Exemples |
|-----------|---------|----------|
| **filter** | Filtres | Filtre a air, filtre a huile, filtre a carburant |
| **oil** | Huiles | Huile moteur 15W-40, huile hydraulique |
| **belt** | Courroies | Courroie trapezoidale, courroie poly-V |
| **bearing** | Roulements | Roulement a billes 6316-2Z, roulement a rouleaux |
| **electrical** | Electrique | Contacteur, fil emaille, fusible |
| **mechanical** | Mecanique | Joint SPI, joint de culasse, segment de piston |
| **consumable** | Consommable | Graisse, resine epoxy, chiffons |

### Les 15 articles de demonstration (11 en base + articles utilises)

Voici le detail complet de chaque article en stock :

---

**1. Roulement 6316-2Z**

| Champ | Valeur |
|-------|--------|
| SKU | RLT-6316-2Z |
| Categorie | Roulement |
| Description | Roulement a billes etanche |
| Quantite en stock | 8 pieces |
| Stock minimum | 4 pieces |
| Stock maximum | 20 pieces |
| Cout unitaire | 60 USD |
| Emplacement | Rayonnage A-12 |
| Fournisseur | SKF Congo |
| Dernier reapprovisionnement | 15 janvier 2026 |
| Statut | OK |

Ce roulement est utilise pour les moteurs electriques de taille moyenne. Il est en stock suffisant (8 pieces, bien au-dessus du minimum de 4).

---

**2. Roulement 6314-2RS**

| Champ | Valeur |
|-------|--------|
| SKU | RLT-6314-2RS |
| Categorie | Roulement |
| Quantite en stock | 12 pieces |
| Stock minimum | 5 pieces |
| Stock maximum | 25 pieces |
| Cout unitaire | 47,50 USD |
| Emplacement | Rayonnage A-11 |
| Fournisseur | SKF Congo |
| Statut | OK |

---

**3. Joint SPI 80x100x10**

| Champ | Valeur |
|-------|--------|
| SKU | JNT-SPI-80 |
| Categorie | Mecanique |
| Quantite en stock | 25 pieces |
| Stock minimum | 10 pieces |
| Stock maximum | 50 pieces |
| Cout unitaire | 12,50 USD |
| Emplacement | Rayonnage B-03 |
| Fournisseur | Etancheite Plus |
| Statut | OK |

---

**4. Graisse SKF LGMT3 1kg**

| Champ | Valeur |
|-------|--------|
| SKU | GRS-LGMT3-1KG |
| Categorie | Consommable |
| Quantite en stock | 6 pots |
| Stock minimum | 3 pots |
| Stock maximum | 15 pots |
| Cout unitaire | 45 USD |
| Emplacement | Rayonnage C-01 |
| Fournisseur | SKF Congo |
| Statut | OK |

---

**5. Huile 15W40 bidon 20L** -- STOCK BAS

| Champ | Valeur |
|-------|--------|
| SKU | HLE-15W40-20L |
| Categorie | Huile |
| Quantite en stock | 4 bidons |
| Stock minimum | 5 bidons |
| Stock maximum | 20 bidons |
| Cout unitaire | 85 USD |
| Emplacement | Zone huiles |
| Fournisseur | Total RDC |
| Derniere utilisation | 1 fevrier 2026 |
| **Statut** | **Stock bas** |

Attention : cet article est en dessous du seuil minimum. Il reste 4 bidons alors que le minimum est de 5. L'huile 15W-40 est utilisee tres frequemment pour les maintenances de groupes electrogenes. Il faut passer commande rapidement aupres de Total RDC.

---

**6. Filtre a air Caterpillar C18**

| Champ | Valeur |
|-------|--------|
| SKU | FLT-AIR-CAT-C18 |
| Categorie | Filtre |
| Quantite en stock | 3 pieces |
| Stock minimum | 2 pieces |
| Stock maximum | 10 pieces |
| Cout unitaire | 125 USD |
| Emplacement | Rayonnage D-05 |
| Fournisseur | Tractafric |
| Statut | OK |

Ce filtre est specifique aux groupes Caterpillar C18 (comme celui de Mining Corp International a Lubumbashi). Le stock est juste suffisant.

---

**7. Filtre a huile Caterpillar C18**

| Champ | Valeur |
|-------|--------|
| SKU | FLT-OIL-CAT-C18 |
| Categorie | Filtre |
| Quantite en stock | 5 pieces |
| Stock minimum | 3 pieces |
| Stock maximum | 12 pieces |
| Cout unitaire | 78 USD |
| Emplacement | Rayonnage D-06 |
| Fournisseur | Tractafric |
| Statut | OK |

---

**8. Courroie trapezoidale A68**

| Champ | Valeur |
|-------|--------|
| SKU | CRR-V-A68 |
| Categorie | Courroie |
| Quantite en stock | 8 pieces |
| Stock minimum | 4 pieces |
| Stock maximum | 20 pieces |
| Cout unitaire | 18 USD |
| Emplacement | Rayonnage E-02 |
| Fournisseur | Courroies Industrielles |
| Statut | OK |

---

**9. Contacteur 12V 80A** -- STOCK BAS

| Champ | Valeur |
|-------|--------|
| SKU | CON-12V-80A |
| Categorie | Electrique |
| Quantite en stock | 2 pieces |
| Stock minimum | 3 pieces |
| Stock maximum | 10 pieces |
| Cout unitaire | 145 USD |
| Emplacement | Rayonnage F-01 |
| Fournisseur | Schneider RDC |
| **Statut** | **Stock bas** |

Deuxieme article en alerte : il ne reste que 2 contacteurs alors que le minimum est de 3. Les contacteurs sont des composants electriques essentiels pour les tableaux de commande des groupes electrogenes.

---

**10. Fil emaille 4mm (bobine 10m)**

| Champ | Valeur |
|-------|--------|
| SKU | FIL-EMAIL-4MM |
| Categorie | Electrique |
| Quantite en stock | 15 bobines |
| Stock minimum | 5 bobines |
| Stock maximum | 30 bobines |
| Cout unitaire | 9 USD |
| Emplacement | Rayonnage F-10 |
| Fournisseur | Cableries du Congo |
| Statut | OK |

Ce fil est utilise pour les rebobinages de moteurs et d'alternateurs en atelier. Le stock est confortable.

---

**11. Resine epoxy isolation 1kg**

| Champ | Valeur |
|-------|--------|
| SKU | RES-EPOXY-1KG |
| Categorie | Consommable |
| Quantite en stock | 8 pots |
| Stock minimum | 4 pots |
| Stock maximum | 20 pots |
| Cout unitaire | 56 USD |
| Emplacement | Zone chimique |
| Fournisseur | Chimie Industrielle |
| Statut | OK |

La resine epoxy est utilisee apres les rebobinages pour isoler et proteger les enroulements. Elle doit etre stockee dans une zone dediee (zone chimique) a l'abri de la chaleur.

---

### Resume de l'inventaire par categorie

| Categorie | Nombre d'articles | Valeur totale en stock |
|-----------|------------------|-----------------------|
| Roulements | 2 articles | (8 x 60) + (12 x 47,50) = 1 050 USD |
| Mecanique | 1 article | 25 x 12,50 = 312,50 USD |
| Consommables | 2 articles | (6 x 45) + (8 x 56) = 718 USD |
| Huiles | 1 article | 4 x 85 = 340 USD |
| Filtres | 2 articles | (3 x 125) + (5 x 78) = 765 USD |
| Courroies | 1 article | 8 x 18 = 144 USD |
| Electrique | 2 articles | (2 x 145) + (15 x 9) = 425 USD |
| **Total** | **11 articles** | **3 754,50 USD** |

### Alertes de stock

L'application affiche des alertes visuelles pour les articles dont la quantite est en dessous du seuil minimum :

| Article | En stock | Minimum | Ecart | Alerte |
|---------|---------|---------|-------|--------|
| Huile 15W40 20L | 4 | 5 | -1 | **Stock bas** (badge ambre) |
| Contacteur 12V 80A | 2 | 3 | -1 | **Stock bas** (badge ambre) |

Si un article tombe a 0, le badge devient **"Rupture"** en rouge. C'est une situation critique qui peut bloquer des interventions.

### Les indicateurs de stock visuels

Pour chaque article, une petite barre de progression montre le niveau de stock :
- **Barre verte** : stock OK (entre le minimum et le maximum)
- **Barre ambre** : stock bas (en dessous du minimum)
- **Barre rouge** : rupture (quantite = 0)
- **Barre bleue** : surstock (au-dessus du maximum)

### Mouvements de stock

L'application permet d'enregistrer les entrees et sorties de stock :

**Entree de stock (reapprovisionnement) :**
1. Cliquez sur l'article concerne
2. Choisissez "Entree" (+)
3. Indiquez la quantite recue
4. Le stock est mis a jour

**Sortie de stock (utilisation) :**
1. Cliquez sur l'article concerne
2. Choisissez "Sortie" (-)
3. Indiquez la quantite utilisee
4. Le stock est mis a jour

### Suivi du reapprovisionnement

Pour chaque article, l'application enregistre :
- La date du dernier reapprovisionnement
- La date de la derniere utilisation
- Le fournisseur habituel

Cela permet de savoir quand passer la prochaine commande et aupres de quel fournisseur.

### Ajouter un nouvel article

**Etape 1 :** Cliquez sur **"+ Nouvel article"**

**Etape 2 :** Remplissez le formulaire :

| Champ | Description |
|-------|-------------|
| Nom | Le nom descriptif (ex: "Roulement 6316-2Z") |
| SKU | Le code de reference (ex: "RLT-6316-2Z") |
| Categorie | Filtre, Huile, Courroie, Roulement, Electrique, Mecanique ou Consommable |
| Quantite initiale | Combien d'unites en stock |
| Stock minimum | Le seuil d'alerte |
| Stock maximum | La quantite maximale |
| Cout unitaire | Le prix d'une unite |
| Unite | piece, bidon, pot, bobine, etc. |
| Emplacement | Ou ranger l'article (ex: "Rayonnage A-12") |
| Fournisseur | Le nom du fournisseur |

**Etape 3 :** Cliquez sur "Creer"

### Recherche et filtrage dans l'inventaire

Vous pouvez filtrer l'inventaire de plusieurs manieres :
- **Par recherche textuelle** : tapez le nom, le SKU ou le fournisseur
- **Par categorie** : selectionnez une categorie dans le menu deroulant (Filtres, Huiles, etc.)
- **Par statut de stock** : affichez uniquement les articles en stock bas, en rupture, ou tous

---

# Conclusion de la Partie 3

Clement, cette troisieme partie a couvert les modules complementaires de l'application AEMI GMAO :

1. **Facturation** : Gestion complete des devis et factures, avec le cycle Intervention -> Devis -> Facture -> Paiement et l'export PDF

2. **Atelier** : Suivi des reparations en atelier avec 7 statuts d'avancement, gestion des pieces, heures de main-d'oeuvre et couts

3. **Logistique** : Gestion des demandes de pieces, vehicules et outils pour les interventions

4. **Charroi** : Flotte de 6 vehicules avec suivi du kilometrage, de l'assurance et de la disponibilite

5. **Reporting** : Tableaux de bord avec graphiques, export PDF et CSV, et KPIs detailles

6. **Parametres** : Profil utilisateur, notifications configurables et mode sombre

7. **Carte interactive** : Visualisation geographique de tous les equipements avec filtrage par statut

8. **Inventaire** : Stock de pieces de rechange avec alertes de stock bas et suivi des mouvements

Chaque module est interconnecte : une intervention peut declencher une demande logistique, qui utilise des pieces du stock, necessite un vehicule du charroi, et aboutit a un devis puis une facture. Le reporting agrege toutes ces donnees pour donner une vision d'ensemble.

L'application est accessible a l'adresse : **https://aemi-gmao.vercel.app**

---

*Document prepare par ExplorIA pour Clement - Fevrier 2026*
# AEMI GMAO - Document de Presentation - PARTIE 4

**Application :** AEMI GMAO - Gestion de Maintenance des Groupes Electrogenes
**URL :** [https://aemi-gmao.vercel.app](https://aemi-gmao.vercel.app)
**Client :** Clement
**Agence :** ExplorIA
**Date :** Fevrier 2026

---

# Table des Matieres - Partie 4

- 17. Vue Technicien Mobile
- 18. Architecture Technique
- 19. Supabase - La Base de Donnees
- 20. Securite
- 21. ExplorIA - L'Agence
- 22. Design & Experience Utilisateur
- 23. Donnees de Demonstration
- 24. Ce qui est en Production vs Demo
- 25. Prochaines Etapes & Roadmap v2
- 26. FAQ - Questions Frequentes
- 27. Contact & Support

---

# 17. Vue Technicien Mobile

Clement, cette section est probablement la plus importante du document. C'est ici qu'on va detailler tout ce que vos techniciens voient et font quand ils sont sur le terrain. L'idee, c'est que vous puissiez suivre chaque etape comme si vous aviez le telephone en main.

On a concu cette vue mobile en pensant a un technicien qui se trouve quelque part dans le Katanga, sur un site minier, ou dans Kinshasa, et qui doit effectuer une intervention de facon autonome. Il ouvre son telephone, il voit ses missions, il les fait, il envoie tout. Vous, de votre cote, vous recevez toutes les informations.

---

## 17.1 Acces Technicien

### Comment se connecter en tant que technicien

Pour tester la vue technicien, vous avez deux comptes de demonstration :

| Champ       | Technicien 1                | Technicien 2                  |
|-------------|----------------------------|-------------------------------|
| **Email**   | `tech1@aemi.cd`            | `tech2@aemi.cd`               |
| **Mot de passe** | `aemi2026`            | `aemi2026`                    |
| **Nom**     | Patrick Ilunga             | Jean-Pierre Tshombe           |
| **Telephone** | +243 81 000 0004         | +243 81 000 0005              |
| **Competences** | GE Caterpillar, Electricite BT | GE Perkins, GE Cummins, Mecanique |

### Etapes de connexion

1. Rendez-vous sur [https://aemi-gmao.vercel.app](https://aemi-gmao.vercel.app)
2. Sur la page de connexion, entrez par exemple `tech1@aemi.cd` et `aemi2026`
3. Cliquez sur "Se connecter"
4. L'application detecte automatiquement le role "technician" attache au profil
5. Au lieu d'afficher le tableau de bord administrateur, elle redirige directement vers la vue mobile

### Detection automatique du role

Quand quelqu'un se connecte, l'application regarde le champ `role` du profil utilisateur. Si ce role est `technician`, l'application fait deux choses :

- Elle redirige toutes les URLs vers les routes technicien (`/technician`, `/technician/history`, `/technician/profile`)
- Elle empeche l'acces aux pages d'administration (si un technicien tape `/interventions` dans la barre d'adresse, il est automatiquement renvoyee vers `/technician`)

Cela veut dire que vos techniciens ne peuvent pas voir le tableau de bord administrateur, ni les pages de facturation, ni les parametres. Ils ont uniquement acces a leurs missions, leur historique et leur profil.

### L'interface mobile

La vue technicien est concue specifiquement pour les telephones. Voici les contraintes techniques :

| Caracteristique | Detail |
|-----------------|--------|
| **Largeur maximale** | 448 pixels (taille `max-w-md`) |
| **Hauteur** | Occupe toute la hauteur de l'ecran (100dvh) |
| **Bords** | Des bordures laterales apparaissent sur tablette/desktop pour simuler un ecran de telephone |
| **Defilement** | Le contenu defilable est independant de l'en-tete et de la barre de navigation |
| **Zone tactile** | Tous les boutons font au minimum 44x44 pixels (norme d'accessibilite) |

Si vous ouvrez cette vue sur votre ordinateur, vous verrez qu'elle est centree au milieu de l'ecran avec des bordures a gauche et a droite. C'est normal. Sur un vrai telephone, elle occupe tout l'ecran.

---

## 17.2 La barre de navigation

En bas de l'ecran, il y a une barre de navigation avec 3 onglets principaux et un bouton d'installation :

| Onglet | Icone | Description |
|--------|-------|-------------|
| **Taches** | Liste a cocher | La page principale avec toutes les interventions assignees |
| **Historique** | Horloge | La liste des interventions passees et terminees |
| **Profil** | Silhouette | Les informations personnelles du technicien |
| **Installer** | Fleche vers le bas | Permet d'installer l'application comme une application native sur le telephone |

Cette barre est fixee en bas de l'ecran. Elle ne bouge pas quand le technicien fait defiler le contenu. L'onglet actif est mis en evidence visuellement.

### Installation en tant qu'application

Le bouton "Installer" permet au technicien d'ajouter l'application sur l'ecran d'accueil de son telephone. Cela fonctionne differemment selon le systeme :

**Sur Android (Chrome) :**
1. Cliquer sur "Installer"
2. Une boite de dialogue apparait "Installer AEMI"
3. Confirmer
4. L'application apparait sur l'ecran d'accueil comme n'importe quelle autre application

**Sur iPhone (Safari) :**
1. Cliquer sur "Installer"
2. Un guide apparait en bas de l'ecran avec 3 etapes :
   - Etape 1 : Appuyez sur le bouton Partager (en bas de Safari)
   - Etape 2 : Choisissez "Sur l'ecran d'accueil"
   - Etape 3 : Appuyez "Ajouter"

Une fois installee, l'application s'ouvre en plein ecran, sans la barre d'adresse du navigateur. Ca donne vraiment l'impression d'une application native.

---

## 17.3 Onglet Taches (Page Principale)

Quand le technicien arrive sur la page principale, voici ce qu'il voit de haut en bas :

### L'en-tete

L'en-tete est fixe en haut de l'ecran. Il contient :

- **Le logo AEMI** : une petite image ronde a gauche
- **Un message de bienvenue** : "Bonjour, Patrick" (le prenom est extrait du nom complet)
- **La date du jour** : par exemple "samedi 15 fevrier" en francais
- **Un indicateur GPS** : un petit badge vert "GPS" si la geolocalisation est disponible, rouge si elle ne l'est pas
- **Un bouton de rafraichissement** : pour recharger les donnees

L'indicateur GPS est important parce que le mode intervention utilise la position du technicien pour calculer la distance au site. Si le GPS n'est pas disponible, le technicien le voit tout de suite.

### Les statistiques du jour

Juste sous l'en-tete, il y a une barre de statistiques avec 3 tuiles :

| Statistique | Icone | Description |
|-------------|-------|-------------|
| **Terminees** | Cercle coche vert | Nombre d'interventions completees aujourd'hui |
| **Travaillees** | Minuteur bleu | Nombre d'heures travaillees aujourd'hui |
| **A faire** | Eclair jaune | Nombre d'interventions encore a realiser |

Par exemple, si Patrick a termine 2 interventions ce matin et qu'il lui en reste 3, il verra : "2 Terminees | 4.5h Travaillees | 3 A faire".

Les heures travaillees sont calculees automatiquement a partir des horodatages de debut et de fin de chaque intervention, plus le temps de l'intervention en cours si il y en a une.

### La banniere d'intervention en cours

Si le technicien a une intervention avec le statut "en cours" (`in_progress`), une grande banniere bleue apparait tout en haut de la liste. Cette banniere est tres visible avec un degrade bleu-indigo. Elle affiche :

- **Le texte "Intervention en cours"** : avec une icone lecture
- **Le nom du client** : en gros caracteres
- **L'equipement** : marque, modele et puissance du groupe electrogene
- **Le type d'intervention** : Entretien, Reparation, etc.
- **La priorite** : Normale, Haute, Urgente
- **Un minuteur en temps reel** : qui montre depuis combien de temps l'intervention est en cours (par exemple "1h 23m 45s"). Ce minuteur se met a jour chaque seconde.
- **Un bouton "Itineraire"** : si le site a des coordonnees GPS, ce bouton ouvre Google Maps avec l'itineraire vers le site

Le technicien peut appuyer sur cette banniere pour revenir directement au mode intervention.

### Les sections de la liste d'interventions

Les interventions sont organisees en sections, dans cet ordre :

**1. Urgentes / En retard (rouge)**

Cette section apparait uniquement s'il y a des interventions en retard ou urgentes. Elle est identifiee par un triangle d'alerte rouge. On y trouve :
- Les interventions dont la date prevue est passee et qui ne sont pas encore terminees
- Les interventions marquees comme "urgentes" meme si elles ne sont pas encore en retard

Pour les interventions en retard, un badge rouge affiche le nombre de jours de retard. Par exemple : "3j retard".

**2. Aujourd'hui (bleu)**

Les interventions prevues pour aujourd'hui qui ne sont ni urgentes ni en retard. Si aucune intervention n'est prevue pour aujourd'hui, un message "Aucune intervention pour aujourd'hui" s'affiche avec une icone verte.

**3. A venir (gris)**

Les interventions dont la date prevue est dans le futur. Elles sont classees par date croissante.

**Si aucune intervention n'existe**, un grand ecran vide s'affiche avec le message "Aucune intervention - Vous n'avez aucune tache assignee".

### Les cartes d'intervention

Chaque intervention est representee par une carte. Voici ce que chaque carte contient :

```
+-----------------------------------------------+
| [Urgente]  [Reparation]  [3j retard]    >     |
|                                                |
| Mining Corp International                      |
| [Cle] Caterpillar - C18 - 750 kVA             |
| [Pin] Zone Industrielle Nord, Lubumbashi       |
|                                                |
| Remplacement alternateur defectueux...         |
|                                                |
| 15 jan. | 09:00 | [Affectee]    [Tel] [GPS]   |
+-----------------------------------------------+
```

Chaque element en detail :

| Element | Description |
|---------|-------------|
| **Badge de priorite** | Couleur selon la priorite : rouge = urgent, ambre = haute, bleu = normale, gris = basse |
| **Badge de type** | Couleur selon le type : rose = reparation, emeraude = entretien, violet = constat, bleu ciel = installation |
| **Badge de retard** | Affiche le nombre de jours de retard si applicable |
| **Nom du client** | En gras, en gros caracteres |
| **Equipement** | Marque, modele et puissance du groupe electrogene |
| **Adresse du site** | L'adresse du site d'intervention |
| **Description** | Un apercu de la description de l'intervention (2 lignes max) |
| **Date** | La date prevue au format "15 jan." |
| **Heure** | L'heure prevue si elle est definie |
| **Statut** | Un badge colore : Affectee, Planifiee, En route, etc. |
| **Bouton telephone** | Appuyer dessus appelle directement le contact du client |
| **Bouton GPS** | Appuyer dessus ouvre Google Maps avec l'itineraire vers le site |

Les boutons telephone et GPS fonctionnent directement. Quand le technicien appuie sur le bouton telephone, son application telephone s'ouvre avec le numero pre-rempli. Quand il appuie sur le bouton GPS, Google Maps s'ouvre avec l'itineraire calcule.

### Le tri des interventions

Les interventions sont triees automatiquement dans cet ordre :
1. D'abord les interventions "en cours" (`in_progress`)
2. Ensuite les interventions en retard
3. Ensuite par priorite (urgent > haute > normale > basse)
4. Enfin par date prevue (les plus proches en premier)

Le technicien n'a pas besoin de trier manuellement. L'application organise tout pour mettre les choses les plus importantes en haut.

---

## 17.4 Le Mode Intervention (le coeur du systeme)

C'est ici que tout se passe. Quand le technicien appuie sur une carte d'intervention, un ecran plein prend le relais. Cet ecran guide le technicien a travers 5 etapes sequentielles, de la preparation a la validation finale.

### La structure de l'ecran

L'ecran d'intervention a 3 zones :

1. **L'en-tete fixe** : avec le nom du client, le type d'intervention, l'equipement, la priorite, et surtout le stepper (indicateur d'etapes)
2. **Le contenu defilable** : qui change selon l'etape
3. **La barre de navigation en bas** : avec les boutons Precedent et Suivant

### Le stepper (indicateur d'etapes)

En haut de l'ecran, sous les informations de l'intervention, il y a un indicateur visuel des 5 etapes :

```
  [1]       [2]       [3]       [4]       [5]
Mission   Trajet   Travail   Photos   Resume
```

Chaque etape est representee par un cercle avec une icone :
- **Etape completee** : cercle vert avec une coche
- **Etape en cours** : cercle bleu avec un halo lumineux
- **Etape a venir** : cercle gris clair

Il y a aussi une barre de progression sous les cercles qui se remplit au fur et a mesure que le technicien avance.

Le technicien peut appuyer sur n'importe quelle etape pour y revenir. Par exemple, s'il est a l'etape 4 (Photos) et qu'il veut revoir les details de la mission (etape 1), il peut appuyer dessus.

### Le minuteur flottant

A partir de l'etape 3 (Travail), un minuteur bleu apparait tout en haut de l'ecran. Il montre le temps ecoule au format `HH:MM:SS`. Ce minuteur est toujours visible, meme quand le technicien fait defiler le contenu. Il peut le mettre en pause ou le reprendre avec un petit bouton.

---

### Etape 1 : Mission

C'est la premiere chose que le technicien voit quand il ouvre une intervention. Cette etape sert a prendre connaissance de la mission avant de partir.

#### Les details de l'intervention

Une carte blanche avec des coins arrondis affiche :

| Information | Exemple |
|-------------|---------|
| **Date et heure** | 2026-02-15 a 09:00 |
| **Description** | Entretien preventif 500h - verifier niveaux, changer filtres |
| **Type** | Entretien 500h |
| **Priorite** | Normale |
| **Duree estimee** | 120 min |
| **Logistique** | Prete / En attente / Non requise |

La description est le texte que vous (Clement) avez saisi lors de la creation de l'intervention. C'est ici que le technicien lit ce qu'on attend de lui.

#### Les informations sur l'equipement

Une carte depliable montre les details du groupe electrogene. Par defaut, elle est repliee et affiche juste le nom et la marque/modele. Le technicien peut l'ouvrir pour voir :

| Champ | Exemple |
|-------|---------|
| **Ref. client** | BK-GE-001 |
| **N. serie** | CAT-2021-C15-001234 |
| **Puissance** | 500 kVA |
| **Compteur** | 4750h |
| **Carburant** | Diesel |
| **Reservoir** | 1000L |

C'est utile pour que le technicien puisse verifier qu'il intervient sur le bon equipement et qu'il a les bonnes pieces de rechange.

#### Les informations sur le site

Une autre carte affiche :

- **Le nom du site** : par exemple "Usine Principale Gombe"
- **L'adresse** : 123 Boulevard du 30 Juin
- **La localite** : Gombe

Si le site a des contraintes d'acces, elles sont affichees dans un encadre jaune/ambre. Par exemple : "Acces par le portail principal, badge obligatoire" ou "Zone SEVESO, formation securite requise". C'est important pour que le technicien sache a quoi s'attendre avant d'arriver.

Un grand bouton vert "Ouvrir dans Google Maps" permet de lancer la navigation GPS.

#### Le contact du client

Sous les informations du site, le contact principal est affiche avec :
- Son nom et sa fonction
- Un bouton "Appeler" qui lance directement l'appel

#### Les notes du superviseur

Si vous (ou un superviseur) avez ajoute des notes lors de la planification de l'intervention, elles apparaissent dans un encadre bleu. Par exemple : "Attention, le client signale des vibrations anormales depuis 2 semaines".

#### Le bouton "Demarrer la mission"

En bas de l'ecran, un grand bouton bleu avec une icone lecture dit "Demarrer la mission". Quand le technicien appuie dessus :

1. Le statut de l'intervention passe de "assigned" a "en_route"
2. L'heure de depart du trajet est enregistree (`travel_start_time`)
3. L'application passe automatiquement a l'etape 2 (Trajet)
4. En base de donnees, ces informations sont sauvegardees immediatement

---

### Etape 2 : Trajet

Cette etape represente le temps de deplacement entre la base du technicien et le site d'intervention.

#### La distance au site

Au centre de l'ecran, un grand indicateur montre la distance entre la position actuelle du technicien et le site :

```
        [Icone boussole]
      Distance au site
         12.3 km
      Precision: 15m
```

Si le GPS est en cours de chargement, un petit spinner s'affiche avec "Localisation en cours...". Si le GPS n'est pas disponible, le message "Position GPS indisponible" s'affiche.

La distance est calculee en utilisant la formule de Haversine (la distance a vol d'oiseau entre deux points GPS). Elle se met a jour en temps reel au fur et a mesure que le technicien se deplace.

#### Le bouton de navigation

Un grand bouton vert "Naviguer vers le site" ouvre Google Maps en mode navigation avec la destination pre-remplie. L'application Google Maps prend le relais pour guider le technicien sur la route.

#### Le bouton d'appel

Un bouton bleu "Appeler [Nom du contact]" permet d'appeler le contact du site pour prevenir de son arrivee.

#### Les informations du site (rappel)

Un petit resume du site est affiche en bas : nom, adresse, et contraintes d'acces si il y en a.

#### Le bouton "Je suis arrive"

Quand le technicien arrive sur le site, il appuie sur le bouton "Je suis arrive". Cela declenche :

1. Le statut passe a "in_progress"
2. L'heure d'arrivee est enregistree (`arrival_time`)
3. L'heure de debut d'intervention est enregistree (`started_at`)
4. Si le technicien avait saisi un compteur horaire de debut, il est aussi enregistre
5. Le minuteur de travail demarre
6. L'application passe a l'etape 3 (Travail)

A ce moment-la, en tant qu'administrateur, vous pouvez voir dans votre tableau de bord que l'intervention est passee "en cours".

---

### Etape 3 : Travail

C'est l'etape principale. Le technicien est sur le site, devant le groupe electrogene, et il fait son travail. Cette etape contient beaucoup d'informations a remplir.

#### Le minuteur de travail

En haut de l'ecran, un grand minuteur affiche le temps de travail au format `HH:MM:SS`. Le technicien peut le mettre en pause (par exemple pendant une pause dejeuner) et le reprendre.

```
    Temps de travail
      01:23:45
         [Pause]
```

#### Le releve du compteur horaire

Deux champs cote a cote :

| Champ | Description |
|-------|-------------|
| **Heures debut** | Le compteur horaire du groupe electrogene au debut de l'intervention. Pre-rempli avec la valeur connue (par ex. 4750h) |
| **Heures fin** | Le compteur horaire a la fin de l'intervention. A remplir par le technicien |

Ces compteurs sont importants pour le suivi de la maintenance preventive. Si un groupe a 4750h et que le prochain entretien est a 5000h, vous savez qu'il reste 250h.

#### La checklist

C'est probablement la partie la plus importante de l'etape Travail. La checklist est une liste de points de controle que le technicien doit verifier et valider.

La checklist est differente selon le type d'intervention. Voici les 4 checklists disponibles :

**Checklist Entretien (maintenance) - 10 items :**

| # | Point de controle | Obligatoire | Categorie |
|---|-------------------|-------------|-----------|
| 1 | Niveau d'huile verifie | Oui | Fluides |
| 2 | Filtres a air changes | Oui | Filtres |
| 3 | Filtres a huile changes | Oui | Filtres |
| 4 | Filtres a carburant verifies | Oui | Filtres |
| 5 | Tension courroies controlee | Oui | Mecanique |
| 6 | Tension batterie OK (>=12.4V) | Oui | Electrique |
| 7 | Niveau liquide refroidissement verifie | Oui | Fluides |
| 8 | Test de demarrage effectue | Oui | Fonctionnel |
| 9 | Releve compteur horaire note | Oui | Mesures |
| 10 | Nettoyage general effectue | Non | General |

**Checklist Reparation (repair) - 5 items :**

| # | Point de controle | Obligatoire |
|---|-------------------|-------------|
| 1 | Diagnostic effectue | Oui |
| 2 | Cause de la panne identifiee | Oui |
| 3 | Pieces remplacees documentees | Oui |
| 4 | Test de fonctionnement reussi | Oui |
| 5 | Client informe | Oui |

**Checklist Constat/Diagnostic (diagnosis) - 7 items :**

| # | Point de controle | Obligatoire |
|---|-------------------|-------------|
| 1 | Inspection visuelle complete | Oui |
| 2 | Releve compteur horaire | Oui |
| 3 | Test demarrage | Oui |
| 4 | Mesures electriques (tension, frequence) | Oui |
| 5 | Verification niveaux fluides | Oui |
| 6 | Photos avant/apres | Oui |
| 7 | Rapport remis au client | Oui |

**Checklist Installation - 9 items :**

| # | Point de controle | Obligatoire |
|---|-------------------|-------------|
| 1 | Emplacement verifie et conforme | Oui |
| 2 | Groupe positionne et cale | Oui |
| 3 | Raccordements electriques effectues | Oui |
| 4 | Raccordements carburant effectues | Oui |
| 5 | Mise a la terre verifiee | Oui |
| 6 | Remplissage fluides effectue | Oui |
| 7 | Test de mise en service reussi | Oui |
| 8 | Formation utilisateur dispensee | Non |
| 9 | Documentation remise au client | Oui |

Le fonctionnement de la checklist :

1. Chaque item est affiche sur une ligne avec un cercle vide a gauche
2. Le technicien appuie sur la ligne pour cocher l'item
3. L'item coche devient vert avec une icone de coche, et le texte est barre
4. Les items obligatoires non coches affichent un badge "Requis" en jaune
5. En haut de la checklist, un compteur montre la progression : "7/10"
6. Une barre de progression change de couleur :
   - Moins de 50% : ambre (jaune)
   - Plus de 50% : bleu
   - 100% : vert
7. Un message d'alerte indique combien de points obligatoires restent a completer

Le technicien ne peut pas valider l'intervention tant que tous les points obligatoires ne sont pas coches. C'est une securite pour s'assurer que le travail est bien fait.

#### Les notes de travail

Un champ de texte libre permet au technicien de prendre des notes pendant le travail. Par exemple : "Fuite detectee au niveau du joint de culasse cote droit, reserrage effectue."

#### Le bouton "Signaler un probleme"

Si le technicien rencontre un probleme sur le terrain (piece manquante, acces bloque, securite compromise...), il peut appuyer sur ce bouton bordure en pointilles rouges. Un formulaire s'ouvre :

1. Le technicien decrit le probleme
2. Il appuie sur "Envoyer"
3. Le probleme est enregistre dans la base de donnees avec la categorie "terrain" et une criticite "medium"
4. Vous (Clement) pouvez voir ces problemes dans le detail de l'intervention

---

### Etape 4 : Photos

Cette etape est dediee a la documentation photographique de l'intervention. L'application permet de prendre des photos dans 4 categories :

#### Photos Avant (bleu)

- Ce sont les photos prises avant le debut du travail
- Elles documentent l'etat initial du groupe electrogene
- Le technicien appuie sur le bouton "Ajouter" pour ouvrir la camera de son telephone
- La camera s'ouvre en mode "environnement" (camera arriere)
- Les photos sont compressees automatiquement avant d'etre sauvegardees
- Maximum 10 photos par categorie
- Les photos s'affichent en grille (3 colonnes)
- Le technicien peut supprimer une photo en appuyant sur le petit "X" dans le coin

#### Photos Pendant (ambre/jaune)

- Ce sont les photos prises pendant le travail
- Par exemple : une photo du filtre colmate qu'on est en train de changer
- Meme fonctionnement que les photos "avant"

#### Photos Apres (vert)

- Ce sont les photos prises apres le travail
- Elles documentent l'etat final du groupe electrogene
- Par exemple : le nouveau filtre installe, le niveau d'huile correct

#### Fiche d'Intervention (photo speciale)

C'est un cas particulier. Beaucoup de techniciens remplissent encore une fiche papier sur le terrain. Cette option leur permet de prendre une photo de cette fiche papier. Contrairement aux autres categories :
- Une seule photo est autorisee
- Le bouton affiche "Photographier la fiche"
- Si le technicien veut reprendre la photo, il appuie sur "Reprendre"
- L'affichage est en format paysage (comme un document)

#### Signature du client

Sur cette meme etape, il y a un module de capture de signature. Le client dessine sa signature directement sur l'ecran du telephone :

```
+------------------------------------------+
|  [Stylo] Signature Client                |
|                                          |
|  Le client signe ci-dessous pour         |
|  confirmer l'intervention                |
|                                          |
|  +------------------------------------+ |
|  |                                    | |
|  |         Signez ici                 | |
|  |                                    | |
|  +------------------------------------+ |
|                                          |
|  [Annuler]  [Effacer]  [Valider]        |
+------------------------------------------+
```

Le fonctionnement :
1. Le client dessine sa signature avec le doigt sur un canvas (zone de dessin)
2. Le trait s'adapte a la pression (trait fin si on va vite, plus epais si on appuie)
3. Le bouton "Annuler" revient un trait en arriere
4. Le bouton "Effacer" efface toute la signature
5. Le bouton "Valider" sauvegarde la signature comme image
6. Une fois validee, la signature s'affiche dans un encadre vert avec le message "Signature enregistree"
7. Le bouton "Recommencer" permet de refaire la signature

La signature est sauvegardee soit dans Supabase Storage (si configure), soit en tant que Data URL (image encodee en base64). Dans les deux cas, vous pouvez la voir dans le detail de l'intervention.

---

### Etape 5 : Resume & Validation

C'est la derniere etape. Le technicien revoit tout ce qu'il a fait et saisit ses conclusions.

#### Travaux realises

Un champ de texte ou le technicien decrit ce qu'il a fait. Par exemple :
> "Entretien 500h effectue. Changement filtres air, huile et carburant. Vidange huile moteur (45L). Verification courroies et tensions. Test de demarrage OK."

#### Diagnostic

Un champ de texte pour le diagnostic technique. Par exemple :
> "Groupe en bon etat general. Legere usure sur la courroie principale, a surveiller. Batterie a 12.6V."

#### Recommandations

Un champ de texte pour les recommandations au client. Par exemple :
> "Prevoir remplacement courroie au prochain entretien (1000h). Verifier le niveau de refroidissement chaque semaine."

#### Le tableau de verification

Un tableau recapitulatif montre l'etat de chaque element :

| Element | Statut | Detail |
|---------|--------|--------|
| **Checklist** | Coche vert ou Triangle jaune | Pourcentage de completion (ex: 100%) |
| **Photos** | Coche vert ou Triangle jaune | Nombre total de photos (ex: 8 photos) |
| **Signature client** | Coche vert ou Triangle jaune | "Oui" ou "Non" |
| **Fiche d'intervention** | Coche vert ou Triangle jaune | "Oui" ou "Non" |
| **Compteur horaire** | Coche vert ou Triangle jaune | Valeurs debut et fin (ex: 4750h -> 4752h) |
| **Temps de travail** | Minuteur bleu | Temps total (ex: 02:15:30) |

#### Le detail des photos

Un tableau visuel montre combien de photos ont ete prises dans chaque categorie :

```
+----------+----------+----------+----------+
|   Avant  |  Pendant |   Apres  |  Fiche   |
|     3    |     2    |     3    |     1    |
+----------+----------+----------+----------+
```

#### L'apercu de la signature

Si une signature a ete capturee, elle est affichee dans un encadre vert.

#### Les avertissements

Si des elements manquent, un encadre jaune d'avertissement s'affiche. Par exemple :
- "Checklist incomplete (7/9 obligatoires)"
- "Signature client manquante"
- "Fiche d'intervention non photographiee"

#### Le bouton "Valider l'intervention"

Le grand bouton vert "Valider l'intervention" est actif seulement si :
1. Tous les points obligatoires de la checklist sont coches
2. Au moins une signature OU une photo de fiche est presente

Si ces conditions ne sont pas remplies, le bouton est grise et inactif.

Quand le technicien appuie sur le bouton :

1. Le statut de l'intervention passe a "completed"
2. L'heure de completion est enregistree (`completed_at`)
3. Le compteur horaire de fin est enregistre (`hours_at_end`)
4. Les travaux realises, le diagnostic et les recommandations sont sauvegardes
5. La checklist complete (avec l'etat de chaque item) est sauvegardee
6. Les URLs des photos (avant, pendant, apres) sont sauvegardees
7. L'URL de la photo de la fiche d'intervention est sauvegardee
8. L'URL de la signature est sauvegardee
9. Un spinner de chargement s'affiche brievement
10. Le technicien est redirige vers la liste des taches

Toutes ces donnees sont envoyees a la base de donnees en une seule operation de mise a jour.

---

## 17.5 Ce que l'administrateur voit apres la validation

Clement, c'est ici que ca devient interessant pour vous. Une fois que le technicien a valide l'intervention, voici ce que vous pouvez voir dans la page de detail de l'intervention (cote administrateur) :

| Donnee | Source | Ou la voir |
|--------|--------|-----------|
| **Statut "Terminee"** | Changement automatique | Badge de statut dans la liste et le detail |
| **Heure de debut** | `started_at` | Timeline de l'intervention |
| **Heure d'arrivee** | `arrival_time` | Timeline de l'intervention |
| **Heure de completion** | `completed_at` | Timeline de l'intervention |
| **Compteur debut/fin** | `hours_at_start` / `hours_at_end` | Section technique |
| **Travaux realises** | `work_done` | Section resultats |
| **Diagnostic** | `diagnosis` | Section resultats |
| **Recommandations** | `recommendations` | Section resultats |
| **Checklist complete** | `checklist[]` | Section checklist avec indicateurs OK/NOK |
| **Photos avant/pendant/apres** | `photos_before[]`, `photos_during[]`, `photos_after[]` | Galerie photos |
| **Photo de la fiche** | `intervention_sheet_photo` | Section documents |
| **Signature du client** | `client_signature` | Image affichee |
| **Problemes signales** | `problems[]` | Section incidents |

Tout est la. Vous n'avez rien a deviner. Le technicien a tout documente, et vous pouvez tout revoir a tete reposee.

A partir de la, vous pouvez :
1. Valider l'intervention (passer le statut de "Terminee" a "Validee")
2. Creer un devis ou une facture
3. Planifier la prochaine intervention

---

## 17.6 Onglet Historique

Quand le technicien appuie sur "Historique" dans la barre de navigation, il arrive sur la page de l'historique de ses interventions.

### L'en-tete

Un bouton retour a gauche et le titre "Historique" avec le nombre total d'interventions terminees.

### Les statistiques

Trois tuiles en haut :

| Tuile | Couleur | Contenu |
|-------|---------|---------|
| **Total** | Vert | Nombre total d'interventions terminees |
| **Pannes** | Rouge | Nombre de reparations effectuees |
| **Entretiens** | Bleu | Nombre d'entretiens effectues |

### La recherche et les filtres

- **Barre de recherche** : Le technicien peut chercher par nom de client ou d'equipement
- **Filtres par type** : Des boutons en forme de pilules permettent de filtrer par "Tous", "Pannes", "Entretiens", "Constats"

### La liste des interventions

Chaque intervention passee est affichee dans une carte avec :
- Le type d'intervention (badge colore)
- La date de completion
- Le nom du client
- L'equipement (marque, modele, puissance)
- L'adresse du site
- Le statut "Termine" avec une coche verte
- Un apercu des travaux realises

Le technicien peut appuyer sur une carte pour revoir le detail complet de l'intervention.

Les interventions sont triees de la plus recente a la plus ancienne.

---

## 17.7 Onglet Profil

La page de profil du technicien contient :

### Informations personnelles

- **Avatar** : Les initiales du technicien dans un cercle colore (par exemple "PI" pour Patrick Ilunga)
- **Nom complet** : Patrick Ilunga
- **Role** : Un badge "Technicien"

### Carte de performance

Une carte avec un degrade bleu affiche les statistiques :

| Statistique | Description |
|-------------|-------------|
| **Terminees** | Nombre total d'interventions completees |
| **En cours** | Nombre d'interventions actuellement en cours |
| **Ce mois** | Nombre d'interventions completees ce mois-ci |

### Statistiques rapides

Deux tuiles supplementaires :
- **Cette semaine** : Nombre d'interventions completees les 7 derniers jours
- **Planifiees** : Nombre d'interventions a venir

### Informations de contact

- **Email** : tech1@aemi.cd (ou l'email reel)
- **Telephone** : +243 81 000 0004 (cliquable pour appeler)

### Competences

Si le profil du technicien a des competences definies, elles sont affichees comme des badges. Par exemple :
- "GE Caterpillar"
- "Electricite BT"

Ou pour Jean-Pierre :
- "GE Perkins"
- "GE Cummins"
- "Mecanique"

### Bouton de deconnexion

Un bouton rouge "Se deconnecter" permet au technicien de se deconnecter de l'application.

---

## 17.8 Navigation generale

Quelques notes sur la navigation dans la vue technicien :

- **Le bouton retour** (fleche vers la gauche) est present sur chaque page secondaire (Historique, Profil, Mode Intervention). Il ramene toujours a la page precedente.
- **La barre de navigation en bas** est presente sur toutes les pages sauf le mode intervention (qui a sa propre navigation par etapes).
- **Le defilement** fonctionne naturellement. Le contenu defilable est separe de l'en-tete fixe et de la barre de navigation fixe.
- **Les animations** sont subtiles : les cartes reagissent au toucher (legere reduction de taille), les transitions entre pages sont fluides.
- **Le rafraichissement** des donnees peut se faire manuellement avec le bouton dans l'en-tete.

---

# 18. Architecture Technique

Clement, cette section explique comment l'application est construite techniquement. On ne va pas entrer dans le code, mais on va vous donner une vue d'ensemble pour que vous compreniez les choix qu'on a faits et pourquoi.

---

## 18.1 Technologies Utilisees

Voici la liste de toutes les technologies qui composent l'application, avec une explication simple pour chacune :

| Technologie | Version | Role | Explication simple |
|-------------|---------|------|-------------------|
| **React** | 18 | Interface utilisateur | C'est la bibliotheque qui rend les pages interactives. Quand vous cliquez sur un bouton et que quelque chose change a l'ecran sans recharger la page, c'est React qui fait ca. |
| **TypeScript** | 5.8 | Typage du code | C'est comme ajouter des regles au code pour eviter les erreurs. Par exemple, si un champ doit etre un nombre, TypeScript va avertir le developpeur s'il essaie d'y mettre du texte. Resultat : moins de bugs. |
| **Vite** | 5.4 | Outil de developpement | C'est l'outil qui transforme le code source en application fonctionnelle. Il est tres rapide, ce qui permet de developper plus vite. |
| **Tailwind CSS** | 3.4 | Styles visuels | C'est le systeme qui donne son apparence a l'application (couleurs, espacements, tailles, bordures). Au lieu d'ecrire des fichiers CSS separes, les styles sont directement dans le code des composants. |
| **shadcn/ui** | - | Composants d'interface | Ce sont des composants pre-faits et bien testes : boutons, menus deroulants, tableaux, formulaires, dialogues, etc. Ils sont coherents visuellement et accessibles. |
| **Supabase** | 2.95 | Backend complet | C'est la base de donnees, l'authentification et le stockage de fichiers. On en parle en detail dans la section 19. |
| **Leaflet** | 1.9 | Cartes interactives | C'est la bibliotheque qui affiche les cartes avec les marqueurs des sites et equipements. |
| **Recharts** | 2.15 | Graphiques | C'est la bibliotheque qui genere les graphiques dans le module de reporting (barres, lignes, camemberts). |
| **React Query** | 5.83 | Gestion des donnees | C'est la bibliotheque qui gere le chargement des donnees depuis la base de donnees. Elle ajoute un cache (les donnees ne sont pas rechargees a chaque page), et un rafraichissement automatique. |
| **Zod** | 3.25 | Validation des donnees | C'est la bibliotheque qui verifie que les donnees saisies dans les formulaires sont correctes (email valide, champs obligatoires remplis, nombres dans les bonnes plages). |
| **react-hook-form** | 7.61 | Gestion des formulaires | C'est la bibliotheque qui gere les formulaires de saisie (creation d'intervention, ajout de client, etc.). Elle s'occupe de la validation, des erreurs, et de la soumission. |
| **jsPDF** | 4.1 | Generation de PDF | C'est la bibliotheque qui permet de generer des rapports au format PDF directement depuis le navigateur. |
| **signature_pad** | 5.1 | Capture de signature | C'est la bibliotheque qui gere le dessin de la signature client sur l'ecran tactile. |
| **date-fns** | 3.6 | Manipulation de dates | C'est la bibliotheque qui facilite le travail avec les dates (calcul de differences, formatage en francais, etc.). |
| **Lucide React** | 0.462 | Icones | C'est la collection d'icones utilisee partout dans l'application. Toutes les petites icones que vous voyez viennent de la. |
| **browser-image-compression** | 2.0 | Compression d'images | C'est la bibliotheque qui compresse les photos prises par le technicien avant de les envoyer. Ca economise de la bande passante, ce qui est important en RDC ou la connexion peut etre limitee. |

### Pourquoi ces choix ?

Chaque technologie a ete choisie pour une raison :

- **React + TypeScript** : C'est la combinaison la plus populaire dans le monde du developpement web. Ca veut dire qu'il sera facile de trouver des developpeurs pour maintenir l'application.
- **Supabase** : Pas de serveur a gerer. Tout est heberge et maintenu par Supabase. Moins de maintenance pour vous.
- **Tailwind + shadcn/ui** : Un design coherent et professionnel sans avoir besoin d'un designer a plein temps.
- **Vite** : L'application se charge vite, meme sur une connexion lente.

---

## 18.2 Comment ca fonctionne

### L'architecture globale

L'application suit une architecture qu'on appelle "Serverless" (sans serveur). Voici ce que ca veut dire :

```
[Navigateur du technicien]  <-->  [Supabase (cloud)]
                                    |-- Base de donnees PostgreSQL
                                    |-- Authentification
                                    |-- Stockage fichiers

[Navigateur de Clement]     <-->  [Supabase (cloud)]
```

Il n'y a pas de serveur intermediaire. Le navigateur (ou l'application installee) communique directement avec Supabase. C'est comme si chaque utilisateur avait un acces direct a la base de donnees, mais avec des regles de securite qui controlent ce que chacun peut voir et faire.

### Le cycle d'une requete

Quand le technicien ouvre l'onglet Taches, voici ce qui se passe :

1. Le navigateur demande a Supabase : "Donne-moi toutes les interventions"
2. Supabase verifie le jeton d'authentification (est-ce que cette personne est connectee ?)
3. Supabase applique les regles de securite (RLS) : le technicien ne voit que ses propres interventions
4. Supabase renvoie les donnees en format JSON
5. React affiche les donnees a l'ecran
6. React Query met les donnees en cache, pour que la prochaine ouverture soit instantanee

### Le mode hors ligne partiel

L'application utilise IndexedDB (une base de donnees locale dans le navigateur) pour stocker certaines donnees localement. Les photos prises hors ligne sont conservees en local et synchronisees quand la connexion revient.

---

## 18.3 Hebergement

| Service | Fournisseur | Role | Localisation |
|---------|-------------|------|-------------|
| **Frontend** | Vercel | Heberge l'application web | CDN mondial (serveurs partout dans le monde) |
| **Backend** | Supabase | Base de donnees, auth, stockage | Cloud AWS |
| **Domaine** | Vercel | aemi-gmao.vercel.app | Peut etre change pour un domaine personnalise |

### Vercel

Vercel est un service d'hebergement specialise dans les applications web modernes. L'application est distribuee sur un CDN (Content Delivery Network) mondial, ce qui veut dire que peu importe ou l'utilisateur se trouve (Kinshasa, Lubumbashi, ou ailleurs), l'application se charge rapidement parce qu'elle est servie depuis le serveur le plus proche.

### Domaine personnalise

Actuellement, l'application est accessible sur `aemi-gmao.vercel.app`. Si vous souhaitez utiliser un domaine personnalise (par exemple `gmao.aemi.cd`), c'est tout a fait possible. Il suffit de :
1. Acheter le domaine
2. Configurer les DNS vers Vercel
3. Activer le SSL (certificat de securite, gratuit avec Vercel)

L'operation prend environ 30 minutes.

---

## 18.4 Organisation du code

Le code de l'application est organise de facon claire :

```
src/
  components/     --> Les composants reutilisables (boutons, cartes, formulaires)
    layout/       --> La mise en page (sidebar, navigation mobile)
    technician/   --> Les composants specifiques au technicien
    dashboard/    --> Les composants du tableau de bord
    ui/           --> Les composants d'interface de base (shadcn/ui)
  pages/          --> Les pages de l'application
  hooks/          --> Les fonctions utilitaires pour acceder aux donnees
  contexts/       --> Le contexte global (authentification, mode metier)
  types/          --> Les definitions de types TypeScript
  data/           --> Les donnees de demonstration
  lib/            --> Les utilitaires (connexion Supabase, etc.)
  services/       --> Les services (upload photos, etc.)
```

Chaque fichier a une responsabilite claire, ce qui facilite la maintenance.

---

# 19. Supabase - La Base de Donnees

## 19.1 Qu'est-ce que Supabase

Clement, Supabase est le service qui stocke toutes les donnees de l'application. C'est un peu comme le coffre-fort de l'application. Voici ce qu'il faut savoir :

- **C'est une alternative open source a Firebase** (le service de Google). "Open source" veut dire que le code de Supabase est public et gratuit. Si un jour on decide de ne plus utiliser le service cloud de Supabase, on peut installer Supabase sur nos propres serveurs.

- **C'est base sur PostgreSQL**, qui est la base de donnees la plus fiable et la plus utilisee dans le monde professionnel. Les banques, les hopitaux, les grandes entreprises l'utilisent. Vos donnees sont en securite.

- **Ca fournit 4 choses en un seul service** :

| Service | Description |
|---------|-------------|
| **Base de donnees** | Le stockage de toutes les donnees (clients, interventions, equipements...) |
| **Authentification** | La gestion des comptes utilisateurs (inscription, connexion, mots de passe) |
| **Stockage de fichiers** | Le stockage des photos et documents (signatures, fiches d'intervention) |
| **Temps reel** | La possibilite de mettre a jour les donnees en direct sans recharger la page |

- **Des milliers d'entreprises l'utilisent**, des startups aux grandes societes.

- **Le plan gratuit est suffisant pour demarrer**, et on peut augmenter la capacite au fur et a mesure que l'activite grandit.

---

## 19.2 Structure de la Base de Donnees

La base de donnees contient 17 tables principales. Voici chaque table expliquee simplement :

### Table 1 : profiles (Profils utilisateurs)

C'est la table qui stocke les informations sur chaque personne qui utilise l'application.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique, lie au compte d'authentification |
| email | Texte | L'adresse email de connexion |
| full_name | Texte | Le nom complet (ex: Patrick Ilunga) |
| role | Texte | Le role : admin, supervisor, technician, driver, agent_admin |
| phone | Texte | Le numero de telephone |
| avatar_url | Texte | L'URL de la photo de profil (optionnel) |
| skills | Liste | Les competences (ex: ["GE Caterpillar", "Electricite BT"]) |
| is_active | Booleen | Vrai si le compte est actif |
| created_at | Date | Date de creation du compte |
| updated_at | Date | Date de derniere modification |

### Table 2 : clients (Clients)

Les entreprises ou particuliers pour lesquels AEMI intervient.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique |
| name | Texte | Le nom du client (ex: "Brasserie de Kinshasa") |
| type | Texte | "company" ou "individual" |
| address | Texte | L'adresse principale |
| has_portal_access | Booleen | Si le client a acces au portail client |
| contract_file | Texte | L'URL du fichier contrat (optionnel) |
| created_at / updated_at | Date | Dates de creation et modification |

### Table 3 : contacts (Contacts)

Les personnes de contact chez chaque client ou sur chaque site.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique |
| client_id | UUID | Le client associe (optionnel) |
| site_id | UUID | Le site associe (optionnel) |
| name | Texte | Le nom du contact |
| function | Texte | La fonction (ex: "Directeur Technique") |
| phone | Texte | Le numero de telephone |
| email | Texte | L'adresse email (optionnel) |

### Table 4 : sites (Sites)

Les emplacements physiques ou se trouvent les equipements.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique |
| client_id | UUID | Le client proprietaire du site |
| name | Texte | Le nom du site (ex: "Usine Principale Gombe") |
| address | Texte | L'adresse |
| locality | Texte | La localite (ex: "Gombe", "Limete") |
| lat / lng | Nombre | Les coordonnees GPS |
| access_constraints | Texte | Les contraintes d'acces (ex: "Badge obligatoire") |

### Table 5 : assets (Equipements / Groupes Electrogenes)

C'est la table centrale du systeme. Chaque groupe electrogene y est enregistre.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique |
| client_id | UUID | Le client proprietaire |
| site_id | UUID | Le site ou se trouve le groupe |
| client_reference | Texte | La reference du client (ex: "BK-GE-001") |
| name | Texte | Le nom du groupe (ex: "Groupe Electrogene Principal") |
| brand | Texte | La marque (Caterpillar, Perkins, Cummins, etc.) |
| model | Texte | Le modele (C15, 2000 Series, QSX15, etc.) |
| serial_number | Texte | Le numero de serie |
| power | Texte | La puissance (ex: "500 kVA") |
| fuel | Texte | Le type de carburant (diesel, gasoline, gas) |
| tank_volume | Texte | Le volume du reservoir (ex: "1000L") |
| hours_count | Nombre | Le compteur horaire actuel |
| maintenance_threshold | Nombre | Le seuil de maintenance (ex: 250 pour un entretien toutes les 250h) |
| status | Texte | L'etat : operational, breakdown, maintenance_needed, in_intervention, out_of_service |
| components | JSON | La liste des composants (moteur, alternateur, filtres...) |
| lat / lng | Nombre | Les coordonnees GPS de l'equipement |
| last_intervention_date | Date | La date de la derniere intervention |
| next_maintenance_hours | Nombre | Le compteur horaire du prochain entretien |

### Table 6 : interventions (Interventions)

La table la plus importante. Chaque intervention y est enregistree avec toutes ses donnees.

| Colonne | Type | Description |
|---------|------|-------------|
| id | UUID | Identifiant unique |
| client_id / site_id / asset_id | UUID | Le client, le site et l'equipement concernes |
| type | Texte | handling, installation, diagnosis, maintenance, repair |
| maintenance_type | Texte | 250h, 500h, ou 1000h (pour les entretiens) |
| priority | Texte | low, normal, high, urgent |
| status | Texte | created, planned, assigned, en_route, on_site, in_progress, waiting, completed, validated, to_invoice, invoiced |
| billing_status | Texte | not_billed, billed, paid |
| assigned_to | Liste | Les IDs des techniciens assignes |
| scheduled_date / scheduled_time | Date/Texte | La date et l'heure prevues |
| description | Texte | La description du travail a effectuer |
| supervisor_notes | Texte | Les notes du superviseur |
| diagnosis | Texte | Le diagnostic du technicien |
| work_done | Texte | Les travaux realises |
| recommendations | Texte | Les recommandations |
| checklist | JSON | La checklist avec l'etat de chaque item |
| photos_before / photos_during / photos_after | Liste | Les URLs des photos |
| client_signature | Texte | L'URL de la signature |
| travel_start_time / arrival_time | Date | Les horodatages de trajet |
| hours_at_start / hours_at_end | Nombre | Les releves de compteur horaire |
| problems | JSON | Les problemes signales sur le terrain |
| started_at / completed_at / validated_at | Date | Les horodatages de workflow |

### Table 7 : offers (Devis)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| client_id | Le client concerne |
| object | L'objet du devis |
| amount_ht / amount_ttc | Les montants HT et TTC |
| status | pending, rejected, accepted |
| purchase_order_number | Le numero de bon de commande |

### Table 8 : invoices (Factures)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| client_id / intervention_id | Le client et l'intervention concernes |
| object | L'objet de la facture |
| amount_ht / amount_ttc | Les montants |
| status | pending, disputed, paid |

### Table 9 : work_orders (Ordres de Travail Atelier)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| order_number | Le numero d'ordre (ex: OT-2026-001) |
| equipment_type | motor, transformer, alternator, other |
| status | received, diagnosed, waiting_parts, in_repair, quality_check, ready, delivered |
| parts_used | Les pieces utilisees (JSON) |
| labor_hours | Les heures de main d'oeuvre |

### Table 10 : inventory_items (Pieces de rechange)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| sku | Le code article (ex: "FLT-AIR-001") |
| name | Le nom de la piece |
| category | filter, oil, belt, bearing, electrical, mechanical, consumable |
| quantity | La quantite en stock |
| min_stock / max_stock | Les seuils de stock |
| unit_cost | Le cout unitaire |
| location | L'emplacement dans le magasin |
| supplier | Le fournisseur |

### Table 11 : vehicles (Vehicules)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| name | Le nom du vehicule (ex: "Toyota Hilux 1") |
| plate_number | La plaque d'immatriculation |
| brand / model | La marque et le modele |
| mileage | Le kilometrage |
| status | available, in_use, maintenance, out_of_service |
| assigned_driver_id | Le chauffeur assigne |

### Table 12 : teams (Equipes)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| name | Le nom de l'equipe (ex: "Equipe Kinshasa Nord") |
| leader_id | L'ID du chef d'equipe |
| member_ids | Les IDs des membres |

### Table 13 : checklist_templates (Modeles de checklist)

Les checklists reutilisables qui sont associees aux types d'intervention.

### Table 14 : notifications (Alertes)

| Colonne | Description |
|---------|-------------|
| id | Identifiant unique |
| user_id | L'utilisateur concerne |
| title | Le titre de la notification |
| message | Le message |
| type | info, warning, error, success |
| read | Vrai si lue |

### Table 15 : logistics_requests (Demandes logistiques)

Les demandes de pieces, vehicules ou outils pour une intervention.

### Table 16 : vehicle_requests (Demandes de vehicule)

Les reservations de vehicule pour les interventions.

### Table 17 : (implicite) auth.users

C'est la table geree automatiquement par Supabase Auth. Elle stocke les identifiants de connexion (email, mot de passe hashe, etc.).

---

## 19.3 Row Level Security (RLS)

Clement, c'est un concept de securite important. RLS signifie "Row Level Security", ou en francais "Securite au niveau des lignes". Voici ce que ca veut dire :

Imaginez une grande table avec toutes les interventions de l'entreprise. Sans RLS, n'importe qui pourrait voir toutes les interventions. Avec RLS, chaque ligne de la table a une "regle" qui dit : "Cette ligne est visible uniquement par telle personne ou tel role."

### Exemple en pratique

| Utilisateur | Ce qu'il voit |
|-------------|---------------|
| **Clement (admin)** | Toutes les interventions, tous les clients, tous les equipements |
| **Patrick Ilunga (technicien)** | Uniquement les interventions qui lui sont assignees (son ID est dans le champ `assigned_to`) |
| **Jean-Pierre (technicien)** | Uniquement les interventions qui lui sont assignees (differentes de celles de Patrick) |
| **Un utilisateur non connecte** | Rien du tout |

### Comment ca marche techniquement

Chaque table a des "politiques" (policies) qui definissent les regles. Par exemple, pour la table interventions :

- **Politique pour les admins** : "Si le role de l'utilisateur est 'admin' ou 'supervisor', autoriser l'acces a toutes les lignes"
- **Politique pour les techniciens** : "Si le role de l'utilisateur est 'technician', autoriser l'acces uniquement aux lignes ou l'ID de l'utilisateur est dans le champ assigned_to"

Ces regles sont appliquees automatiquement par la base de donnees. Meme si un technicien essayait de modifier l'URL pour acceder a une intervention qui ne lui appartient pas, la base de donnees refuserait de lui montrer les donnees.

C'est une double securite : l'application filtre les donnees dans l'interface, ET la base de donnees filtre les donnees au niveau des requetes.

---

## 19.4 Auto-creation de profil

Quand un nouvel utilisateur s'inscrit dans l'application, voici ce qui se passe :

1. Supabase Auth cree un compte dans la table `auth.users`
2. Un "trigger" (un automatisme) se declenche dans la base de donnees
3. Ce trigger cree automatiquement une ligne dans la table `profiles` avec :
   - L'ID du compte
   - L'email
   - Le nom complet (fourni lors de l'inscription)
   - Le role (fourni lors de l'inscription, par defaut "technician")
4. Le profil est immediatement utilisable

Ce mecanisme assure que chaque utilisateur a toujours un profil correspondant dans la base de donnees. Pas de risque d'avoir un compte sans profil ou un profil sans compte.

---

# 20. Securite

Clement, la securite est une priorite. Vos donnees de maintenance, les informations de vos clients, les rapports des techniciens, tout cela doit etre protege. Voici comment l'application s'en assure.

---

## 20.1 Authentification

L'authentification, c'est le processus qui verifie l'identite de l'utilisateur. En d'autres termes : "Est-ce que cette personne est bien celle qu'elle pretend etre ?"

### Email + mot de passe

L'application utilise le systeme classique d'email et mot de passe. Voici les details :

| Aspect | Detail |
|--------|--------|
| **Hashage du mot de passe** | Le mot de passe n'est jamais stocke en clair. Il est transforme par l'algorithme bcrypt en une chaine illisible. Meme si quelqu'un accedait a la base de donnees, il ne pourrait pas lire les mots de passe. |
| **Jetons JWT** | Apres la connexion, l'utilisateur recoit un "jeton" (JSON Web Token). Ce jeton est comme un badge temporaire qui prouve son identite. Il est envoye avec chaque requete a la base de donnees. |
| **Rafraichissement automatique** | Le jeton expire apres un certain temps (1 heure par defaut). L'application le renouvelle automatiquement en arriere-plan. L'utilisateur n'a pas besoin de se reconnecter. |
| **Stockage securise** | Le jeton est stocke dans les cookies du navigateur, pas dans le localStorage (ce qui est plus securise). |

### Le processus de connexion

1. L'utilisateur saisit son email et son mot de passe
2. L'application envoie ces informations a Supabase Auth (en HTTPS, donc chiffre)
3. Supabase verifie le mot de passe en le comparant au hash stocke
4. Si c'est correct, Supabase genere un jeton JWT et le renvoie
5. L'application stocke le jeton et redirige vers la page appropriee (admin ou technicien)
6. Chaque requete suivante inclut le jeton pour prouver l'identite

---

## 20.2 Autorisation

L'autorisation, c'est ce qui vient apres l'authentification : "Cette personne est bien identifiee, mais qu'a-t-elle le droit de faire ?"

### Les 5 roles

| Role | Code | Acces |
|------|------|-------|
| **Administrateur** | `admin` | Acces complet a toutes les fonctionnalites, tous les modules, toutes les donnees |
| **Superviseur** | `supervisor` | Acces similaire a l'admin, gestion des equipes et des interventions |
| **Technicien** | `technician` | Acces uniquement a la vue mobile : ses missions, son historique, son profil |
| **Chauffeur** | `driver` | Acces aux demandes de vehicule et a la navigation |
| **Agent administratif** | `agent_admin` | Acces aux modules de facturation et de gestion administrative |

### Double securite

La verification des permissions se fait a deux niveaux :

1. **Dans l'application** : L'application verifie le role de l'utilisateur pour afficher les bons menus et les bonnes pages. Un technicien ne voit pas le menu "Facturation". Un admin ne voit pas la vue mobile (sauf s'il le demande explicitement).

2. **Dans la base de donnees** : Les politiques RLS (voir section 19.3) empechent physiquement l'acces aux donnees non autorisees. Meme si quelqu'un modifiait le code de l'application pour contourner les verifications du premier niveau, la base de donnees refuserait l'acces.

C'est comme avoir une porte avec deux serrures differentes. Il faut les deux cles pour entrer.

---

## 20.3 Protection des Donnees

### Chiffrement des communications

| Couche | Protection |
|--------|-----------|
| **En transit** | Toutes les communications entre le navigateur et Supabase passent par HTTPS (TLS 1.3). Les donnees sont chiffrees pendant le transport. |
| **Au repos** | La base de donnees PostgreSQL chiffre les donnees stockees sur le disque. Meme si quelqu'un acced ait aux serveurs physiques, les donnees seraient illisibles. |

### Ce qui n'est PAS dans le code

Certaines informations sensibles ne sont jamais presentes dans le code source de l'application :

- Les mots de passe des utilisateurs
- La cle secrete de Supabase (service_role_key)
- Les certificats SSL

Seule la "cle anonyme" (anon key) de Supabase est utilisee dans l'application. Cette cle permet de se connecter a Supabase mais ne donne aucun acces direct aux donnees. Les donnees ne sont accessibles qu'apres authentification et dans le respect des regles RLS.

### Variables d'environnement

Les cles d'API sont stockees dans des variables d'environnement, pas dans le code. Cela signifie que :
- Sur Vercel, les variables sont configurees dans les parametres du projet
- En developpement, elles sont dans un fichier `.env` qui n'est jamais envoye dans le code source

---

## 20.4 Bonnes pratiques de securite

| Pratique | Implementation |
|----------|---------------|
| **Validation des entrees** | Tous les formulaires utilisent Zod pour valider les donnees avant de les envoyer a la base de donnees. Un email doit etre un email valide, un nombre doit etre un nombre, etc. |
| **Protection contre les injections SQL** | Supabase utilise des requetes parametrees. Le technicien ne peut pas injecter du code SQL malveillant dans un champ de texte. |
| **Protection contre le XSS** | React echappe automatiquement le contenu HTML. Un utilisateur ne peut pas injecter du code JavaScript dans un champ de texte. |
| **Configuration CORS** | L'API Supabase n'accepte les requetes que depuis les domaines autorises (aemi-gmao.vercel.app). |
| **Compression des images** | Les photos sont compressees avant l'envoi, ce qui reduit les risques de surcharge du serveur. |

---

# 21. ExplorIA - L'Agence

## 21.1 Presentation

Clement, dans le menu lateral de l'application, vous avez peut-etre remarque un lien "ExplorIA". Ce lien mene vers la page de presentation de l'agence qui a cree cette application.

ExplorIA est une agence digitale specialisee dans le developpement d'applications web, de produits SaaS (Software as a Service), et de solutions numeriques. L'agence se concentre sur la creation de solutions qui repondent a des besoins reels, avec un souci constant de qualite et de simplicite.

---

## 21.2 La philosophie de design

La page de presentation d'ExplorIA suit un style de design appele "neobrutalism" (neobrutralisme). C'est un choix delibere. Voici ce que ca veut dire :

Le neobrutralisme est un style de design qui se caracterise par :

- **Des bordures nettes et visibles** : Pas de fondus, pas de flou. Les elements sont clairement delimites.
- **Des ombres portees prononcees** : Les elements ont une ombre decalee qui donne un effet "decolle" de la page.
- **Des couleurs vives et franches** : Pas de pastels timides. Des couleurs qui affirment leur presence.
- **Une typographie assumee** : Des textes en gras, lisibles, qui vont droit au but.
- **Une honnete visuelle** : Pas de decorations inutiles. Chaque element a une raison d'etre.

C'est un style qui dit : "On est serieux, on est professionnel, et on n'a pas besoin de fioritures pour le montrer."

La page de l'agence comprend au moins 5 sections detaillees, avec des animations fluides et des micro-interactions (de petits details d'animation qui rendent l'experience agreable). Le design est entierement responsive (adaptatif) et fonctionne aussi bien sur ordinateur que sur telephone.

---

## 21.3 Les services d'ExplorIA

L'agence se specialise dans :

| Service | Description |
|---------|-------------|
| **Applications web** | Des applications comme AEMI GMAO, accessibles depuis un navigateur |
| **Produits SaaS** | Des logiciels en tant que service, heberges dans le cloud |
| **Solutions numeriques** | Des outils sur mesure pour repondre a des besoins specifiques |
| **Design d'interface** | La conception d'interfaces utilisateur intuitives et esthetiques |

---

# 22. Design & Experience Utilisateur

## 22.1 Design System

Clement, le "design system" c'est l'ensemble des regles visuelles qui font que l'application a une apparence coherente d'une page a l'autre. Voici les principes :

### Les composants d'interface

L'application utilise shadcn/ui, qui fournit une bibliotheque de composants pre-concus. Chaque composant (bouton, champ de saisie, tableau, dialogue, menu, etc.) suit les memes regles visuelles :

| Element | Style |
|---------|-------|
| **Coins arrondis** | Tous les elements ont des coins arrondis (rayon de 8 a 16 pixels). Ca donne un aspect moderne et accueillant. |
| **Ombres subtiles** | Les cartes et les dialogues ont une ombre legere qui donne de la profondeur sans etre agressive. |
| **Espacement regulier** | Les espaces entre les elements suivent une grille de 4 pixels (4, 8, 12, 16, 24, 32...). Ca cree un rythme visuel agreable. |
| **Typographie claire** | La police de caracteres est lisible a toutes les tailles. Les titres sont en gras, les textes secondaires sont en gris plus clair. |

### La palette de couleurs

| Couleur | Utilisation |
|---------|-------------|
| **Bleu** | L'action principale (boutons principaux, liens, progression) |
| **Vert** | Le succes, la validation, les elements completes |
| **Ambre/Jaune** | Les avertissements, les elements en attente |
| **Rouge** | Les erreurs, les urgences, les alertes |
| **Gris** | Les textes secondaires, les fonds, les bordures |

Chaque couleur a plusieurs nuances (clair, moyen, fonce) pour s'adapter au contexte.

### Les badges

Les badges sont utilises partout dans l'application pour indiquer des statuts, des priorites et des types :

| Type de badge | Couleurs |
|---------------|----------|
| **Priorite urgente** | Fond rouge clair, texte rouge fonce |
| **Priorite haute** | Fond ambre clair, texte ambre fonce |
| **Priorite normale** | Fond bleu clair, texte bleu fonce |
| **Priorite basse** | Fond gris clair, texte gris |
| **Statut en cours** | Fond ambre, texte ambre |
| **Statut termine** | Fond vert, texte vert |
| **Type reparation** | Fond rose, texte rose |
| **Type entretien** | Fond emeraude, texte emeraude |

---

## 22.2 Mode Sombre

L'application supporte un mode sombre (dark mode). Voici comment ca fonctionne :

### Comment l'activer

Dans l'en-tete de l'application, il y a un bouton avec une icone de soleil ou de lune. Un simple clic bascule entre le mode clair et le mode sombre.

### Ce qui change

| Element | Mode Clair | Mode Sombre |
|---------|-----------|-------------|
| **Fond de page** | Blanc / gris tres clair | Gris tres fonce / noir |
| **Texte principal** | Noir / gris fonce | Blanc / gris clair |
| **Cartes** | Fond blanc, bordure grise | Fond gris fonce, bordure gris moyen |
| **Sidebar** | Fond clair | Fond fonce |
| **Boutons** | Fond bleu, texte blanc | Fond bleu (inchange), texte blanc |
| **Badges** | Couleurs claires | Couleurs adaptees au fond sombre |

### Pourquoi c'est utile

- **Le soir ou dans des environnements sombres** : Le mode sombre est plus agreable pour les yeux quand la lumiere ambiante est faible. Si un technicien travaille dans une salle de machines mal eclairee, le mode sombre evitera que son ecran l'eblouisse.
- **L'economie de batterie** : Sur les ecrans OLED (courants sur les smartphones modernes), le mode sombre consomme moins de batterie parce que les pixels noirs sont eteints.

### Persistance du choix

Le choix du mode (clair ou sombre) est sauvegarde localement dans le navigateur. Si le technicien choisit le mode sombre, il le retrouvera la prochaine fois qu'il ouvre l'application.

---

## 22.3 Responsive Design

L'application s'adapte a toutes les tailles d'ecran. Voici comment :

### Desktop (ordinateur de bureau)

```
+----------+----------------------------------------+
|          |                                        |
| Sidebar  |        Zone de contenu                 |
|          |        (large, avec tableaux,          |
| - Menu   |         cartes, graphiques)            |
| - Menu   |                                        |
| - Menu   |                                        |
|          |                                        |
+----------+----------------------------------------+
```

- La sidebar est toujours visible a gauche
- La zone de contenu est large (environ 80% de l'ecran)
- Les tableaux affichent toutes leurs colonnes
- Les graphiques sont en taille normale

### Tablette

- La sidebar peut etre repliee (bouton hamburger)
- La zone de contenu occupe tout l'ecran quand la sidebar est repliee
- Les tableaux peuvent necessiter un defilement horizontal
- La disposition est globalement similaire au desktop

### Mobile (telephone)

Pour les administrateurs sur telephone :
- La sidebar est remplacee par un menu hamburger
- Le contenu s'adapte a la largeur de l'ecran
- Les tableaux deviennent des listes de cartes
- Les formulaires s'empilent verticalement

Pour les techniciens :
- L'interface est entierement concue pour le mobile (mobile-first)
- Largeur maximale de 448px
- Navigation par onglets en bas de l'ecran
- Boutons et zones tactiles de grande taille

---

## 22.4 Accessibilite

L'application respecte plusieurs principes d'accessibilite :

| Principe | Implementation |
|----------|---------------|
| **Contraste** | Les couleurs de texte et de fond respectent les ratios de contraste recommandes. Le texte noir sur fond blanc, le texte blanc sur fond bleu, etc. |
| **Navigation au clavier** | Tous les elements interactifs (boutons, liens, champs) sont accessibles au clavier avec la touche Tab. La touche Entree active le bouton selectionne. |
| **Lecteurs d'ecran** | Les elements ont des attributs `aria-label` qui decrivent leur fonction. Par exemple, le bouton d'appel a l'attribut "Appeler le client". |
| **Zones tactiles** | Tous les boutons et liens dans la vue mobile font au minimum 44x44 pixels. C'est la taille recommandee par Apple et Google pour eviter les erreurs de toucher. |
| **Texte redimensionnable** | Le texte est defini en unites relatives (rem). Si l'utilisateur augmente la taille du texte dans les parametres de son telephone, l'application s'adapte. |

---

# 23. Donnees de Demonstration

Clement, l'application est livree avec un jeu de donnees de demonstration. Ces donnees representent des scenarios realistes dans le contexte de la RDC et du Katanga. Voici le detail complet.

---

## 23.1 Les Clients (6 clients)

| # | Nom | Type | Adresse | Contacts | Portail |
|---|-----|------|---------|----------|---------|
| 1 | Brasserie de Kinshasa | Entreprise | 123 Boulevard du 30 Juin, Gombe, Kinshasa | Jean-Marie Lumumba (Dir. Technique), Marie Kabila (Resp. Maintenance) | Oui |
| 2 | Ambassade de France | Entreprise | 97 Avenue de la Justice, Gombe, Kinshasa | Pierre Dubois (Attache Technique) | Oui |
| 3 | Hotel du Fleuve | Entreprise | 45 Avenue du Port, Ngaliema, Kinshasa | Patrick Mwamba (Directeur), Cecile Bongo (Maintenance) | Non |
| 4 | Mining Corp International | Entreprise | Zone Industrielle, Lubumbashi | James Wilson (Ops Manager), Albert Kasongo (Maintenance Manager), Sophie Tshilombo (Admin) | Oui |
| 5 | Cimenterie Nationale | Entreprise | Route de Matadi, Bas-Congo | Francois Ngoma (Directeur Usine) | Non |
| 6 | Raffinerie Petroliere | Entreprise | Port de Moanda, Muanda | Charles Mbemba (Chef Maintenance), David Kalonji (Ingenieur) | Oui |

---

## 23.2 Les Sites (8 sites)

| # | Client | Nom du site | Localite | GPS | Contraintes |
|---|--------|-------------|----------|-----|-------------|
| 1 | Brasserie de Kinshasa | Usine Principale Gombe | Gombe | -4.3217, 15.3125 | Badge obligatoire |
| 2 | Brasserie de Kinshasa | Entrepot Limete | Limete | -4.3350, 15.3400 | - |
| 3 | Ambassade de France | Batiment Principal | Gombe | -4.3089, 15.2921 | Controle securite, piece d'identite |
| 4 | Hotel du Fleuve | Hotel du Fleuve | Ngaliema | -4.3156, 15.2678 | - |
| 5 | Mining Corp International | Mine Site Alpha | Lubumbashi | -11.6647, 27.4794 | Zone industrielle, EPI obligatoires |
| 6 | Mining Corp International | Mine Site Beta | Lubumbashi | -11.6800, 27.4900 | - |
| 7 | Cimenterie Nationale | Site Principal | Bas-Congo | -5.8544, 13.0458 | - |
| 8 | Raffinerie Petroliere | Raffinerie Port | Muanda | -5.9311, 12.3497 | Zone SEVESO, formation securite |

---

## 23.3 Les Equipements (11 groupes electrogenes)

| # | Client | Site | Ref. | Marque | Modele | Puissance | Heures | Statut |
|---|--------|------|------|--------|--------|-----------|--------|--------|
| 1 | Brasserie | Gombe | BK-GE-001 | Caterpillar | C15 | 500 kVA | 4750h | Entretien requis |
| 2 | Ambassade | Batiment | AMB-GE-01 | Perkins | 2000 Series | 350 kVA | 2340h | Operationnel |
| 3 | Hotel | Hotel | HDF-001 | Volvo Penta | TAD1345GE | 400 kVA | 3120h | Operationnel |
| 4 | Mining Corp | Alpha | MCI-ALPHA-001 | Caterpillar | C18 | 750 kVA | 5680h | En panne |
| 5 | Brasserie | Gombe | BK-GE-002 | Perkins | 4000 Series | 600 kVA | 1890h | Operationnel |
| 6 | Cimenterie | Principal | CIMNAT-001 | Cummins | QSX15 | 550 kVA | 4200h | Hors service |
| 7 | Raffinerie | Port | RAFPET-001 | MTU | 16V4000 DS | 2000 kVA | 3500h | Operationnel |
| 8 | Mining Corp | Alpha | MCI-ALPHA-002 | Cummins | KTA50 | 1500 kVA | 2800h | Operationnel |
| 9 | Mining Corp | Beta | MCI-BETA-001 | Caterpillar | C32 | 1100 kVA | 4100h | Entretien requis |
| 10 | Mining Corp | Beta | MCI-BETA-002 | Perkins | 4000 Series | 800 kVA | 2100h | Operationnel |
| 11 | Mining Corp | Alpha | MCI-ALPHA-003 | Caterpillar | C9 | 300 kVA | 980h | En intervention |

Les marques representees sont les plus courantes en Afrique centrale : Caterpillar, Perkins, Cummins, Volvo Penta, et MTU. Les puissances vont de 300 kVA a 2000 kVA, couvrant les besoins des petits batiments aux grandes installations industrielles.

---

## 23.4 Le Personnel (8 personnes)

| # | Nom | Role | Competences |
|---|-----|------|-------------|
| 1 | Clement Kabongo | Administrateur | - |
| 2 | Dieudonne Mutombo | Superviseur | GE Caterpillar, GE Perkins, Diagnostic |
| 3 | Michel Kalala | Chauffeur | - |
| 4 | Patrick Ilunga | Technicien | GE Caterpillar, Electricite BT |
| 5 | Jean-Pierre Tshombe | Technicien | GE Perkins, GE Cummins, Mecanique |
| 6 | Francois Lukusa | Technicien | GE Volvo, GE MTU, Installation |
| 7 | Andre Mbala | Chauffeur | - |
| 8 | Marie Nsimba | Agent Administratif | - |

---

## 23.5 Les Equipes (3 equipes)

| # | Nom | Chef | Membres |
|---|-----|------|---------|
| 1 | Equipe Kinshasa Nord | Dieudonne Mutombo | Patrick Ilunga, Jean-Pierre Tshombe |
| 2 | Equipe Kinshasa Sud | Francois Lukusa | Francois Lukusa |
| 3 | Equipe Mobile | Dieudonne Mutombo | Patrick Ilunga, Jean-Pierre Tshombe, Francois Lukusa |

---

## 23.6 Les Interventions

Les donnees de demonstration contiennent 18 interventions avec des statuts varies :

- Des interventions "creees" (en attente de planification)
- Des interventions "planifiees" (date fixee, pas encore assignee)
- Des interventions "assignees" (technicien designe)
- Des interventions "en cours" (technicien sur le terrain)
- Des interventions "terminees" (travail fait, en attente de validation)
- Des interventions "validees" (approuvees par l'admin)
- Des interventions "facturees" (facture envoyee)

Les types couvrent : entretien 250h, entretien 500h, entretien 1000h, reparation, constat, installation, et manutention.

---

## 23.7 Les causes de panne

10 causes de panne sont definies pour le diagramme de Pareto dans le reporting :

1. Surchauffe moteur
2. Defaillance batterie
3. Filtre colmate
4. Fuite carburant
5. Probleme demarreur
6. Alternateur defectueux
7. Courroie usee
8. Capteur defaillant
9. Panne electrique
10. Manque huile

---

## 23.8 Le contexte realiste

Ces donnees ont ete concues pour refleter la realite du terrain en RDC :

- **Les noms** sont des noms congolais typiques (Kabongo, Ilunga, Tshombe, Mutombo...)
- **Les adresses** sont de vraies rues et quartiers de Kinshasa et Lubumbashi
- **Les coordonnees GPS** pointent vers des emplacements reels en RDC
- **Les equipements** utilisent des marques presentes sur le marche congolais
- **Les contraintes d'acces** refletent la realite (zones industrielles, ambassades, sites SEVESO)
- **Les numeros de telephone** utilisent l'indicatif +243 (RDC)

---

# 24. Ce qui est en Production vs Demo

Clement, il est important de faire la distinction entre ce qui fonctionne reellement avec la base de donnees et ce qui est pre-rempli pour la demonstration.

---

## 24.1 En Production (fonctionne avec des donnees reelles)

Voici la liste de tout ce qui fonctionne reellement avec Supabase :

| Fonctionnalite | Detail | Persistance |
|----------------|--------|-------------|
| **Authentification** | Se connecter, se deconnecter, creer un compte | Les sessions persistent entre les visites |
| **Gestion du profil** | Modifier son profil, voir ses informations | Sauvegarde en base de donnees |
| **Creation d'intervention (admin)** | Creer une nouvelle intervention, l'assigner a un technicien | Sauvegarde en base de donnees |
| **Voir les interventions (technicien)** | Le technicien voit les interventions qui lui sont assignees | Lecture depuis la base de donnees |
| **Workflow complet du technicien** | Les 5 etapes (Mission, Trajet, Travail, Photos, Resume) | Chaque etape sauvegarde les donnees en temps reel |
| **Changement de statut** | Le passage de "assigned" a "en_route" a "in_progress" a "completed" | Sauvegarde en base de donnees |
| **Checklist** | Le technicien coche les items, ils sont sauvegardes | JSON sauvegarde dans la colonne checklist |
| **Photos** | Prise de photos et upload vers Supabase Storage | Les URLs sont sauvegardees dans l'intervention |
| **Signature** | Capture de la signature client | Sauvegardee comme image |
| **Toutes les operations CRUD** | Creer, lire, modifier, supprimer sur tous les modules | Sauvegarde en base de donnees |
| **Notifications** | Creation et lecture des notifications | Sauvegarde en base de donnees |

### Ce que "fonctionne avec des donnees reelles" veut dire

Quand vous creez une intervention dans l'application et que vous fermez le navigateur, l'intervention est toujours la quand vous revenez. Elle n'a pas disparu. C'est ca, la persistance des donnees. Tout est stocke dans la base de donnees Supabase, pas dans la memoire du navigateur.

De la meme facon, quand Patrick Ilunga complete une intervention sur son telephone, toutes les donnees (checklist, photos, signature, diagnostic) sont envoyees a la base de donnees. Vous, Clement, pouvez les voir immediatement depuis votre ordinateur.

---

## 24.2 Les donnees de demonstration

Les donnees de demonstration (clients, equipements, interventions pre-remplies) sont incluses dans l'application pour que vous puissiez la tester immediatement sans avoir a tout saisir.

### Comment les reconnaitre

Les donnees demo ont des identifiants qui commencent par des prefixes reconnaissables :
- Clients : `client-1`, `client-2`, etc.
- Sites : `site-1-1`, `site-2-1`, etc.
- Equipements : `asset-1`, `asset-2`, etc.
- Personnel : `staff-1`, `staff-2`, etc.

### Peut-on les remplacer ?

Oui. Quand vous serez pret a utiliser l'application avec vos vraies donnees, il suffira de :

1. Supprimer les donnees de demonstration
2. Saisir vos vrais clients, sites et equipements
3. Creer les comptes de vos vrais techniciens

Ou alors, on peut faire la migration pour vous. C'est une operation qui prend quelques heures.

### Le systeme est pret pour l'utilisation reelle

L'application n'est pas un prototype ou une maquette. C'est un systeme fonctionnel. Les donnees demo sont la uniquement pour illustrer les fonctionnalites. Le jour ou vous remplacez les donnees de Patrick Ilunga par celles de votre vrai technicien, tout fonctionnera exactement de la meme facon.

---

# 25. Prochaines Etapes & Roadmap v2

Clement, l'application que vous avez en main est la version 1. Elle couvre les besoins fondamentaux de la gestion de maintenance. Mais on a deja identifie plusieurs ameliorations pour la version 2. Voici la feuille de route.

---

## 25.1 Ameliorations prevues

### Notifications en temps reel (Push Notifications)

**Quoi :** Envoyer des alertes sur le telephone du technicien quand une nouvelle intervention lui est assignee, ou quand un admin a besoin de son attention.

**Comment :** Utiliser les Web Push Notifications, compatibles avec Android et les navigateurs desktop. Sur iOS, les notifications push sont maintenant supportees pour les applications installees sur l'ecran d'accueil.

**Exemple concret :** Clement cree une intervention urgente et l'assigne a Patrick. Patrick recoit une notification sur son telephone : "Nouvelle intervention urgente - Mining Corp International - Reparation alternateur".

### Upload photos vers Supabase Storage

**Quoi :** Les photos prises par les techniciens seront stockees directement dans Supabase Storage, un service de stockage de fichiers dans le cloud.

**Comment :** Supabase Storage fonctionne comme un disque dur dans le cloud. Les photos sont compressees, envoyees et organisees par intervention.

**Avantage :** Les photos seront accessibles depuis n'importe quel appareil, et ne seront pas perdues si le technicien change de telephone.

### Mode hors-ligne pour les techniciens

**Quoi :** Permettre aux techniciens de travailler meme sans connexion Internet.

**Comment :** Les donnees de l'intervention seront stockees localement dans IndexedDB (une base de donnees dans le navigateur). Quand la connexion revient, les donnees sont automatiquement synchronisees avec le serveur.

**Pourquoi c'est important :** En RDC, la couverture reseau peut etre instable, surtout sur les sites miniers ou dans les zones rurales. Un technicien ne devrait pas etre bloque parce qu'il n'a pas de reseau.

### Application mobile native (React Native)

**Quoi :** Creer une vraie application Android et iOS, disponible sur le Google Play Store et l'App Store.

**Comment :** Utiliser React Native, qui partage une grande partie du code avec l'application web existante.

**Avantages :**
- Notifications push natives
- Acces direct a la camera et au GPS
- Fonctionnement hors-ligne ameliore
- Meilleure performance
- Installation depuis les stores officiels

### Integration SMS pour alertes

**Quoi :** Envoyer des SMS aux techniciens pour les alertes les plus importantes (intervention urgente, annulation, etc.).

**Comment :** Utiliser un service de SMS comme Twilio ou Africa's Talking (qui a une bonne couverture en RDC).

**Pourquoi :** Un SMS fonctionne meme sans connexion Internet, sur n'importe quel telephone, meme les plus basiques.

### Tableau de bord client (Portail Client)

**Quoi :** Donner aux clients un acces pour voir l'etat de leurs equipements et de leurs interventions.

**Comment :** Un espace dedie avec un login specifique. Le client peut voir ses equipements, l'historique des interventions, les rapports, et les factures.

**Avantage :** Les clients n'ont plus besoin d'appeler pour savoir ou en est leur intervention.

### Suivi GPS en temps reel

**Quoi :** Suivre la position des techniciens sur une carte en temps reel.

**Comment :** Le telephone du technicien envoie sa position GPS toutes les 30 secondes a Supabase. L'admin peut voir les techniciens se deplacer sur la carte.

**Utilite :** Savoir quel technicien est le plus proche d'une intervention urgente, ou verifier qu'un technicien est bien arrive sur le site.

### Rapports PDF automatiques

**Quoi :** Generer automatiquement des rapports PDF de fin d'intervention, avec toutes les informations (checklist, photos, signature).

**Comment :** Utiliser jsPDF (deja integre) pour generer le PDF directement depuis l'application.

**Resultat :** Un document professionnel que le technicien peut envoyer au client par email immediatement apres l'intervention.

### Multi-langue

**Quoi :** Supporter plusieurs langues dans l'application.

**Langues prevues :**
- Francais (actuel)
- Lingala (pour les techniciens qui preferent)
- Swahili (pour la region du Katanga)
- Anglais (pour les clients internationaux)

### Integration comptable

**Quoi :** Connecter le module de facturation a un logiciel comptable.

**Comment :** Via une API vers QuickBooks, Sage, ou un logiciel local.

**Avantage :** Les factures creees dans AEMI GMAO se retrouvent automatiquement dans la comptabilite.

---

## 25.2 Priorite proposee

Voici comment on envisage l'ordre de realisation :

| Priorite | Amelioration | Justification |
|----------|-------------|---------------|
| 1 | Upload photos vers Supabase Storage | Indispensable pour la documentation terrain |
| 2 | Mode hors-ligne | Indispensable pour la fiabilite sur le terrain en RDC |
| 3 | Notifications push | Ameliore la reactivite des techniciens |
| 4 | Rapports PDF automatiques | Simplifie le travail administratif |
| 5 | Application mobile native | Meilleure experience utilisateur |
| 6 | Integration SMS | Couverture des techniciens sans smartphone |
| 7 | Portail client | Ameliore la relation client |
| 8 | Suivi GPS temps reel | Optimisation logistique |
| 9 | Multi-langue | Accessibilite regionale |
| 10 | Integration comptable | Automatisation administrative |

Bien sur, cette priorite est une proposition. Votre retour est essentiel pour ajuster.

---

## 25.3 Comment donner votre retour

Clement, votre retour est la chose la plus importante pour la suite du projet. C'est vous qui utilisez l'application au quotidien, c'est vous qui connaissez les besoins de vos equipes et de vos clients.

Voici les domaines ou votre retour serait le plus utile :

### Navigation et facilite d'utilisation

- Est-ce que vous trouvez facilement les informations que vous cherchez ?
- Y a-t-il des pages ou vous etes perdu ?
- Le nombre de clics pour accomplir une tache est-il raisonnable ?
- Les techniciens comprennent-ils facilement comment utiliser l'application ?

### Fonctionnalites manquantes

- Y a-t-il quelque chose que vous faites aujourd'hui (sur papier ou dans un tableur) que l'application ne couvre pas ?
- Quelles informations aimeriez-vous voir sur le tableau de bord ?
- Quels rapports avez-vous besoin de generer ?

### Preferences de design

- Les couleurs sont-elles a votre gout ?
- La taille du texte est-elle confortable ?
- Le mode sombre fonctionne-t-il bien ?
- Les icones sont-elles claires ?

### Ajustements de workflow

- Le processus en 5 etapes du technicien correspond-il a votre facon de travailler ?
- Faut-il ajouter ou supprimer des etapes ?
- Les checklists contiennent-elles les bons points de controle ?
- Le workflow de facturation correspond-il a votre processus ?

### Priorite des futures fonctionnalites

- Parmi les ameliorations listees ci-dessus, lesquelles sont les plus urgentes pour vous ?
- Y a-t-il des fonctionnalites que vous souhaitez et qui ne sont pas dans la liste ?

---

# 26. FAQ - Questions Frequentes

Clement, voici les reponses aux questions qu'on nous pose le plus souvent.

---

**Q1 : Est-ce que mes donnees sont securisees ?**

Oui. Les donnees sont stockees dans une base de donnees PostgreSQL geree par Supabase. Les communications sont chiffrees en HTTPS. Les mots de passe sont hashes avec bcrypt. Les regles RLS empechent les utilisateurs non autorises d'acceder aux donnees. C'est le meme niveau de securite que celui utilise par les banques en ligne.

---

**Q2 : L'application fonctionne-t-elle hors-ligne ?**

Partiellement. L'application peut continuer a fonctionner si la connexion est interrompue brievement grace au cache local. Les photos prises hors-ligne sont conservees localement. Cependant, pour une experience complete, une connexion Internet est necessaire. Le mode hors-ligne complet est prevu dans la version 2.

---

**Q3 : Puis-je ajouter d'autres techniciens ?**

Oui. Depuis la page "Equipes" dans le menu d'administration, vous pouvez ajouter autant de techniciens que necessaire. Chaque technicien aura son propre compte avec son email et son mot de passe. Il n'y a pas de limite au nombre d'utilisateurs.

---

**Q4 : Comment changer mon mot de passe ?**

Actuellement, le changement de mot de passe se fait via la fonctionnalite "Mot de passe oublie" sur la page de connexion. Dans une prochaine version, un bouton de changement de mot de passe sera ajoute dans la page de parametres.

---

**Q5 : L'application est-elle disponible sur Android et iPhone ?**

Oui, mais pas comme une application native (pour l'instant). L'application fonctionne dans le navigateur de n'importe quel smartphone. De plus, les techniciens peuvent l'installer sur leur ecran d'accueil grace a la fonctionnalite PWA (Progressive Web App). Elle se comportera alors comme une application native. Une vraie application native (React Native) est prevue dans la roadmap.

---

**Q6 : Que se passe-t-il si le technicien n'a pas de reseau ?**

Si le technicien perd la connexion en pleine intervention, les donnees qu'il a saisies sont conservees dans la memoire de l'application. Quand la connexion revient, les donnees sont envoyees au serveur. Pour les photos, elles sont compressees et stockees localement. Cependant, on recommande de s'assurer d'avoir une connexion avant de valider l'intervention. Le mode hors-ligne ameliore est en cours de developpement.

---

**Q7 : Puis-je exporter les donnees ?**

Oui. Le module de reporting permet de generer des rapports PDF. De plus, depuis Supabase, les donnees peuvent etre exportees au format CSV ou JSON. Si vous avez besoin d'un format d'export specifique, on peut le mettre en place.

---

**Q8 : Comment fonctionne la maintenance preventive ?**

La maintenance preventive est basee sur le compteur horaire de chaque groupe electrogene. L'application surveille le nombre d'heures et vous alerte quand un seuil est atteint. Par exemple, si un groupe a un seuil de 250 heures et qu'il atteint 4750h, l'application indique qu'un entretien est necessaire a 5000h. Vous pouvez alors creer une intervention de type "Entretien 250h" et l'assigner a un technicien.

---

**Q9 : Qui peut voir quoi dans l'application ?**

| Role | Ce qu'il voit |
|------|---------------|
| Admin | Tout : tous les clients, equipements, interventions, factures, rapports |
| Superviseur | Tout le module de maintenance GE, les equipes |
| Technicien | Uniquement ses propres interventions (assignees, en cours, terminees) |
| Chauffeur | Les demandes de vehicule qui le concernent |
| Agent admin | Les modules de facturation et d'administration |

---

**Q10 : Comment contacter le support ?**

Par email a l'adresse d'ExplorIA. Le temps de reponse vise est de 24 heures en jours ouvrables. Pour les urgences (l'application ne fonctionne plus du tout), contactez directement le numero de telephone fourni.

---

**Q11 : Puis-je modifier les checklists ?**

Oui. Les checklists sont configurables. Si vous avez besoin d'ajouter ou de supprimer des points de controle, ou de creer des checklists specifiques pour certains types de groupes electrogenes, c'est possible. Faites-nous savoir vos besoins.

---

**Q12 : L'application supporte-t-elle plusieurs entites (filiales) ?**

L'application est configuree pour AEMI, mais l'architecture permet de gerer plusieurs entites grace au systeme de "Business Context" (Maintenance GE, Atelier, Logistique). Si vous avez des filiales ou des divisions separees, on peut adapter le systeme.

---

**Q13 : Que se passe-t-il si un technicien quitte l'entreprise ?**

Son compte peut etre desactive dans la page de gestion des equipes. Un compte desactive ne peut plus se connecter, mais l'historique de ses interventions est conserve. Les interventions en cours peuvent etre reassignees a un autre technicien.

---

**Q14 : Les photos prennent-elles beaucoup de place ?**

Non. Les photos sont compressees automatiquement avant d'etre envoyees. Une photo de 5 Mo est reduite a environ 200-500 Ko sans perte visible de qualite. Le plan Supabase gratuit offre 1 Go de stockage, ce qui represente environ 2000 a 5000 photos compressees.

---

**Q15 : Puis-je utiliser l'application sur plusieurs appareils en meme temps ?**

Oui. Clement peut etre connecte sur son ordinateur au bureau pendant que Patrick est connecte sur son telephone sur le terrain. Les donnees sont synchronisees en temps reel. Si Patrick complete une intervention, Clement voit le changement dans les secondes qui suivent.

---

**Q16 : L'application est-elle conforme aux normes ISO ?**

Les checklists d'entretien sont inspirees des bonnes pratiques ISO pour la maintenance des groupes electrogenes. Cependant, une certification ISO formelle necessite un audit independant. Si c'est un besoin, on peut adapter les checklists pour se conformer strictement a une norme specifique (ISO 8528, par exemple).

---

**Q17 : Combien coute l'hebergement ?**

| Service | Cout mensuel |
|---------|-------------|
| Vercel (frontend) | Gratuit (plan hobby) ou ~20$/mois (plan pro) |
| Supabase (backend) | Gratuit (plan free) ou ~25$/mois (plan pro) |
| **Total** | **0$ a 45$/mois** selon le plan choisi |

Le plan gratuit est suffisant pour une utilisation moderee (quelques dizaines d'utilisateurs, quelques milliers d'interventions). Au-dela, les plans payants offrent plus de capacite et de fonctionnalites.

---

**Q18 : Puis-je avoir un nom de domaine personnalise ?**

Oui. Au lieu de `aemi-gmao.vercel.app`, vous pouvez utiliser un domaine comme `gmao.aemi.cd` ou `app.aemi.cd`. Il suffit d'acheter le domaine (environ 10-15$/an) et de le configurer. L'operation prend environ 30 minutes.

---

**Q19 : Que se passe-t-il en cas de bug ?**

Si vous rencontrez un bug, signalez-le a ExplorIA avec le maximum de details :
- Quel ecran etiez-vous en train d'utiliser ?
- Quelle action avez-vous faite ?
- Quel message d'erreur avez-vous vu (si applicable) ?
- Sur quel appareil et quel navigateur etiez-vous ?

L'application inclut un systeme de gestion d'erreurs (Error Boundary) qui attrape les erreurs et affiche un message propre au lieu de planter silencieusement.

---

**Q20 : Mes donnees m'appartiennent-elles ?**

Oui, absolument. Vos donnees sont les votres. Elles sont stockees dans votre base de donnees Supabase, et vous en avez le controle total. Si vous decidez de quitter l'application, vous pouvez exporter toutes vos donnees a tout moment. Rien n'est verrouille.

---

# 27. Contact & Support

Clement, pour toute question, tout retour ou tout signalement de bug, voici comment nous joindre.

---

## 27.1 Pour un retour ou une question

Pour tout ce qui concerne l'application (fonctionnalites, suggestions, ameliorations, questions d'utilisation), contactez l'equipe ExplorIA par email. Decrivez votre demande le plus precisement possible. Plus vous etes precis, plus vite on pourra vous repondre.

## 27.2 Delai de reponse

| Type de demande | Delai vise |
|-----------------|-----------|
| **Bug bloquant** (l'application ne fonctionne plus) | Sous 4 heures en jours ouvrables |
| **Bug non bloquant** (quelque chose ne fonctionne pas correctement) | Sous 24 heures |
| **Question d'utilisation** | Sous 24 heures |
| **Demande de fonctionnalite** | Sous 48 heures pour un premier retour |
| **Demande d'evolution** | Planification conjointe |

## 27.3 Comment signaler un bug

Pour nous aider a comprendre et resoudre un bug rapidement, merci de fournir :

1. **L'ecran concerne** : Sur quelle page etiez-vous ? (par exemple "Page de detail de l'intervention INT-2026-014")
2. **L'action effectuee** : Qu'avez-vous fait exactement ? (par exemple "J'ai clique sur le bouton Valider")
3. **Le resultat attendu** : Que s'attendiez-vous a voir ? (par exemple "L'intervention devrait passer en statut Validee")
4. **Le resultat obtenu** : Que s'est-il passe a la place ? (par exemple "Rien ne s'est passe, le bouton est reste grise")
5. **L'appareil et le navigateur** : Sur quel appareil etes-vous ? Quel navigateur ? (par exemple "iPhone 14, Safari" ou "PC Windows, Chrome")
6. **Une capture d'ecran** : Si possible, prenez une capture d'ecran du probleme

## 27.4 Les mises a jour

Les mises a jour de l'application sont deployees automatiquement. Quand une correction ou une amelioration est prete, elle est publiee sur Vercel et devient disponible immediatement. Vous n'avez rien a faire : il suffit de recharger la page (ou d'ouvrir l'application) pour avoir la derniere version.

Pour les mises a jour importantes, on vous enverra un message pour vous informer des changements.

---

## Mot de la fin

Clement, ce document couvre les aspects techniques et fonctionnels de l'application AEMI GMAO dans leur integralite. L'application est prete a etre utilisee, et l'equipe ExplorIA est disponible pour accompagner la mise en route, former vos equipes, et developper les prochaines fonctionnalites selon vos besoins.

Votre retour est ce qui va rendre cette application encore meilleure. N'hesitez pas a nous contacter pour toute question, suggestion, ou besoin.

---

*Document redige par ExplorIA pour AEMI - Fevrier 2026*
*Application : [https://aemi-gmao.vercel.app](https://aemi-gmao.vercel.app)*
