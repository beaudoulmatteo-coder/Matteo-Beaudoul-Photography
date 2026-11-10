# Préparation WordPress — Matteo Beaudoul Photography

Ce document décrit comment le site actuel est organisé pour être repris dans WordPress, et ce que tu pourras gérer toi-même ensuite. Rien n'est à faire maintenant : on termine d'abord le design.

## 1. Ce qui est déjà prêt
Le contenu est séparé du design. Tout ce qui devra devenir modifiable depuis WordPress se trouve dans un seul bloc de configuration (en haut de `index.html`) :

| Dans le site aujourd'hui | Équivalent WordPress prévu |
|---|---|
| Une photo (fichier dans `images/<galerie>/`) | Un contenu « Photo » avec son image (médiathèque WordPress) |
| Une galerie (Nature, Paysages…) | Une taxonomie « Galerie » : nom, description, photo de couverture |
| Photo de couverture (`images/covers/`) | Champ « Image de couverture » de la galerie |
| Ajouter une catégorie | Créer une nouvelle « Galerie » dans l'administration |
| Textes d'accueil, À propos, Contact (`content`) | Champs modifiables des pages Accueil, À propos et Contact |
| Photo d'accueil et portrait (`images/hero/`) | Champs image de l'Accueil et de À propos |

Les galeries, les cartes et les pages sont générées automatiquement à partir de cette configuration : le design n'a pas à être refait quand le contenu change.

## 2. Administration privée et visiteurs
- Tu te connectes à l'espace d'administration de WordPress (`/wp-admin`) avec ton compte : c'est là que tu ajoutes ou supprimes des photos, modifies les galeries, choisis les couvertures, crées des catégories et changes les textes.
- Les visiteurs n'ont pas de compte et ne voient que le site publié : ils peuvent le consulter, jamais le modifier. À l'installation, on désactivera l'inscription publique.
- Sécurité à prévoir : mot de passe long et unique, double authentification, limitation des tentatives de connexion, mises à jour régulières, aucun compte inutile.

## 3. Deux façons de procéder (à décider plus tard)
- **A. Thème WordPress sur mesure** (recommandé) : on transforme ce design en thème. Tout se gère dans WordPress, sans code.
- **B. Site actuel + WordPress en coulisses** : plus technique, plus fragile. À éviter sauf besoin précis.

## 4. Avant de créer ton compte
- Un thème sur mesure demande une formule WordPress qui autorise l'envoi de thèmes personnalisés (ou un hébergement WordPress classique). Vérifie les conditions sur wordpress.com/pricing avant de payer.
- Choisis un nom de domaine (ex. matteobeaudoulphotography.be).
- Garde tes photos originales en haute résolution : WordPress crée lui-même les versions allégées.

## 5. Format des données (le « contrat »)
Le futur thème devra fournir la même structure que celle de la configuration actuelle :
`categories[] { slug, title, description, cover, photos[] }` et `content { home, about, contact }`.
