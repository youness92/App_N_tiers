# Utilisez une image Nginx pour servir le contenu statique
FROM nginx:alpine

# Copiez votre code frontend (html, js, css, etc.) vers /usr/share/nginx/html
COPY html/ /usr/share/nginx/html/

# Utilisez votre fichier de configuration Nginx
COPY nginx.conf /etc/nginx/conf.d/default.conf
