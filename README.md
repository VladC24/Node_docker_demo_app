# Node_docker_kube_demo_app
A small Node app deployed with Docker, Kubernetes and AWS.

Install instructions:
1. Clone the repo
2. Install Docker, npm, minikube and create an AWS account
3. Run `npm install` and `npm run start:dev`.
4. Run `localhost:3000` in the browser. You will see `Hello World!!`
5. Change the `Hello World` text into anything and refresh the page. By adding the `nodemon` dependency, you can simply refresh rather than stop/start the service again.
6. Run `docker build -t <image_name> -f Dockerfile.dev .` for development purposes.
7. Run `docker run docker run --name <container_name> -p 9000:3000 -v $(pwd):/usr/src/app -v /usr/src/app/node_modules <image_name>` to create a new container.
8. Change the text into anything and refresh. This should seamlessly sync with the container.
