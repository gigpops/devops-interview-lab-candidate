# Lab Charts

Charts deployed on the staging cluster.

- `webapp/` - nginx frontend
- `api/`    - backend API
- `worker/` - worker service

## Deployment

```bash
kubectl create namespace lab
for c in webapp api worker; do
  helm upgrade --install "$c" ./"$c" -n lab --wait
done
```

Last review: the previous team confirmed everything deployed without issues.
