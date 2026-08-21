FROM nginx:1.27-alpine

# Remove default nginx site config
RUN rm /etc/nginx/conf.d/default.conf

# Custom config: listen on 3000 instead of nginx's default 80
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy the pre-built static site
COPY dist/ /usr/share/nginx/html/

EXPOSE 3000

CMD ["nginx", "-g", "daemon off;"]
