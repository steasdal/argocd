# ArgoCD Deployment - Self Managed

This repo contains a kustomized deployment for self-managed ArgoCD.  The deployment requires a bit of bootstrap trickery like so:

   * Clone this repo locally
   * Deploy via good ol' `kubectl`:

```bash
kubectl apply -f deploy
```

   * Login to ArgoCD UI
   * Create an ArgoCD app called "ArgoCD" but use this repo's GitHub URL and the `deploy` directory.

The ArgoCD app should _override_ the existing config that was deployed via kubectl.