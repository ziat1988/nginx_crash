### Pratice Nginx as Proxy Server

#### 1. How to use

- From root project, cd docker, run `docker compose up -d`
- On browser, `localhost:8080`
- Remove container node, one by one, `docker rm -f <container-name>` app will still run. (until run out all 3 node server)

#### 2. Explain

- Nginx act as a reserve proxy / load balancing, it distributes incoming traffic across 3 node back end.
- In a PHP application, Nginx is typically used as a web server. However, in a Node.js application, a specific web server like Nginx is not required because Node.js comes with a built-in web server. Instead, Nginx is often used as a reverse proxy in such cases.
- The only config custom is in docker/nginx/config/proxy.conf. All others config default of nginx is keep as it is.
- This docker setup is likely in production mode, in dev mode, we should use volume.

#### 3. Credit

- From Nana courses https://www.youtube.com/watch?v=q8OleYuqntY&t=3159s
- But instead have nginx install direct on machine, here we have both on docker.
