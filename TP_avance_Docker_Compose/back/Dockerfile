# Utiliser une image de Node.js
FROM node:20

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers de package
COPY back/package.json back/package-lock.json ./

# Installer les dépendances
RUN npm install

# Copier le code source de l'application
COPY back/ ./

# Exposer le port
EXPOSE 3000

# Lancer l'application
CMD ["node", "index.js"]
