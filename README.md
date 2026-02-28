# SENSAFE 360 📱🛡️

**Backend IA national pour la vérification d’authenticité et la protection numérique au Sénégal.**  
Détection de deepfakes, rumeurs, images IA, arnaques, cyberharcèlement : SENSAFE 360 combine LLMs (Ollama), DeepFace, FastAPI et Docker.  
Idéal pour le hackathon – prêt à brancher sur une app mobile, un web mobile ou une interface citoyenne !

---

## ✨ Fonctionnalités principales

- **Vérification IA de photos, images, vidéos, textes**
- **Détection deepfakes** (visages, expressions…)
- **Détection IA/généré, montage, fake news, arnaques**
- **Synthèse pédagogique multilingue (LLM)**
- **Agrégation d’analyses techniques + explications citoyennes**
- **Déploiement Docker, prêt pour la prod et la démo**

---

## 🏗️ Architecture

- **FastAPI** (Python) – Backend asynchrone, modulable
- **Ollama** – Serveur de LLMs open-source (ex: mistral, llava, deepseek, phi…)
- **DeepFace** – Détection faciale (deepfake, expression, âge/genre…)
- **OpenCV** – Traitement images/vidéos
- **Swagger UI** – Documentation et sandbox test

---

## 🚀 Lancement rapide

### 1. **Prérequis**

- [Docker](https://docs.docker.com/get-docker/)
- Environ 16Go RAM recommandés
- Place disque selon modèles Ollama

### 2. **Cloner et préparer les modèles**

```bash
git clone <url-du-repo>
cd sensafe360-backend
docker compose up --build
# Dans un autre terminal, charger les modèles IA désirés :
docker compose exec ollama ollama pull mistral
docker compose exec ollama ollama pull llava
docker compose exec ollama ollama pull phi
```

### 3. **Accéder à l’API et Swagger**

Ouvre [http://localhost:8000/docs](http://localhost:8000/docs)

- Teste chaque endpoint en live (ex : upload image/jpeg/png…)
- Tu choisis le modèle à chaque requête !

---

## 📖 Endpoints disponibles

Voir le code source (`app/api/endpoints/`) ou lance Swagger pour l’API complète.

---

## 🏆 Hackathon Ready

- Mobile ready, API universelle, analyse real-time
- Fonctionne localement, scalable sur cloud infra sans effort
- Swagger clef en main pour tester devant jury, ONG, citoyens

---

**Démo/présentation :**  
> “L’utilisateur sélectionne l’image/vidéo/message reçu → SENSAFE 360 l’analyse en quelques secondes → verdict citoyen (vrai/faux/suspect), explication simple, recommandations.”

---

**Licence : ©2026 SENSAFE/Octopus - Open innovation**
