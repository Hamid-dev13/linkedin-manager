# Intent

## Pourquoi ce projet existe

LinkedIn a une interface de publication limitée — pas de vrai planning visuel,
pas d'upload d'image propre via API, pas de preview avant publication.

Ce projet est un espace personnel pour gérer les posts LinkedIn comme un pro :
rédiger, prévisualiser, uploader des images, programmer et publier — tout depuis
une interface web connectée directement à l'API LinkedIn.

## Ce qu'on construit

Un manager de posts LinkedIn personnel. Interface web avec :
- Éditeur de post avec preview en temps réel (rendu tel qu'il apparaîtra sur LinkedIn)
- Upload d'images directement via l'API LinkedIn
- Scheduling — programmer un post à une date/heure précise
- File d'attente des posts programmés avec statut (draft / scheduled / published)
- Historique des posts publiés

## Philosophie

- Open source — conçu pour être réutilisable par n'importe qui
- API LinkedIn officielle — pas de scraping, pas de browser automation
- Simple — une seule page, tout visible d'un coup
- L'agent Hermes reste le point d'entrée Telegram — la web app c'est la visualisation

## Ce qu'on ne construit pas (pour l'instant)

- Multi-compte LinkedIn
- Analytics et statistiques de posts
- Gestion de commentaires
- Génération de contenu IA (Hermes s'en charge côté Telegram)
