# RSVP with kubertnet

We will be using a sample RSVP application. Using this application, users can register for an event by providing their username and email ID.
Once a user registers, his/her name and email appears in a table.
The application consists of a backend database and a frontend. For the backend, we will be using a MongoDB database, and for the frontend, we have a Python Flask-based application.

## Instalación

(As prerequisites we have to have minikube installed on our machine)

First we have to clone the repository.

```bash
# Clonar el repositorio
git clone https://github.com/StevenZ-G/RSVP.git
```

After cloning the repository, it is time to run the following commands to create our app.

```bash
kubectl create -f rsvp-db.yml
kubectl create -f rsvp-db-service.yml
kubectl create -f rsvp-web.yml
kubectl create -f rsvp-web-service.yml
```
Now we verify that the Deployments and Services have been created properly

```bash
kubectl get deployments
kubectl get services
```

Now we proceed to open our app

```bash
minicube services rsvp
```


