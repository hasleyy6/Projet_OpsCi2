# Utiliser l'image officielle de Node.js comme image de base
FROM node:18

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers `package.json` et `package-lock.json` (ou `yarn.lock`)
COPY package*.json ./
COPY yarn.lock ./

# Installer les dépendances du projet
RUN npm install

# Copier les fichiers et dossiers du projet dans le répertoire de travail (/app)
COPY . .

# Construire l'application pour la production
RUN npm run build

ENV PORT=5173

# Installer serve pour servir l'application sur le port 3000
CMD ["npm", "run", "dev"]

