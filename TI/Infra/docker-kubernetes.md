---
markmap:
  initialExpandLevel: 2
---

# 🐳☸️ **Docker e Kubernetes – IaC**

## 🐳 **Docker – Conceito**
- Plataforma para **containerização** de aplicações
- Empacota **aplicação + dependências** em ambiente isolado
- Baseada no kernel do sistema operacional
- Usa o conceito de ==containers== para **isolamento leve**

## 🧱 **Componentes do Docker**

### **Docker Engine**
- **Motor principal do Docker**
- ==Serve para criar e Executar containers==
- 3 partes:
  - `dockerd` (daemon)
  - API REST
  - Cliente CLI (`docker`)

### **Imagem (Image)**
- 📎 Snapshot com aplicação e dependências
- Criada a partir de um `Dockerfile`

### **Container**
- 📎 Instância **em execução** da imagem
- Imagem = somente leitura  
- Container = camada de ==gravação==

### **Dockerfile**
- 📎 Script com instruções para gerar imagem
- ==Cada comando gera uma camada==

**Instruções comuns:**
- `FROM` – imagem base  
- `RUN` – comandos a executar  
- `COPY` / `ADD` – copiar arquivos  
- `EXPOSE` – portas abertas  
- `CMD` / `ENTRYPOINT` – comando principal

- **Exemplo:**
  ```
  FROM ubuntu  
  RUN apt-get install -y nginx  
  CMD ["nginx", "-g", "daemon off;"]
  ```

### **Docker Hub**
- 📎 Registro público de imagens (ex: nginx, mysql)

### **Docker Registry**
- 📎 Sistema de armazenamento de imagens  
- Pode ser **público ou privado**

### **Volume**
- 📎 Armazena dados persistentes fora do container

### **Network**
- 📎 Permite comunicação entre containers

---

## ⚙️ **Principais comandos Docker**

- `docker build` → cria imagem a partir do Dockerfile  
- `docker run` → executa container  
- `docker ps` → lista containers  
- `docker exec` → executa comando no container  
- `docker stop` / `docker rm` → para e remove container

---

## 🧩 **Docker Compose**
- 📎 Orquestra múltiplos containers com YAML  
- Ideal para ambientes com **app + banco**
- **Exemplo:**
    ```
    version: "3"  
    services:  
      web:  
        image: nginx  
        ports:  
          - "80:80"  
      db:  
        image: mysql  
        environment:  
          MYSQL_ROOT_PASSWORD: senha
    ```
    ---

## ☸️ **Kubernetes – Conceito**
- Plataforma de **orquestração de containers**
- Automatiza: ==Deploy, escalonamento, rede e atualização==
- Criado pela **Google**

## 🧱 **Componentes do Kubernetes**

### **Cluster**
- 📎 Conjunto de máquinas (nós)

### **Node**
- 📎 Cada máquina (física/virtual)
- Pode ser:
  - **Master**
  - **Worker**

### **Pod**
- 📎 Menor unidade executável
- Pode conter múltiplos containers

### **ReplicaSet**
- 📎 Garante número desejado de pods

### **Deployment**
- 📎 Controla rollout e rollback de versões

### **Service**
- 📎 Cria ponto de acesso estável
- Tipos: `ClusterIP`, `NodePort`, `LoadBalancer`

### **Namespace**
- 📎 Agrupamento lógico de recursos

### **ConfigMap e Secret**
- 📎 Configurações externas
- `Secret` = criptografado

---

## ⚙️ **Comandos kubectl**

- `kubectl get pods`  
- `kubectl get services`  
- `kubectl describe pod`  
- `kubectl apply -f app.yaml`  
- `kubectl delete pod nome`

---

## 📁 **YAML – Definição no Kubernetes**
```
apiVersion: v1  
kind: Pod  
metadata:  
  name: nginx  
spec:  
  containers:  
    - name: nginx  
      image: nginx
```
---

## 🧭 **==Fluxo de Execução no Kubernetes==**
-  1️⃣ **Usuário aplica manifesto YAML**  
  2️⃣ **API Server** recebe requisição  
  3️⃣ **Scheduler** decide o nó  
  4️⃣ **Kubelet** instala pod no nó  
  5️⃣ **Kube Proxy** gerencia a rede

---

## ⚠️ **🔥 Bizus de Prova**

- ✅ Docker = **"E"mpacotar e "E"xecutar**
- ✅ Kubernetes = **orquestrar e gerenciar**
- ✅ Pod = **menor unidade do K8s**
- ✅ Deployment = **controla atualizações**
- ✅ Volume ≠ persistência nativa no container
- ✅ Container ≠ VM → **compartilha kernel**
- ✅ Dockerfile = instruções | Imagem = resultado
- ✅ ReplicaSet ≠ réplica de container (é de pod)
- ✅ Compose = orquestração local
- ✅ Registry ≠ Hub: Registry = sistema | Hub = repositório

---

## 🧠 **Palavras-chave finais**
- ➡️ **Docker**: container, Dockerfile, image, volume, run, hub  
➡️ **Kubernetes**: cluster, pod, service, deployment, ReplicaSet  
➡️ **YAML**: definição como código  
➡️ Orquestração = Kubernetes | Execução = Docker  
➡️ Secrets = dados sensíveis | ConfigMap = configs externas
