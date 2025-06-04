User          →  Kube API Server  → etcd
   ↓                   ↓              ↓
Apply CRD        Register endpoints   |
   ↓                   ↓              |
Apply CR           Store CR in etcd ← |
   ↓                   ↓              |
Custom Controller ← Watch CR changes
   ↓
Reconcile logic → Creates Deployments, Services, etc.
