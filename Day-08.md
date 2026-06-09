1. Self Introduction  
- Given

2. What happens when “kubectl apply” runs.  
- When kubectl apply runs, kubectl reads the YAML and sends it to the Kubernetes API Server.
The API Server authenticates, authorizes, validates, and stores the object in etcd as the desired state.
Controllers detect the change through reconciliation loops and create/update resources like ReplicaSets and Pods.
The scheduler assigns pods to nodes, kubelets start containers through the container runtime, and status is continuously updated back to the API Server.  

3. How will you trouble shoot the "CrashLoopBackoff".  
- “When troubleshooting CrashLoopBackOff, I first check pod status and restart count using kubectl get pods.
Then I inspect logs using kubectl logs and --previous for crashed containers.
Next I use kubectl describe pod to analyze events, exit codes, probe failures, or OOMKilled errors.
I then verify configs, secrets, dependencies, resource limits, and liveness/readiness probes.
Most issues are usually application crashes, memory limits, or incorrect startup configurations.

4. 

