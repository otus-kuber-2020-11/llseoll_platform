FROM nginx:latest
RUN addgroup --gid 1001 www && adduser --uid 1001 --gid 1001 www --shell /bin/sh
COPY nginx.conf /etc/nginx/nginx.conf
COPY homework.html /app/index.html
EXPOSE 8000
USER 1001
WORKDIR /app
CMD ["nginx", "-g", "daemon off;"]
