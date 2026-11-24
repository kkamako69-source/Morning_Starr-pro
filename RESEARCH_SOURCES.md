# Réservoirs de données et d'innovation — Morning Starr Morgan

Dernière vérification documentaire : 24 novembre 2026.

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
- LRSC : https://huggingface.co/datasets/BantuLanguagesInitiative/LRSC — corpus de parole lue en Lingala, avec audio et transcriptions ; 2 940 énoncés et environ 5,01 heures selon la fiche de données.
- CSRC : https://huggingface.co/datasets/BantuLanguagesInitiative/CSRC — archives radio non annotées en Lingala, Kikongo et Tshiluba ; la fiche affiche 97 779 segments et environ 690,35 heures, sans transcriptions de référence.
- Les deux releases Hugging Face indiquent la licence CC-BY-4.0. Conserver l'attribution aux auteurs du jeu original et à l'équipe de reconditionnement Bantu Languages Initiative.
- Usages possibles : prototype de recherche vocale, transcription et navigation vocale en Lingala. LRSC est le point de départ supervisé le plus simple ; CSRC convient plutôt à la recherche auto-supervisée et à l'adaptation radio, et représente un téléchargement volumineux.
- Ces corpus ne sont pas des réservoirs de punchlines et ne doivent pas être utilisés pour cloner/reproduire la voix d'une personne. Vérifier consentement, provenance et conditions d'utilisation avant toute réutilisation audio.

## 4. Localisation et cartographie

### OpenStreetMap
- Données : https://www.openstreetmap.org/
- Politique de copyright : https://www.openstreetmap.org/copyright
- Licence des données : Open Database License (ODbL).
- Usages : repères géographiques et lieux culturels ou événementiels, lorsque l'adresse et l'existence du lieu sont vérifiées.
- Exigences : crédit visible « © OpenStreetMap contributors » et respect des conditions ODbL. Ne pas aspirer les tuiles de la carte ; utiliser un fournisseur de tuiles conforme à sa politique.
- Ne pas afficher publiquement l'adresse d'un événement privé avant confirmation de l'organisateur.

## 5. Indicateurs publics

### Banque mondiale — World Development Indicators
- Documentation API : https://datahelpdesk.worldbank.org/knowledgebase/articles/889392
- API v2 : https://api.worldbank.org/v2/
- Accès public sans clé API.
- Usages : indicateurs comparables sur la population, l'éducation, l'accès à l'électricité, la santé, la connectivité et l'économie des pays d'Afrique centrale.
- Toujours afficher l'indicateur exact, le pays, l'année, l'unité, la source et la date de récupération. Ne pas présenter une estimation ou une donnée ancienne comme une mesure actuelle.

## 6. Images et médias

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

## 7. Recherche et actualités

- Pour les actualités, utiliser les flux ou APIs des éditeurs avec autorisation ; afficher le titre, la date de publication, la source et un lien, puis paraphraser. Ne pas recopier des articles complets.
- Pour la musique, utiliser les liens officiels des artistes et plateformes ; ne pas extraire des paroles protégées, des enregistrements privés ou des commentaires privés pour construire la base de contenu.
- Pour le projet Smoke Party, les prix et les conditions de billetterie restent ceux confirmés par l'organisateur. Les demandes WhatsApp ne sont pas des billets et le site ne confirme pas de paiement.

## 8. Architecture de collecte recommandée

1. Collecte serveur ou tâche planifiée avec cache, limites de requêtes et respect des conditions d'utilisation.
2. Enregistrer pour chaque item : source, URL d'origine, date de collecte, licence, attribution, langue et date de vérification.
3. Valider et modérer les contenus avant affichage public.
4. Échapper tout texte externe avant injection dans le DOM.
5. Permettre le signalement et le retrait d'un contenu erroné ou dont les droits sont contestés.
6. Afficher la date de mise à jour afin de distinguer un fait vérifié d'une donnée ancienne.

Aucun connecteur ni clé API n'est installé dans le site à ce stade. Les intégrations devront être faites progressivement, après choix des sources, vérification des licences et configuration sécurisée côté serveur.

## 9. Musique : catalogues, données et droits

### MusicBrainz — catalogue de métadonnées musicales
- API : https://musicbrainz.org/doc/MusicBrainz_API
- Utilité : retrouver artistes, groupes, sorties, labels, dates de parution et liens d’identification. MusicBrainz fournit des métadonnées, pas les fichiers audio des morceaux.
- L’accès au web service est gratuit pour un usage non commercial, sans clé API. Chaque application doit fournir un User-Agent parlant et respecter la limite d’une requête par seconde ; les usages commerciaux doivent faire l’objet d’un accord/plan adapté.
- Bon usage : construire des fiches artiste/albums et dédupliquer les références musicales, sans extraire ou héberger des enregistrements protégés.

### MTG-Jamendo — tags musicaux et recherche audio
- Site : https://mtg.github.io/mtg-jamendo-dataset/
- Environ 55 000 pistes avec métadonnées et tags de genre/ambiance ; utile pour tester la recherche musicale et les prototypes de classification.
- Les métadonnées sont sous CC BY-NC-SA 4.0 ; les fichiers audio disposent de licences individuelles et le jeu est destiné à la recherche non commerciale. Toute réutilisation commerciale nécessite une autorisation écrite préalable de Jamendo et la vérification des droits de chaque piste.
- Ne pas intégrer ce corpus aux clips commerciaux, à la publicité ou à des chansons monétisées sans autorisation.

