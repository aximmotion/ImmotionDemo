# IMMOTION · site web

Site complet de l'agence IMMOTION, assemblé à partir des maquettes du canvas « azadîmmo · identité et site ».
Toutes les pages sont reliées entre elles : menus, boutons, cartes de biens, pied de page, espace client.

## Ouvrir le site sur votre ordinateur

Les pages se chargent par un petit serveur local (un double-clic sur `index.html` ne suffit pas toujours, selon le navigateur).

```
cd immotion-site
python3 -m http.server 8000
```

Puis ouvrir http://localhost:8000 dans le navigateur.

## Mettre le site en ligne avec GitHub Pages

1. Créer un dépôt sur GitHub (par exemple `immotion-site`).
2. Y déposer **le contenu** de ce dossier (pas le dossier lui-même) : bouton « Add file › Upload files », glisser tous les fichiers et le dossier `assets`.
3. Dans le dépôt : Settings › Pages › Source « Deploy from a branch », branche `main`, dossier `/ (root)`, Enregistrer.
4. Après une à deux minutes, le site est en ligne à l'adresse indiquée par GitHub. `404.html` sert automatiquement de page introuvable.

## Organisation

| Dossier ou fichier | Rôle |
|---|---|
| `*.html` | une page du site (liste complète ci-dessous) |
| `assets/img/` | photos et portraits |
| `assets/dc-runtime.js` | moteur qui affiche les pages et leurs interactions (filtres, onglets, formulaires, assistant) |
| `assets/site.js` | centre la page sur les grands écrans et la réduit sur les petits |
| `carte.html` | carte interactive des 100 communes |

## À savoir avant la mise en ligne publique

- Les pages sont conçues pour ordinateur (1440 px). Sur un écran plus petit, elles sont réduites proportionnellement ; une vraie version mobile reste à faire à partir des maquettes « Mobile ».
- Les formulaires (contact, estimation, rendez-vous, newsletter, dossier locataire) mènent aux pages de confirmation mais **n'envoient encore rien** : il faudra les brancher à un service d'envoi.
- L'assistant IMMOTION (bouton rond en bas à droite) affiche une conversation d'exemple ; c'est l'endroit prévu pour brancher vos agents IA.
- Les contenus marqués « Données d'exemple » ou entre crochets (`[délai]`, `[Étude notariale]`…) sont à remplacer par les vrais.
- Les publicités SYNDIKA pointent vers une page Claude privée : remplacez le lien par l'adresse publique de SYNDIKA.

## Liste des pages

| Page | Fichier |
|---|---|
| 01 · Accueil | `index.html` |
| 01 · Connexion | `client-connexion.html` |
| 01 · Home (EN) | `en.html` |
| 01 · Startseite (DE) | `de.html` |
| 02 · Achat · liste des biens | `acheter.html` |
| 02 · Espace vendeur | `client-vendeur.html` |
| 02a · Achat · recherche avancée | `recherche.html` |
| 02b · Achat · les biens sur la carte | `carte-biens.html` |
| 02c · Programmes neufs (VEFA) | `programmes.html` |
| 02d · Fiche d'un programme neuf | `programme.html` |
| 03 · Achat · fiche d'un bien | `bien.html` |
| 03 · Espace acheteur | `client-acheteur.html` |
| 04 · Espace bailleur | `client-bailleur.html` |
| 04 · Location · liste des biens | `louer.html` |
| 04a · Location · recherche détaillée | `recherche-location.html` |
| 05 · Location · fiche d'un bien | `location.html` |
| 05a · Location · dossier locataire (6 étapes) | `dossier-locataire.html` |
| 06 · Estimation | `estimer.html` |
| 06a · Estimation · étape 1, le bien | `estimer-bien.html` |
| 06b · Estimation · étape 3, coordonnées | `estimer-coordonnees.html` |
| 06c · Estimation · résultat | `estimation-resultat.html` |
| 07 · Gestion | `gestion.html` |
| 08 · L'agence et contact | `agence.html` |
| 09 · L'agence · Claire Schmit, fondatrice (vente) | `conseiller-claire.html` |
| 09b · L'agence · Tiago Moreira (achat, off-market) | `conseiller-tiago.html` |
| 09c · L'agence · Matteo Rinaldi (location, gestion) | `conseiller-matteo.html` |
| 09d · L'agence · Jonas Kieffer (neuf, Sud) | `conseiller-jonas.html` |
| 09e · Rendez-vous avec Jonas Kieffer | `rdv-agenda-jonas.html` |
| 09e · Rendez-vous avec Matteo Rinaldi | `rdv-agenda-matteo.html` |
| 09e · Rendez-vous avec Tiago Moreira | `rdv-agenda-tiago.html` |
| 10 · Off-market | `offmarket.html` |
| 10a · Off-market · accès validé | `offmarket-acces.html` |
| 11 · Rendez-vous · choix du conseiller | `rdv-choix.html` |
| 12 · Rendez-vous · agenda | `rdv-agenda.html` |
| 13 · Assistant IMMOTION (conversation) | `assistant.html` |
| Avis clients | `avis.html` |
| Bailleur · dossier d'un candidat | `client-candidat.html` |
| Commune · immobilier à Strassen (modèle des 100 communes) | `commune.html` |
| Confirmation · demande envoyée | `merci-demande.html` |
| Confirmation · inscription newsletter | `merci-newsletter.html` |
| Confirmation · rendez-vous réservé | `merci-rdv.html` |
| Cookies · bannière et préférences | `cookies.html` |
| Favoris, comparateur et alertes | `client-favoris.html` |
| Guide · acheter au Luxembourg | `guide-acheter.html` |
| Guides pratiques | `guides.html` |
| Honoraires et tarifs | `honoraires.html` |
| Mandat de vente ou de gestion · avant signature | `mandat.html` |
| Mentions légales, confidentialité, cookies | `legal.html` |
| Mes documents | `client-documents.html` |
| Mes visites | `client-visites.html` |
| Messages | `client-messages.html` |
| Mon profil | `client-profil.html` |
| Newsletter · page d'inscription | `newsletter.html` |
| Nous rejoindre | `recrutement.html` |
| Page introuvable (404) | `404.html` |
| Questions fréquentes | `faq.html` |
| Vendeur · détail d'une offre | `client-offre.html` |
| Carte des communes | `carte.html` |

## Version de test

Cette version est cachée des moteurs de recherche : chaque page contient `<meta name="robots" content="noindex,nofollow">` et `robots.txt` interdit l'exploration. Avant la mise en ligne publique définitive, retirez cette balise des pages et supprimez `robots.txt`.
