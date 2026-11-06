### Hi, I'm Yashaswini 👋

**Infrastructure / DevOps engineer** working on build and release infrastructure: CI/CD
pipelines (**GitHub Actions** and **Jenkins**), build-agent fleets, configuration management and
observability for large-scale software builds.

I like making infrastructure **boring in the good way**: reproducible, tested, observable, and
safe to change on a Friday.

#### 🔧 What I work with

`GitHub Actions` (dynamic matrices, composite actions, required checks) · `Jenkins` (shared libraries, Pipeline, JCasC) · `Ansible` · `Terraform` ·
`Docker` · `Kubernetes` · `Helm` · `Argo CD` · `OpenStack` · `Prometheus` · `Grafana` ·
`Splunk` · `Python` · `Groovy` · `Bash` · `Linux`

#### 📌 Projects

| project | what it shows |
|---|---|
| [**pr-integration-gate**](https://github.com/yashaswinin61-sketch/pr-integration-gate) | **GitHub Actions** PR gate for long-running integration tests: builds the service from the PR, runs a **dynamic matrix** of end-to-end tests on isolated instances, triages failures (real cause vs infra, with automatic retry), posts a sticky PR comment, and merges only through a single required `gate` check. Based on a gate I built for multi-hour builds on cloud VMs. |
| [**jenkins-pr-gate-library**](https://github.com/yashaswinin61-sketch/jenkins-pr-gate-library) | Jenkins shared library for PR gates: parallel test groups, throwaway OpenStack VMs for integration tests, **HOLD_ON_FAILURE** to SSH into failed environments, and a reaper for leaked VMs. Unit-tested with JenkinsPipelineUnit. |
| [**k8s-platform-gitops**](https://github.com/yashaswinin61-sketch/k8s-platform-gitops) | Terraform → kind → Argo CD app of apps → kube-prometheus-stack + an instrumented service with a hardened Helm chart, HPA, PDB, NetworkPolicy and SLO alerts. The CI e2e test on kind requires **zero failed requests during a rolling restart**. |
| [**ansible-container-services**](https://github.com/yashaswinin61-sketch/ansible-container-services) | Ansible role for running Docker services on VMs with **health-gated rollouts and automatic rollback**, pruning, and secrets kept out of logs. Molecule tests deploy a broken image on purpose and check that the role recovers. |
| [**ci-agent-janitor**](https://github.com/yashaswinin61-sketch/ci-agent-janitor) | Keeps CI build agents from filling their disks: age + LRU free-space policy, lock files protect running builds, and every cleanup is exported to Prometheus with Grafana dashboards and alerts. |

#### 🧭 How I work

- **Test the infrastructure, not just the app**: pipeline unit tests, Molecule, kubeconform, e2e on kind
- **Make it observable**: if a job deletes, scales or fails, there's a metric or log event for it
- **Fail safe**: health gates, rollbacks, TTLs on anything ephemeral, dry-run modes
- **Write it down**: runbooks and KT docs so the next person doesn't have to reverse-engineer anything

#### 📫 Reach me

[LinkedIn](https://www.linkedin.com/in/yashaswini-gowda-136a6a233)