### Free Music Archive — FMA sur Hugging Face
- Dataset : https://huggingface.co/datasets/benjamin-paine/free-music-archive-full
- La version empaquetée annonce 106 199 clips, 8 104 heures et environ 593 GB. Les métadonnées sont CC BY 4.0 ; les fichiers audio ont des licences individuelles variées.
- Trop volumineux pour un prototype avec peu de budget. Sélectionner uniquement des titres dont la licence individuelle autorise clairement le contexte de diffusion prévu et conserver les attributions.

### Métadonnées libres et bases d'inspiration
- MusicBrainz pour les relations artiste/sortie ; Wikidata pour les identifiants et faits structurés CC0 ; OpenAlex pour les publications de recherche (musique, IA, acoustique, culture, langues).
- OpenAlex permet les requêtes simples sans clé. Une clé gratuite augmente le budget quotidien et est nécessaire pour poursuivre la pagination par curseur au-delà de la première page ; appliquer des limites et du backoff en cas de 429.
- Garder séparées les métadonnées musicales, les fichiers audio et les œuvres/lyrics : une licence sur une base de tags ne donne pas les droits sur les enregistrements ou paroles.
## 10. Sources actualisées et limites d’intégration

### OpenAlex — littérature scientifique
- API : https://api.openalex.org/ et guide : https://help.openalex.org/api/
- Rechercher travaux, chercheurs, institutions, thèmes et publications sur acoustique, IA, musique, culture et linguistique.
- Les requêtes simples fonctionnent sans clé. Une clé gratuite augmente le budget quotidien et permet la pagination par curseur ; appliquer les limites de requêtes et un backoff exponentiel en cas de 429.

### MusicBrainz — identité des artistes et sorties
- API : https://musicbrainz.org/doc/MusicBrainz_API
- Données utiles : artistes, groupes, albums, labels, dates, relations et identifiants musicaux. Ce n’est pas un hébergeur audio ni une licence sur les morceaux.
- Usage non commercial gratuit, sans clé, mais chaque client doit fournir un User-Agent explicite et rester à une requête par seconde. L’usage commercial doit être discuté avec MusicBrainz.

### World Bank Open Data — indicateurs de contexte
- API : https://datahelpdesk.worldbank.org/knowledgebase/articles/889392
- Indicateurs comparables sur population, éducation, économie, connectivité, énergie et développement au Congo, en Afrique centrale et dans le monde.
- L’accès aux indicateurs ne nécessite pas de clé API. Conserver la date d’extraction, le code d’indicateur, le pays et l’unité pour chaque graphique.

### Bantu Languages Initiative — corpus vocaux régionaux
- Catalogue : https://bantulanguageinitiative.com/fr/datasets
- LRSC : parole lue en Lingala, annotée avec transcription ; candidat léger pour reconnaissance vocale et tests de transcription.
- CSRC : archives radio non annotées en Lingala, Kikongo et Tshiluba ; plus adaptées à l’adaptation acoustique et à l’apprentissage auto-supervisé qu’à une transcription clé-en-main.
- Le catalogue annonce une licence par défaut CC BY 4.0, mais il faut toujours lire la fiche de chaque release et respecter les conditions de consentement, attribution et redistribution.

### MTG-Jamendo — classification musicale, pas bibliothèque commerciale
- Dataset : https://mtg.github.io/mtg-jamendo-dataset/
- Plus de 55 000 pistes et 195 tags de genre, instrument et humeur ; utile pour prototypes de recherche et d’auto-tagging.
- Le code du dépôt est Apache 2.0, les métadonnées CC BY-NC-SA 4.0 et les fichiers audio ont des licences individuelles. Le dataset est réservé à la recherche non commerciale sauf autorisation écrite de Jamendo : ne pas l’utiliser dans Smoke Party, les clips ou la publicité sans licence commerciale distincte.

### Bases cartographiques et iconographiques
- OpenStreetMap : données sous ODbL ; conserver attribution et vérifier les obligations liées à une base dérivée.
- Wikimedia Commons : vérifier la licence de chaque fichier et respecter l’attribution, la mention des modifications et les éventuelles restrictions.
- Openverse : bon moteur de découverte ; ouvrir la source et vérifier la licence d’origine avant publication.

## 11. Politique commune de données

- Séparer métadonnées, fichiers audio, paroles et contenus utilisateur ; leurs licences et droits ne sont pas interchangeables.
- Enregistrer la source, l’auteur, l’URL d’origine, la date de collecte, la licence, l’attribution, la langue et les éventuelles restrictions.
- Ne pas aspirer les paroles, commentaires privés ou médias personnels pour nourrir les plateformes.
- Utiliser des jeux synthétiques pour les tests et modérer toute contribution publique.
- Mettre les appels API derrière un cache côté serveur lorsqu’un service public est consulté à grande échelle ; gérer limites, erreurs 429/503 et backoff.