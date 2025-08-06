## kUBERNETES SELECTORS ##

k8 Selectors : A selector in Kubernetes is a way to find and group resources (like Pods) based on their labels, so other components (like Services or ReplicaSets) can interact with them automatically.

The below are the selectors:

1. Node selector: A node selector is the simplest way to control which node a Pod gets     
                  scheduled on in a Kubernetes cluster. It uses labels on nodes to guide the scheduler.

2. Taints and Tolerations:
   Taints ----> Taint is a way to stop unwanted PODS from running on a Node
   1. prefernoschedule- Requesting scheduler not to schedule the PODS. scheduler still 
                        schedules the PODS
   2. Noschedule - ordering the scheduler not to schedule the PODS
   3. NOEXECUTE - nO SCHEDULE + EVICT THE pods already running on that node

   Toleration ---> Toleartions are a way for PODS to tolerate taints on nodes allowing them
                   to be scheduled onto nodes that would otherwise repel them

3. Node Affinity: It is a way to tell K8, where to place your PODS by matching them to 
                  specific nodes based on labels
    IT comes in two flavours
    1. HARD RULE ---> Must be followed
    2. SOFT RULE ---> Not mandatory

4. Node anti-affinity: It is a rule that tells k8 not to place certain PODS on nodes with 
                       specific labels.

5. POD Affinity : It is a rule that tells k8 to place a POD close to another POD usually 
                  on the same node or in same zone

6. POD Anti-affinity: It is a rule that tells k8 not to place a POD near another POD with
                      specific labels usually on same node
