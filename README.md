# Kubernetes - Modul Basics

## Agenda 

  1. Docker-Grundlagen 
     * [Übersicht Architektur](architektur.md)
     * [Was ist ein Container ?](container.md)
     * [Was sind container images](container-images.md) 
     * [Container vs. Virtuelle Maschine](container-vs-vm.md)
     * [Was ist ein Dockerfile](dockerfile.md) 
     * [Dockerfile - image kleinhalten](dockerfile-image-small.md)

  1. Kubernetes - Überblick
     * [12-Factor-App - Design Prinzipien fuer Cloud Native Anwendungen](12-factor-app.md)
     * [Warum Kubernetes, was macht Kubernetes](warum-kubernetes.md)
     * [Aufbau Allgemein](/kubernetes/architecture.md)
     * [Kubernetes Architektur Deep-Dive](https://github.com/jmetzger/training-kubernetes-advanced/assets/1933318/1ca0d174-f354-43b2-81cc-67af8498b56c)
     * [Wann macht Kubernetes Sinn, wann nicht?](/kubernetes/wann-sinnvoll-wann-nicht.md)   
     * [Welches System ? (minikube, micro8ks etc.)](welches-system.md)

  1. kubectl 
     * [kubectl einrichten mit namespace](/kubectl/kubectl-einrichten.md)
     * [kubectl cheatsheet kubernetes](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

  1. Kubernetes Praxis API-Objekte 
     * [Das Tool kubectl (Devs/Ops) - Spickzettel](/kubectl/spickzettel.md)
     * [kubectl example with run](/kubectl/run-with-example.md)
     * [Bauen einer Applikation mit Resource Objekten](bauen-einer-webanwendung.md)
     * [Anatomie einer Webanwendungen](anatomie-einer-webanwendung.md)
     * [kubectl/manifest/pod](/kubectl-examples/01-pod-nginx.md)
     * ReplicaSets kurz erwähnen (Deployments verwalten sie automatisch)
     * Deployments (Devs/Ops)
     * [kubectl/manifest/deployments](/kubectl-examples/03-nginx-deployment.md)
     * Services (Devs/Ops)
     * [kubectl/manifest/service](/kubectl-examples/03b-service.md)

  1. Kubernetes Ingress
     * [Hintergrund Ingress](/kubernetes/ingress.md)
     * [Install Traefik-IngressController](/ingress/traefik/install-with-helm.md)
     * [Ingress mit traefik](kubectl-examples/04-ingress-traefik-with-hostnames-deployment.md)

  1. Kubernetes Praxis (Stateful Sets)
     * [Hintergrund statefulsets](/kubernetes/statefulsets.md)
     * [Example stateful set](/kubectl-examples/10-statefulset.md)

  1. Kubernetes Storage, ConfigMaps & Secrets
     * [Überblick Persistant Volumes (CSI)](kubernetes-csi/overview.md)
     * [Übung Persistant Storage](kubernetes-csi/nfs-exercise.md)
     * [Credentials in Kubernetes verwenden - welche Moeglichkeiten gibt es?](/kubernetes/secrets/credentials-overview.md)
     * [ConfigMap Example MariaDB](/kubectl-examples/06a-configmap-mariadb.md)
     * [ConfigMap Example nginx.conf](/kubectl-examples/06a-configmap-nginx-conf.md)
     * [Secrets Example MariaDB](/kubectl-examples/07-mariadb-secret.md)

  1. Kubernetes API-Objekte (Teil 2)
     *  [Jobs](kubectl-examples/12-job.md)

  1. Helm (Kubernetes Paketmanager)
     * [Helm - Was kann Helm](helm/was-kann-helm.md)
     * [Helm Grundlagen](/helm/grundlagen.md)
     * [Helm Warum ?](/helm/warum.md)
     * [Helm Example](/helm/example.md)
     * [Installation, Upgrade, Uninstall helm-Chart exercise - simple (mariadb-cloudpirates)](exercises/install/mariadb-cloudpirates.md)
     * [Helm Spickzettel](/helm/spickzettel.md)

  1. Kubernetes Debugging (Troubleshooting)
     * [Netzwerkverbindung zum Pod testen](/tipps-tricks/verbindung-zu-pod-testen.md)
     * [Befehle in pod ausführen - Übung](kubectl-examples/15-exec-example.md)
     * [Welche Pods mit Namen gehören zu einem Service](tipps-tricks/welche-pods-mit-namen-gehoeren-zu-einem-service.md)
     * [Übung: Service-Verbindungsprobleme debuggen mit kubectl debug (ohne NetworkPolicy)](kubectl-examples/21-debug-service.md)
