# Alerts

## Updating alerts

Grafana Alerts are provisioned. Run the following command after updating and reconciliating so that they are updated:

```sh
flux reconcile kustomization monitoring-configs --with-source -n flux-system
kubectl -n monitoring rollout restart deployment/kube-prometheus-stack-grafana
kubectl -n monitoring rollout status deployment/kube-prometheus-stack-grafana --timeout=180s
```