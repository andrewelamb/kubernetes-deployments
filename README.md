# kubernetes_deployments
Kubernetes deployments on ibc EKS cluster

## Deployment

- Deploying cronjobs on kubernetes: https://v1-21.docs.kubernetes.io/docs/tasks/job/automated-tasks-with-cron-jobs/

    ```
    kubectl get svc
    kubectl create secret generic tyu-syn-pat --from-literal=synapse_auth_token=....
    kubectl create -f projectlive_nf_cronjob.yaml
    kubectl get cronjob projectlive-nf
    kubectl get pods --selector=job-name=projectlive-nf-27164915
    kubectl logs projectlive-nf-27164915-6h75l
    kubectl delete cronjob projectlive-nf
    ```