# LinkedIn Manager

Interface web personnelle pour gérer, programmer et publier des posts LinkedIn via l'API officielle.

## Fonctionnalités

- **Éditeur** — rédige ton post avec preview temps réel
- **Images** — upload direct via LinkedIn Images API
- **Scheduling** — programme tes posts à l'heure exacte
- **File d'attente** — visualise tous tes posts (draft / schedulé / publié)
- **Historique** — retrouve tous tes posts publiés

## Stack

- **Frontend** : Next.js 14 + TypeScript + Tailwind
- **Backend** : API routes Next.js
- **Auth** : Token OAuth LinkedIn (géré par Hermes)
- **Scheduling** : Cronjobs Hermes
- **API** : LinkedIn REST API v2

## Structure

```
linkedin-manager/
├── intent.md              # Pourquoi ce projet existe
├── spec.md                # Ce qui doit être construit
├── architecture.md        # Comment c'est conçu
├── plan.md                # Ordre d'implémentation
├── CLAUDE.md              # Conventions pour les agents
├── app/
│   ├── page.tsx           # Dashboard principal
│   ├── api/
│   │   ├── posts/         # CRUD posts
│   │   ├── upload/        # Upload image LinkedIn
│   │   └── schedule/      # Gestion du scheduling
│   └── components/
│       ├── PostEditor.tsx  # Éditeur + preview
│       ├── PostQueue.tsx   # File d'attente
│       └── ImageUpload.tsx # Upload d'images
├── lib/
│   ├── linkedin.ts        # Client API LinkedIn
│   └── types.ts           # Types TypeScript
└── data/
    └── posts.json         # Posts locaux (draft/scheduled)
```

## Setup

```bash
# Variables d'environnement
LINKEDIN_ACCESS_TOKEN=your_token
LINKEDIN_PERSON_URN=urn:li:person:your_id

# Lancer en dev
npm install
npm run dev
```

## Lien avec Hermes

Hermes (agent Telegram) peut interagir avec ce manager :
- Envoyer un post à publier → il apparaît dans la file d'attente
- Déclencher une publication schedulée
- Notifier quand un post est publié

---

*Projet personnel — Hamid Bennacef*
