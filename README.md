# Kubernetes + Node.js - Projeto de Aprendizado

> **Projeto simples para aprender Kubernetes na prática!** 

Este é um projeto que demonstra como **deployar uma aplicação Node.js no Kubernetes** usando Minikube

##  arquitetura do Projeto

```
kube-node-api/
├── 📁 k8s/                    # Configurações Kubernetes
│   ├── deployment.yaml        # Define como rodar a aplicação
│   └── service.yaml          # Expõe a aplicação externamente
├── 📄 Dockerfile             # Como construir a imagem Docker
├── 📄 index.js              # Aplicação Node.js simples
├── 📄 package.json          # Dependências do projeto
```

##  Como Funciona

### 1. **Aplicação Node.js** (`index.js`)
```

### 2. **Containerização** (`Dockerfile`)
```

### 3. **Kubernetes Deployment** (`k8s/deployment.yaml`)
- **2 réplicas** da aplicação para alta disponibilidade
- **Auto-healing**: Se um Pod morrer o outro é criado automaticamente


### 4. **Kubernetes Service** (`k8s/service.yaml`)
- **NodePort** para expor a aplicação externamente
- **Porta 30080** para acesso de fora do cluster
- **Distribui tráfego** entre os Pods automaticamente

##  Pré-requisitos

Antes de começar, você precisa ter instalado:

- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## conceitos Kubernetes Aprendidos

### **Pod**
- Contém um ou mais containers
- É efêmero (pode ser recriado a qualquer momento)

### **Deployment**
- Gerencia Pods automaticamente
- Garante que sempre tenhamos o número de réplicas especificado

### **Service**
- Expõe Pods

### **Minikube**
- Kubernetes local para desenvolvimento
- Simula um cluster no pc

## o que acontece por baixo dos panos?

1. **Minikube** cria um cluster Kubernetes virtual
2. **Docker** constrói a imagem da aplicação
3. **Kubernetes** cria 2 Pods com a aplicação
4. **Service** expoe os Pods na porta 30080
5. **Load balancer** distribui tráfego entre os Pods


**feito com ❤️ para aprender Kubernetes!** 
# k8s
