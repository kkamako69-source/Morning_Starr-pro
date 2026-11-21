# Morning Starr Morgan — site officiel

Site artistique personnel de **Morning Starr Morgan**.

**Site publié :** https://kkamako69-source.github.io/Morning_Starr-pro/

## Contenu
- `index.html` : page principale avec l’identité artistique, les liens sociaux et des éléments interactifs.
- Le fichier charge la bibliothèque QR Code depuis jsDelivr ; l’accès à cette fonctionnalité dépend donc de la disponibilité de cette ressource externe.

## Modifier le site
1. Vérifie le rendu sur ordinateur et téléphone.
2. Modifie `index.html` en conservant une copie de la version précédente.
3. Contrôle les liens, les textes, les médias et les interactions avant de publier.
4. Après validation, enregistre les changements sur la branche `main`, utilisée par ce dépôt.

## Maintenance recommandée
- Garder les informations de contact et les liens sociaux à jour.
- Ajouter des descriptions accessibles aux images et vérifier le contraste des textes.
- Éviter les scripts ou clés secrètes dans le code public.
- Tester le site après chaque changement pour éviter une régression de la page publiée.

> Ce dépôt contient une page HTML principale ; ce README ne prétend pas qu’un test automatisé ou une vérification complète des navigateurs a déjà été réalisé.

## Contrôle automatique

Le contrôle de structure HTML peut être lancé localement avec :

```sh
python tools/check_site.py
```

GitHub Actions lance aussi ce contrôle à chaque modification de la branche `main` et pour chaque pull request. Les avertissements (par exemple un fragment HTML ou une ressource locale introuvable) doivent être examinés ; un passage réussi ne remplace pas les tests dans un vrai navigateur.

## Événement en vedette

La page d'accueil met en avant [Smoke Party — Nouvelle l'an](smoke-party/), collaboration Morning Starr × Nandiro prévue du 31 décembre 2026 au 1er janvier 2027. Les demandes de pass restent soumises à confirmation par l'organisation et vérification du paiement ; le site ne délivre pas automatiquement un billet.
## Recherche et sources de données
Voir [RESEARCH_SOURCES.md](RESEARCH_SOURCES.md) pour les catalogues OpenAlex, Wikidata, BantuLanguages Initiative, OpenStreetMap, Wikimedia Commons et Openverse, avec leurs licences et conditions de réutilisation.
