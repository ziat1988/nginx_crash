### Pratice Nginx as Proxy Server

1. How to use

- From root project, cd docker, run `docker compose up -d`
- On browser, `localhost:8080`
- Remove container node, one by one, `docker rm -f <container-name>` app will still run. (until run out all 3 node server)

2. Explain

- Nginx act as a reserve proxy / load balancing, it distributes incoming traffic across 3 node back end.
- Distingues with nginx as Web server in a php app, in nodejs app, we don't need a specific web server, we already have built-in webserver so Nginx here is a reverse proxy.
- The only config custom is in docker/nginx/config/proxy.conf. All others config default of nginx is keep as it is.

3. Credit

- From Nana courses https://www.youtube.com/watch?v=q8OleYuqntY&t=3159s
- But instead have nginx install direct on machine, here we have both on docker.
