# Projets d'automatisation et d'IA avec n8n

Trois projets pratiques réalisés en novembre 2026 pour apprendre l'automatisation de tâches et les agents IA avec **n8n Cloud**. Ce sont des exercices personnels, pas des missions pour des clients.

Auteur : Islam Nasiri, titulaire d'un BTS CIEL (Cybersécurité, Informatique et Réseaux).

## TP1 : inscription automatique
**Workflow :** formulaire → Google Sheets → email de confirmation.
- Un formulaire (nom, email, niveau) enregistre chaque inscription dans une feuille Google Sheets.
- Un email de confirmation personnalisé est envoyé automatiquement.
- Blocs utilisés : Form Trigger, Google Sheets, Gmail.

## TP2 : météo quotidienne
**Workflow :** planification → appel d'API → extraction → email.
- Chaque matin à 7 h, n8n interroge l'API gratuite Open-Meteo pour Rouen.
- Il extrait la température et la vitesse du vent de la réponse JSON, puis envoie le résultat par email.
- Blocs utilisés : Schedule Trigger, HTTP Request, Edit Fields, Gmail.

## TP3 : chatbot FAQ avec agent IA
**Workflow :** message de chat → agent IA avec mémoire.
- Un agent répond aux questions d'une boulangerie fictive (« Le Fournil de Rouen »).
- Un prompt système lui impose de répondre uniquement à partir des informations fournies, sans inventer. Testé avec une question hors sujet : il répond qu'il ne sait pas.
- La mémoire de conversation lui permet de comprendre « Et le lundi ? ».
- Blocs utilisés : Chat Trigger, AI Agent, Simple Memory, OpenAI Chat Model.

## Contenu des dossiers
Chaque dossier contient le workflow exporté (`.json`) et des captures d'écran (workflow, résultat).

## Réutiliser un workflow
Dans n8n : **Workflows → Import from file** et choisir le fichier `.json`. Les connexions (Google, OpenAI) ne sont pas incluses : il faut les recréer avec vos propres identifiants.

## Ce que ces projets m'ont appris
- Relier des services avec des déclencheurs, des API et des expressions.
- Lire et extraire des données JSON.
- Écrire une consigne claire pour limiter les erreurs d'un agent IA et tester ses réponses.

## Suite prévue
Un workflow de tri automatique de demandes clients avec IA, et la reproduction d'un TP avec Make.
