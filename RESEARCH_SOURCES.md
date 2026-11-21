# Réservoirs de données et d'innovation — Morning Starr Morgan

Dernière vérification documentaire : 21 novembre 2026.

Ce document liste des sources publiques pour enrichir les rubriques Découverte & Éducation, Actualités, Innovation et Localisation. Il s'agit de pistes documentées, pas de flux déjà connectés au site.

## 1. Recherche scientifique et innovation

### OpenAlex — publications, chercheurs et institutions
- API : https://api.openalex.org
- Documentation : https://help.openalex.org/api/
- Licence des données : CC0 (selon la documentation OpenAlex).
- Démarrage : recherches simples gratuites sans clé ; une clé gratuite augmente le budget journalier et permet la pagination avancée.
- Usages : présenter des publications ouvertes sur l'IA, la musique, les sciences, l'entrepreneuriat, la culture congolaise et les technologies.
- Limites : OpenAlex indexe des métadonnées scientifiques, pas une vérité universelle ; vérifier le titre, l'année, les auteurs et surtout le lien vers le texte intégral. Les champs venant de sources tierces doivent être échappés avant rendu HTML.

## 2. Connaissances structurées

### Wikidata
- Point d'entrée : https://www.wikidata.org/wiki/Wikidata:Data_access
- SPARQL : https://query.wikidata.org/
- Usages : faits structurés sur les lieux, institutions, artistes, langues, œuvres et dates ; chaque carte doit garder un lien vers la fiche Wikidata et la référence de provenance.
- Licence : les données structurées Wikidata sont publiées sous CC0 ; les médias liés peuvent avoir des licences différentes.
- Limites : les données peuvent être incomplètes, contestées ou modifiées. Vérifier les références avant de publier un fait sensible ou biographique.

## 3. Données linguistiques et patrimoine oral

### BantuLanguages Initiative — corpus congolais
- Catalogue : https://bantulanguageinitiative.com/fr/datasets
- Corpus LRSC : parole lue en Lingala, avec audio et transcription.
- Corpus CSRC : archives radio non annotées en Lingala, Kikongo et Tshiluba.
- Le catalogue indique un défaut de licence CC-BY-4.0 ; vérifier la fiche Hugging Face et la licence de chaque release avant réutilisation.
- Usages possibles : prototype de recherche vocale, transcription, prononciation ou navigation vocale en Lingala. Ce corpus n'est pas un réservoir de punchlines et ne doit pas être utilisé pour entraîner à reproduire les voix des personnes.
- Exigences : conserver attribution, provenance, conditions de consentement et limites du corpus ; ne pas republier l'audio sans vérifier les droits.

## 4. Localisation et cartographie

### OpenStreetMap
- Données : https://www.openstreetmap.org/
- Politique de copyright : https://www.openstreetmap.org/copyright
- Licence des données : Open Database License (ODbL).
- Usages : repères géographiques et lieux culturels ou événementiels, lorsque l'adresse et l'existence du lieu sont vérifiées.
- Exigences : crédit visible « © OpenStreetMap contributors » et respect des conditions ODbL. Ne pas aspirer les tuiles de la carte ; utiliser un fournisseur de tuiles conforme à sa politique.
- Ne pas afficher publiquement l'adresse d'un événement privé avant confirmation de l'organisateur.

## 5. Images et médias

### Wikimedia Commons
- Catalogue : https://commons.wikimedia.org/
- API : https://commons.wikimedia.org/wiki/Commons:API
- Usages : images éducatives, lieux, monuments, instruments et patrimoine.
- Chaque média a sa propre licence. Enregistrer le créateur, la source, la licence, l'URL de la page du fichier et le texte d'attribution avant de l'intégrer.

### Openverse
- Catalogue : https://openverse.org/
- API : https://api.openverse.org/v1/
- Usages : rechercher des médias réutilisables.
- Le filtre de recherche ne remplace pas la vérification de la licence sur la page d'origine. Ne pas utiliser d'images de célébrités ou de personnes privées sans droits/consentement adaptés.

## 6. Recherche et actualités

- Pour les actualités, utiliser les flux ou APIs des éditeurs avec autorisation ; afficher le titre, la date de publication, la source et un lien, puis paraphraser. Ne pas recopier des articles complets.
- Pour la musique, utiliser les liens officiels des artistes et plateformes ; ne pas extraire des paroles protégées, des enregistrements privés ou des commentaires privés pour construire la base de contenu.
- Pour le projet Smoke Party, les prix et les conditions de billetterie restent ceux confirmés par l'organisateur. Les demandes WhatsApp ne sont pas des billets et le site ne confirme pas de paiement.

## 7. Architecture de collecte recommandée

1. Collecte serveur ou tâche planifiée avec cache, limites de requêtes et respect des conditions d'utilisation.
2. Enregistrer pour chaque item : source, URL d'origine, date de collecte, licence, attribution, langue et date de vérification.
3. Valider et modérer les contenus avant affichage public.
4. Échapper tout texte externe avant injection dans le DOM.
5. Permettre le signalement et le retrait d'un contenu erroné ou dont les droits sont contestés.
6. Afficher la date de mise à jour afin de distinguer un fait vérifié d'une donnée ancienne.

Aucun connecteur ni clé API n'est installé dans le site à ce stade. Les intégrations devront être faites progressivement, après choix des sources, vérification des licences et configuration sécurisée côté serveur.
