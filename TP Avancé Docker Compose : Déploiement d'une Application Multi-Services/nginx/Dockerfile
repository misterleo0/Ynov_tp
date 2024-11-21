# Utiliser l'image officielle de Nginx
FROM nginx:alpine

# Copier la configuration Nginx personnalisée
COPY nginx/nginx.conf /etc/nginx/nginx.conf
COPY nginx/conf.d /etc/nginx/conf.d
# Exposer le port 80 pour le reverse proxy
EXPOSE 80
