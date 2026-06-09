**************** 27 May ***********

1. Self Intro / Walk me thru your Resume.
2. Can you explain your CICD
3. Since you said, you are using Rollback - What Rollback Mechanism you are having.

    In Jenkins and K8s we primarily use K8s Deployment Rollback using - "kubectl rollout undo", since k8s maintain ReplicaSet Revisions.
    we also keep versioned Docker images, allowing us to redeploy a previous image tag.
    where Helm is used, we leverage Helm release history and "helm rollback".
    Jenkins pipeline perform post-deployment validation using rollout status and health checks, and if validation fails, the pipeline automatically triggers a rollback.
    For critical services, blue-green or canary deployments near-instance rollback by shifting traffic back to the previous version.
    
    # K8s
    => kubectl rollout undo deployment/my-app
    => kubectl rollout undo deployment/my-app --to-revision=3 (Specific version)
    
    # Helm
    => helm history my-app
    => helm rollback my-app 2
    
    # Jenkins pipeline
    => kubectl rollout status deployment/my-app - Write in Try
    => kubectl rollout undo deployment/my-app - write in catch

4. What deployment strategy you are using.
5. 


