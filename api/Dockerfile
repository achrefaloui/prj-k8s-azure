# Utiliser une image Node.js légère
FROM node:18-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier package.json pour installer les dépendances (profite du cache Docker)
COPY package*.json ./
RUN npm install

# Copier le reste du code de l'application
COPY . .

# Exposer le port sur lequel l'API écoute
EXPOSE 3000

# Commande pour démarrer l'application
CMD [ "node", "server.js" ]