# install-kubernetes
## Instalar `kubectl`

`kubectl` es un cli para trabajar con kubernetes. Las diferentes instalaciones dependiendo del sistema operativo se encuentran en el siguiente link:

- [Kubectl installation](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

### Ejemplo con macos:

```
$ brew install kubectl
```

## Instalar `Minikube`

Minikube es una suite para probar las bondades de kubernetes localmente. La instalación se encuentra disponible en el siguiente link:

- [Drivers installation](https://kubernetes.io/docs/setup/minikube/#quickstart)

### Ejemplo con macos:

```
$ brew cask install minikube
```

## Instalar `Drivers`
`kubectl` trabaja con varios drivers, dependiendo del que se quiera usar se deben de instalar los drivers. Las instalaciones se encuentran descritas aqui:

- [Drivers installation](https://kubernetes.io/docs/setup/minikube/#quickstart)

### Ejemplo con macos:

```
$ brew install docker-machine-driver-xhyve
$ sudo chown root:wheel /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
$ sudo chmod u+s /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
```

## Uso de `Minikube`

### `start`

Para levantar `minikube` debemos de utilizar el comando `start`. Tambien podemos pasar en un flag el tipo de driver que quisieramos usar.

### Ejemplo en macos

```
$ minikube start --vm-driver=xhyve
```


## Uso de `kubecetl`

### `context`

Para conocer a que instancia de kubernetes estamos conectados podemos usar el siguiente comando:

```
$ kubectl config current-context
```

### `cluster-info`

Vemos la información de nuestro cluster:

```
$ kubectl cluster-info
```

### `get`

Para conocer a que instancia de kubernetes estamos conectados podemos usar el siguiente comando:

```
$ kubectl get nodes/pods/rc
```
Ej:
```
$ kubectl get pods --all-namespaces
```


### `describes`

Para describir de manera de tallada pods, nodes y otros:

```
$ kubectl describe nodes/pods
```


### `dashboard`

Sirve para crear un nuevo :

```
$ kubectl dashboard
```

### `create`

Sirve para crear la `definicion` dentro del cluster de nuestro Pod/Servicio/etc.. :

Comando:

```
$ kubectl create -f FILENAME

```

Ej:

```
$ kubectl create -f mipod.yml
```


### `apply`

Sirve para actualizar la `definicion` dentro del cluster de nuestro Pod/Servicio/RC/etc.. :

Comando:

```
$ kubectl apply -f FILENAME

```

Ej:

```
$ kubectl aply -f mirc.yml
```





