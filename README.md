# armada-demo
Demoing Armada

## Queue Creation via Armadactrl

`armadactl` can be either installed or run from the repo directly.

a) Delete queues:
    `go run ./cmd/armadactl/main.go --armadaUrl armada.demo.armadaproject.io:443 delete queue queue-a`

b) Create queues from a file:
    `go run ./cmd/armadactl/main.go --armadaUrl armada.demo.armadaproject.io:443 create -f docs/quickstart/queue-a.yaml`

c) Submit a job:
    `go run ./cmd/armadactl/main.go --armadaUrl armada.demo.armadaproject.io:443 submit docs/quickstart/job-queue-a.yaml`

d) Describe queues:
    `go run ./cmd/armadactl/main.go --armadaUrl armada.demo.armadaproject.io:443 describe queue queue-a`

d) Watch JobSet/Queue:
    `go run ./cmd/armadactl/main.go --armadaUrl armada.demo.armadaproject.io:443 watch queue-a job-set-1`
    
## Queue Creation via Python Client

1) Create virtual environment
2) Install armada-client
3) run `ARMADA_SERVER=armada.demo.armadaproject.io ARMADA_PORT=443 python3 workflow.py` for creating queue and submitting some jobs

## View Lookout/UI for information about Jobs

Browse to `https://ui.demo.armadaproject.io/job-sets?active_only=false&newest_first=true&queue=kubecon-eu&view=job-counts`

## Airflow Demo

a) Airflow running locally via Sequential Executor
b) dags folder shows some Airflow examples against the EKS Demo Cluster.
c) Browse to `localhost:8081`
