# docker-compose
```
version: '3.8'
services:

  motd:
    image: nginx:latest
    container_name: motd
    ports:
      - 80:80
    volumes:
      - ./motd/nginx.conf:/etc/nginx/nginx.conf
      - ./motd/html/:/usr/share/nginx/html/
      - ./motd/logs/:/var/log/nginx/
    networks:
      - default
    restart: always

networks:
  default:
    driver: bridge

```
