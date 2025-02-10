Hallo,<br>
um diese Kubernetes Anwendung zu deployen muss ein Cluster laufen.
Wenn dies der Fall ist führe die folgenden Befehle nacheinander in der Konsole aus:

`kubectl apply -f '.\Kubernetes Manifeste\namespace.yaml'`

`kubectl apply -f '.\Kubernetes Manifeste\web-anwendung.yaml'`

An dieser Stelle kann man einmal prüfen, dass der Server schon gestartet ist:

`kubectl get pod -n mini-projekt`

Danach kann man die Website abrufen (z.B. mit)

`minikube service web-anwendung -n mini-projekt`

Alternative (wenn man nicht Docker Desktop als Container Driver nutzt) sollte es auch möglich sein, den Server unter folgender Adresse abzurufen:

`http://$(node ip):30080`

Die Node IP kann man mit diesem Befehl abrufen:

`kubectl get node -o wide`
