# Étape de construction
FROM node:20 AS build

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers de package
COPY front/my-app/package.json front/my-app/package-lock.json ./

# Installer les dépendances
RUN npm install

# Copier le code source de l'application
COPY front/my-app ./

# Construire l'application Next.js
RUN npm run build

# Étape d'exécution
FROM node:20

# Définir le répertoire de travail
WORKDIR /app

# Copier le build depuis l'étape précédente
COPY --from=build /app ./

# Exposer le port
EXPOSE 3000

# Lancer l'application
CMD ["npm", "start"]
