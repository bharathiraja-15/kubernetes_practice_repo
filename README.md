# kubernetes_practice_repo
Perfect 👍
You already learned **Git like real DevOps engineer practice**, now we will do **Kubernetes → REAL 5 Years Experience Level Training**.

I will train you **not theory learner → Production DevOps Engineer**.

✅ Step-by-step
✅ Real company scenarios
✅ Interview + Hands-on
✅ Production mindset
✅ Daily practice labs

---

# 🚀 Kubernetes MASTER ROADMAP (0 → 5 Years Experience)

## 🔥 PHASE 1 — Kubernetes Foundation (VERY STRONG BASE)

👉 Goal: Understand **how Kubernetes actually works internally**

### ✅ Step 1: Container → Pod Concept

First understand:

* Docker Container problem
* Why Kubernetes needed
* Cluster architecture

### Learn:

* Node
* Master Node
* Worker Node
* Pod
* Container Runtime

---

## 🧠 Kubernetes Architecture (Must Visualize)

![Image](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg)

![Image](https://kubernetes.io/images/docs/components-of-kubernetes.svg)

![Image](https://miro.medium.com/1%2AQWJijlj7kwd0hIYk8Wsnow.png)

![Image](https://www.plural.sh/blog/content/images/2025/02/image.png)

### Master Node Components

You MUST know like interview expert:

✅ API Server
✅ ETCD
✅ Scheduler
✅ Controller Manager

### Worker Node

✅ Kubelet
✅ Kube-proxy
✅ Container Runtime

---

## 🧪 STEP 2 — Setup Your OWN Cluster (MANDATORY)

Real DevOps NEVER learn only theory.

### Install locally:

👉 Choose ONE:

✅ Minikube (Beginner)
✅ Kind
✅ K3s
✅ AWS EKS (Later)

### Practice:

```bash
minikube start
kubectl get nodes
kubectl cluster-info
```

---

## 🔥 STEP 3 — POD MASTER LEVEL

Pod = Heart of Kubernetes

Create first pod:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx
    image: nginx
```

Apply:

```bash
kubectl apply -f pod.yaml
```

Check:

```bash
kubectl get pods
kubectl describe pod nginx-pod
kubectl logs nginx-pod
```

✅ Practice until NO GOOGLE needed.

---

## 🔥 STEP 4 — Deployment (REAL COMPANY USE)

Nobody runs Pods directly in production.

Use **Deployment**.

![Image](https://www.researchgate.net/publication/371543145/figure/fig2/AS%3A11431281415825806%401746050153374/Hierarchical-structure-of-Deployment-ReplicaSet-and-Pod-adapted-from-official.tif)

![Image](https://kubernetes.io/images/docs/components-of-kubernetes.svg)

![Image](https://kubernetes.io/docs/tutorials/kubernetes-basics/public/images/module_06_rollingupdates2.svg)

![Image](https://miro.medium.com/1%2AV3grVwrlokIKTH2rvoY-lg.png)

### Deployment YAML

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: web-deploy
spec:
  replicas: 3
  selector:
    matchLabels:
      app: web
  template:
    metadata:
      labels:
        app: web
    spec:
      containers:
      - name: nginx
        image: nginx
```

Practice:

```bash
kubectl scale deployment web-deploy --replicas=5
kubectl rollout status deployment web-deploy
kubectl rollout undo deployment web-deploy
```

🔥 Interview Question:

> Production failed → rollback how?

You must answer instantly.

---

## 🔥 STEP 5 — Services (NETWORKING KING)

Pods change IP always.

Service gives **stable access**.

![Image](https://assets.bytebytego.com/diagrams/0005-4-k8s-service-types.png)

![Image](https://opensource.com/sites/default/files/2022-05/1containerandpodnets.jpg)

![Image](https://kubebyexample.com/sites/default/files/2021-06/service-redirect-static.svg_.png)

![Image](https://i.sstatic.net/Cwd7c.png)

Types:

✅ ClusterIP
✅ NodePort
✅ LoadBalancer

Example:

```yaml
kind: Service
apiVersion: v1
metadata:
  name: web-service
spec:
  type: NodePort
  selector:
    app: web
  ports:
  - port: 80
    targetPort: 80
```

---

## 🔥 STEP 6 — CONFIGMAP + SECRET (REAL TIME)

Production apps need:

* DB password
* API key
* Config values

DevOps responsibility ⭐

```bash
kubectl create configmap app-config --from-literal=env=prod
kubectl create secret generic db-secret \
--from-literal=password=admin123
```

---

## 🔥 STEP 7 — Ingress (PRODUCTION ENTRY)

Company traffic flow:

```
Internet
   ↓
Ingress
   ↓
Service
   ↓
Pods
```

This is **REAL production routing**.

---

## 🔥 STEP 8 — Storage (VERY IMPORTANT)

Know difference:

✅ emptyDir
✅ Persistent Volume
✅ Persistent Volume Claim
✅ StorageClass

Interview favorite topic.

---

## 🔥 STEP 9 — Production Scaling

You MUST practice:

```bash
kubectl autoscale deployment web-deploy \
--cpu-percent=50 --min=2 --max=10
```

Concept:
✅ HPA
✅ Auto Healing
✅ Self Recovery

---

## 🔥 STEP 10 — DevOps REAL RESPONSIBILITY

Daily DevOps Kubernetes Tasks:

✅ Deploy application
✅ Debug CrashLoopBackOff
✅ Check logs
✅ Resource tuning
✅ Upgrade cluster
✅ Secret rotation
✅ Monitoring
✅ Incident handling

---

# 🧪 REAL EXPERIENCE LAB PLAN (IMPORTANT)

## Week 1

✅ Cluster setup
✅ Pods
✅ kubectl mastery

## Week 2

✅ Deployment
✅ Scaling
✅ Rollback

## Week 3

✅ Services
✅ Networking
✅ DNS

## Week 4

✅ Ingress
✅ ConfigMap
✅ Secrets

## Week 5

✅ Storage
✅ Stateful apps

## Week 6

✅ Production simulation

---

# 🔥 FINAL TARGET (5-Year Engineer Skills)

If you can do WITHOUT GOOGLE:

✅ Debug pod failure
✅ Fix networking issue
✅ Rollback production
✅ Scale automatically
✅ Deploy using YAML
✅ Expose app globally
✅ Handle node failure
✅ Read events/logs fast

👉 Then you are **real Kubernetes DevOps Engineer**.

---

## 🚀 NEXT STEP (Tomorrow Lab Style)

Next I will give you:

✅ **Kubernetes REAL COMPANY ENVIRONMENT SETUP**

* Dev
* QA
* Stage
* Prod
* Namespace strategy
* Branch → Environment mapping

⚡ Same like Git real-company lab.

---

Before moving next tell me:

👉 Are you using **Laptop Ubuntu / Windows / AWS EC2** for practice?

I will give exact setup based on your system.
