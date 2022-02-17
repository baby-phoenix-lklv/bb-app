# to set venv

```
python3 -m venv venv
source venv/bin/activate
python3 --version
```

# run app locally

```
pip install flask
flask run --host=0.0.0.0
curl localhost:5000
```

# to build image

```
pip freeze | grep Flask > requirements.txt
docker build . --tag louiskimlevu/bb-app:v3
docker images
docker run -p 5000:5000 louiskimlevu/bb-app:v3
curl localhost:5000
```

# to push to registry

```
// Create bb-app repository in Dockerhub
docker tag bb-app louiskimlevu/bb-app:v1
sudo docker login -u louiskimlevu --password-stdin
docker push louiskimlevu/bbphoenix/bb-app:v1
```
