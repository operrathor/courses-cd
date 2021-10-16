# Courses CD

Kubernetes & Argo CD configuration for [courses](https://github.com/operrathor/courses).

## Setup

Create Argo CD application:

```bash
kubectl apply -f application.yaml
```

Generate Basic Auth secret:

```bash
htpasswd -c courses-secret <username>
```

Import Basic Auth secret:

```bash
kubectl create secret generic courses-secret --from-file=courses-secret -n courses
```
