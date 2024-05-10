source ./venv/bin/activate
docker build -t <username>/<repo_name>:0.0.1 .
docker push <username>/<repo_name>:0.0.1
docker run -p 8000:80 <tag_name> (testing image)
cd k8s
kubectl apply -f .
kubectl port-forward <pod_id> 8080:80

CI/CD

brew install jenkins-lts
brew services start jenkins-lts
brew services restart jenkins-lts
brew upgrade jenkins-lts