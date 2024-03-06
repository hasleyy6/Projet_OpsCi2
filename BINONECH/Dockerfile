# Utiliser une image node officielle comme base
FROM node:18

# Définir le répertoire de travail dans le conteneur
WORKDIR /usr/src/app

# Copier les fichiers de configuration du projet dans le conteneur
COPY package.json ./
COPY yarn.lock ./

# Installer les dépendances de Strapi (peut inclure strapi-plugin)
RUN yarn install

# Copier le reste des fichiers du projet dans le conteneur
COPY . .

# Construire le projet Strapi (peut être omis si le projet a été construit localement)
RUN yarn build

# Exposer le port sur lequel Strapi va s'exécuter
#EXPOSE 1337

# Lancer Strapi
CMD ["yarn", "develop"]
