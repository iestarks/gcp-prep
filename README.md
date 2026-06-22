# Google Cloud Platform (GCP) Interview Questions & Answers

> A curated list of Google Cloud Platform interview questions covering GCP Fundamentals, IAM & Governance, Compute Engine, GKE & Containers, Cloud Run & Serverless, Cloud Storage & File Storage, Databases & Caching, Networking & Load Balancing, Pub/Sub & Event-Driven Architecture, DevOps & CI/CD, Observability & SRE, Security & Compliance, Data Analytics & AI, and Architecture, Reliability, Cost & Migration — each with a clear explanation and Java code example where applicable.

---

### Table of Contents

<details open>
<summary>
Hide/Show table of contents
</summary>

| No. | Questions |
| --- | --------- |
|     | **GCP Fundamentals** |
| 1 | [What is Google Cloud Platform, and how is it different from traditional data centers?](#what-is-google-cloud-platform-and-how-is-it-different-from-traditional-data-centers) |
| 2 | [What is the difference between a Google Cloud project, folder and organization?](#what-is-the-difference-between-a-google-cloud-project-folder-and-organization) |
| 3 | [Why is a project considered the main boundary for billing, IAM and APIs in GCP?](#why-is-a-project-considered-the-main-boundary-for-billing-iam-and-apis-in-gcp) |
| 4 | [What are regions and zones in Google Cloud?](#what-are-regions-and-zones-in-google-cloud) |
| 5 | [How do you choose a region for a production backend application?](#how-do-you-choose-a-region-for-a-production-backend-application) |
| 6 | [What is the difference between regional and zonal resources?](#what-is-the-difference-between-regional-and-zonal-resources) |
| 7 | [What happens if a single zone goes down in GCP?](#what-happens-if-a-single-zone-goes-down-in-gcp) |
| 8 | [What is the purpose of resource hierarchy in Google Cloud?](#what-is-the-purpose-of-resource-hierarchy-in-google-cloud) |
| 9 | [What are labels and tags in Google Cloud?](#what-are-labels-and-tags-in-google-cloud) |
| 10 | [How do you organize multiple environments like dev, QA, staging and production in GCP?](#how-do-you-organize-multiple-environments-like-dev-qa-staging-and-production-in-gcp) |
| 11 | [What is the difference between Google Cloud Console, gcloud CLI and client libraries?](#what-is-the-difference-between-google-cloud-console-gcloud-cli-and-client-libraries) |
| 12 | [What are Google Cloud APIs, and why do they need to be enabled?](#what-are-google-cloud-apis-and-why-do-they-need-to-be-enabled) |
| 13 | [What is a service account in GCP?](#what-is-a-service-account-in-gcp) |
| 14 | [What is Application Default Credentials?](#what-is-application-default-credentials) |
| 15 | [How does Google Cloud handle billing and cost attribution?](#how-does-google-cloud-handle-billing-and-cost-attribution) |
|     | **IAM, Identity and Governance** |
| 16 | [What is IAM in Google Cloud?](#what-is-iam-in-google-cloud) |
| 17 | [What is the difference between a principal, role and permission?](#what-is-the-difference-between-a-principal-role-and-permission) |
| 18 | [What is the difference between basic roles, predefined roles and custom roles?](#what-is-the-difference-between-basic-roles-predefined-roles-and-custom-roles) |
| 19 | [Why should basic roles like Owner, Editor and Viewer be avoided in production?](#why-should-basic-roles-like-owner-editor-and-viewer-be-avoided-in-production) |
| 20 | [What is the principle of least privilege in GCP IAM?](#what-is-the-principle-of-least-privilege-in-gcp-iam) |
| 21 | [How do IAM policies inherit across organization, folder and project levels?](#how-do-iam-policies-inherit-across-organization-folder-and-project-levels) |
| 22 | [What happens when conflicting IAM permissions are applied at different hierarchy levels?](#what-happens-when-conflicting-iam-permissions-are-applied-at-different-hierarchy-levels) |
| 23 | [What is the difference between a user account and a service account?](#what-is-the-difference-between-a-user-account-and-a-service-account) |
| 24 | [What is service account impersonation?](#what-is-service-account-impersonation) |
| 25 | [What is Workload Identity Federation?](#what-is-workload-identity-federation) |
| 26 | [How is Workload Identity Federation different from downloading service account keys?](#how-is-workload-identity-federation-different-from-downloading-service-account-keys) |
| 27 | [Why should service account keys be avoided?](#why-should-service-account-keys-be-avoided) |
| 28 | [How do you rotate service account keys safely?](#how-do-you-rotate-service-account-keys-safely) |
| 29 | [What are IAM conditions?](#what-are-iam-conditions) |
| 30 | [How can IAM conditions be used for time-based or resource-based access?](#how-can-iam-conditions-be-used-for-time-based-or-resource-based-access) |
| 31 | [What are organization policies in GCP?](#what-are-organization-policies-in-gcp) |
| 32 | [How can organization policies restrict resource creation?](#how-can-organization-policies-restrict-resource-creation) |
| 33 | [What is Cloud Identity?](#what-is-cloud-identity) |
| 34 | [What are Cloud Audit Logs?](#what-are-cloud-audit-logs) |
| 35 | [What is the difference between Admin Activity logs and Data Access logs?](#what-is-the-difference-between-admin-activity-logs-and-data-access-logs) |
|     | **Compute Engine** |
| 36 | [What is Compute Engine in Google Cloud?](#what-is-compute-engine-in-google-cloud) |
| 37 | [What is a VM instance in Compute Engine?](#what-is-a-vm-instance-in-compute-engine) |
| 38 | [What is the difference between machine families in Compute Engine?](#what-is-the-difference-between-machine-families-in-compute-engine) |
| 39 | [How do you choose between general-purpose, compute-optimized and memory-optimized machines?](#how-do-you-choose-between-general-purpose-compute-optimized-and-memory-optimized-machines) |
| 40 | [What is a managed instance group?](#what-is-a-managed-instance-group) |
| 41 | [What is the difference between managed and unmanaged instance groups?](#what-is-the-difference-between-managed-and-unmanaged-instance-groups) |
| 42 | [How does autoscaling work in a managed instance group?](#how-does-autoscaling-work-in-a-managed-instance-group) |
| 43 | [What is an instance template?](#what-is-an-instance-template) |
| 44 | [How do you perform a rolling update in Compute Engine?](#how-do-you-perform-a-rolling-update-in-compute-engine) |
| 45 | [What is a startup script in Compute Engine?](#what-is-a-startup-script-in-compute-engine) |
| 46 | [What are Shielded VMs?](#what-are-shielded-vms) |
| 47 | [What are sole-tenant nodes?](#what-are-sole-tenant-nodes) |
| 48 | [What is the difference between Persistent Disks and local SSDs?](#what-is-the-difference-between-persistent-disks-and-local-ssds) |
| 49 | [How do snapshots work for Persistent Disks?](#how-do-snapshots-work-for-persistent-disks) |
| 50 | [What is the difference between Standard, Balanced, SSD and Extreme Persistent Disks?](#what-is-the-difference-between-standard-balanced-ssd-and-extreme-persistent-disks) |
| 51 | [What are Spot VMs?](#what-are-spot-vms) |
| 52 | [When would you use Spot VMs in backend systems?](#when-would-you-use-spot-vms-in-backend-systems) |
| 53 | [How do you design a highly available application using Compute Engine?](#how-do-you-design-a-highly-available-application-using-compute-engine) |
|     | **GKE and Containers** |
| 54 | [What is Google Kubernetes Engine?](#what-is-google-kubernetes-engine) |
| 55 | [What is the difference between GKE Standard and GKE Autopilot?](#what-is-the-difference-between-gke-standard-and-gke-autopilot) |
| 56 | [When would you choose GKE over Cloud Run?](#when-would-you-choose-gke-over-cloud-run) |
| 57 | [What is a GKE cluster?](#what-is-a-gke-cluster) |
| 58 | [What is a node pool in GKE?](#what-is-a-node-pool-in-gke) |
| 59 | [How does GKE manage Kubernetes control plane availability?](#how-does-gke-manage-kubernetes-control-plane-availability) |
| 60 | [What is the difference between regional and zonal GKE clusters?](#what-is-the-difference-between-regional-and-zonal-gke-clusters) |
| 61 | [What are Kubernetes pods, deployments, services and ingress resources?](#what-are-kubernetes-pods-deployments-services-and-ingress-resources) |
| 62 | [How does horizontal pod autoscaling work in GKE?](#how-does-horizontal-pod-autoscaling-work-in-gke) |
| 63 | [How does cluster autoscaling work in GKE?](#how-does-cluster-autoscaling-work-in-gke) |
| 64 | [What is the difference between HPA, VPA and cluster autoscaler?](#what-is-the-difference-between-hpa-vpa-and-cluster-autoscaler) |
| 65 | [What is Workload Identity in GKE?](#what-is-workload-identity-in-gke) |
| 66 | [How does Workload Identity improve security compared to node service accounts?](#how-does-workload-identity-improve-security-compared-to-node-service-accounts) |
| 67 | [What is a Kubernetes service account?](#what-is-a-kubernetes-service-account) |
| 68 | [How do you expose a GKE workload to the internet?](#how-do-you-expose-a-gke-workload-to-the-internet) |
| 69 | [What is the difference between ClusterIP, NodePort, LoadBalancer and Ingress?](#what-is-the-difference-between-clusterip-nodeport-loadbalancer-and-ingress) |
| 70 | [How does GKE integrate with Cloud Load Balancing?](#how-does-gke-integrate-with-cloud-load-balancing) |
| 71 | [What is a readiness probe?](#what-is-a-readiness-probe) |
| 72 | [What is a liveness probe?](#what-is-a-liveness-probe) |
| 73 | [What is a startup probe?](#what-is-a-startup-probe) |
| 74 | [How do you perform zero-downtime deployments in GKE?](#how-do-you-perform-zero-downtime-deployments-in-gke) |
| 75 | [What is a rolling update in Kubernetes?](#what-is-a-rolling-update-in-kubernetes) |
| 76 | [What is a blue-green deployment in GKE?](#what-is-a-blue-green-deployment-in-gke) |
| 77 | [What is a canary deployment in GKE?](#what-is-a-canary-deployment-in-gke) |
| 78 | [How do you troubleshoot a pod stuck in CrashLoopBackOff?](#how-do-you-troubleshoot-a-pod-stuck-in-crashloopbackoff) |
|     | **Cloud Run and Serverless** |
| 79 | [What is Cloud Run?](#what-is-cloud-run) |
| 80 | [How is Cloud Run different from App Engine?](#how-is-cloud-run-different-from-app-engine) |
| 81 | [How is Cloud Run different from Cloud Functions?](#how-is-cloud-run-different-from-cloud-functions) |
| 82 | [When would you choose Cloud Run for a backend service?](#when-would-you-choose-cloud-run-for-a-backend-service) |
| 83 | [What is container-based serverless?](#what-is-container-based-serverless) |
| 84 | [How does autoscaling work in Cloud Run?](#how-does-autoscaling-work-in-cloud-run) |
| 85 | [What is scale-to-zero in Cloud Run?](#what-is-scale-to-zero-in-cloud-run) |
| 86 | [What is a cold start in Cloud Run?](#what-is-a-cold-start-in-cloud-run) |
| 87 | [How can you reduce cold starts in Cloud Run?](#how-can-you-reduce-cold-starts-in-cloud-run) |
| 88 | [What is concurrency in Cloud Run?](#what-is-concurrency-in-cloud-run) |
| 89 | [How do CPU allocation settings affect Cloud Run performance?](#how-do-cpu-allocation-settings-affect-cloud-run-performance) |
| 90 | [How do you secure a Cloud Run service?](#how-do-you-secure-a-cloud-run-service) |
| 91 | [How do you make a Cloud Run service private?](#how-do-you-make-a-cloud-run-service-private) |
| 92 | [How do you connect Cloud Run to a VPC?](#how-do-you-connect-cloud-run-to-a-vpc) |
| 93 | [What is Serverless VPC Access?](#what-is-serverless-vpc-access) |
| 94 | [How can Cloud Run access Cloud SQL privately?](#how-can-cloud-run-access-cloud-sql-privately) |
| 95 | [What is Cloud Functions?](#what-is-cloud-functions) |
| 96 | [What are event-driven Cloud Functions?](#what-are-event-driven-cloud-functions) |
| 97 | [What is App Engine Standard?](#what-is-app-engine-standard) |
| 98 | [What is App Engine Flexible?](#what-is-app-engine-flexible) |
|     | **Cloud Storage and File Storage** |
| 99 | [What is Cloud Storage?](#what-is-cloud-storage) |
| 100 | [What is the difference between object storage and block storage?](#what-is-the-difference-between-object-storage-and-block-storage) |
| 101 | [What is a Cloud Storage bucket?](#what-is-a-cloud-storage-bucket) |
| 102 | [What are Cloud Storage storage classes?](#what-are-cloud-storage-storage-classes) |
| 103 | [How do you choose between Standard, Nearline, Coldline and Archive storage?](#how-do-you-choose-between-standard-nearline-coldline-and-archive-storage) |
| 104 | [What is object versioning in Cloud Storage?](#what-is-object-versioning-in-cloud-storage) |
| 105 | [What is lifecycle management in Cloud Storage?](#what-is-lifecycle-management-in-cloud-storage) |
| 106 | [How do signed URLs work in Cloud Storage?](#how-do-signed-urls-work-in-cloud-storage) |
| 107 | [What is uniform bucket-level access?](#what-is-uniform-bucket-level-access) |
| 108 | [How is Cloud Storage secured using IAM?](#how-is-cloud-storage-secured-using-iam) |
| 109 | [What is the difference between bucket-level IAM and object ACLs?](#what-is-the-difference-between-bucket-level-iam-and-object-acls) |
| 110 | [What is a retention policy in Cloud Storage?](#what-is-a-retention-policy-in-cloud-storage) |
| 111 | [What is object lock in Cloud Storage?](#what-is-object-lock-in-cloud-storage) |
| 112 | [What is Filestore?](#what-is-filestore) |
| 113 | [When would you use Filestore instead of Cloud Storage?](#when-would-you-use-filestore-instead-of-cloud-storage) |
| 114 | [What is Cloud Storage FUSE?](#what-is-cloud-storage-fuse) |
| 115 | [How do you design a secure file upload system using Cloud Storage?](#how-do-you-design-a-secure-file-upload-system-using-cloud-storage) |
|     | **Databases and Caching** |
| 116 | [What is Cloud SQL?](#what-is-cloud-sql) |
| 117 | [Which database engines are supported by Cloud SQL?](#which-database-engines-are-supported-by-cloud-sql) |
| 118 | [When would you choose Cloud SQL over Cloud Spanner?](#when-would-you-choose-cloud-sql-over-cloud-spanner) |
| 119 | [What is the difference between Cloud SQL high availability and read replicas?](#what-is-the-difference-between-cloud-sql-high-availability-and-read-replicas) |
| 120 | [How does Cloud SQL failover work?](#how-does-cloud-sql-failover-work) |
| 121 | [What are Cloud SQL backups?](#what-are-cloud-sql-backups) |
| 122 | [What is point-in-time recovery in Cloud SQL?](#what-is-point-in-time-recovery-in-cloud-sql) |
| 123 | [How do you connect a Spring Boot application to Cloud SQL securely?](#how-do-you-connect-a-spring-boot-application-to-cloud-sql-securely) |
| 124 | [What is the Cloud SQL Auth Proxy?](#what-is-the-cloud-sql-auth-proxy) |
| 125 | [What is private IP connectivity for Cloud SQL?](#what-is-private-ip-connectivity-for-cloud-sql) |
| 126 | [What is Cloud Spanner?](#what-is-cloud-spanner) |
| 127 | [When would you choose Cloud Spanner?](#when-would-you-choose-cloud-spanner) |
| 128 | [How is Cloud Spanner different from a traditional relational database?](#how-is-cloud-spanner-different-from-a-traditional-relational-database) |
| 129 | [What is horizontal scalability in Cloud Spanner?](#what-is-horizontal-scalability-in-cloud-spanner) |
| 130 | [What is strong consistency in Cloud Spanner?](#what-is-strong-consistency-in-cloud-spanner) |
| 131 | [What is AlloyDB?](#what-is-alloydb) |
| 132 | [When would you choose AlloyDB over Cloud SQL for PostgreSQL?](#when-would-you-choose-alloydb-over-cloud-sql-for-postgresql) |
| 133 | [What is Firestore?](#what-is-firestore) |
| 134 | [What is the difference between Firestore Native mode and Datastore mode?](#what-is-the-difference-between-firestore-native-mode-and-datastore-mode) |
| 135 | [When would you choose Firestore for backend application development?](#when-would-you-choose-firestore-for-backend-application-development) |
| 136 | [What is Bigtable?](#what-is-bigtable) |
| 137 | [When would you use Bigtable instead of Firestore?](#when-would-you-use-bigtable-instead-of-firestore) |
| 138 | [What is Memorystore?](#what-is-memorystore) |
| 139 | [What is the difference between Memorystore for Redis and Memorystore for Valkey?](#what-is-the-difference-between-memorystore-for-redis-and-memorystore-for-valkey) |
| 140 | [How do you use Memorystore for caching session data?](#how-do-you-use-memorystore-for-caching-session-data) |
|     | **Networking, Load Balancing, DNS and CDN** |
| 141 | [What is a VPC in Google Cloud?](#what-is-a-vpc-in-google-cloud) |
| 142 | [How is a Google Cloud VPC different from a traditional VPC?](#how-is-a-google-cloud-vpc-different-from-a-traditional-vpc) |
| 143 | [What is the difference between auto mode and custom mode VPC?](#what-is-the-difference-between-auto-mode-and-custom-mode-vpc) |
| 144 | [What are subnets in GCP?](#what-are-subnets-in-gcp) |
| 145 | [Why are GCP subnets regional?](#why-are-gcp-subnets-regional) |
| 146 | [What are firewall rules in GCP?](#what-are-firewall-rules-in-gcp) |
| 147 | [What is the difference between ingress and egress firewall rules?](#what-is-the-difference-between-ingress-and-egress-firewall-rules) |
| 148 | [What are network tags and service accounts used for in firewall rules?](#what-are-network-tags-and-service-accounts-used-for-in-firewall-rules) |
| 149 | [What is Cloud NAT?](#what-is-cloud-nat) |
| 150 | [Why is Cloud NAT used for private workloads?](#why-is-cloud-nat-used-for-private-workloads) |
| 151 | [What is Private Google Access?](#what-is-private-google-access) |
| 152 | [What is Private Service Connect?](#what-is-private-service-connect) |
| 153 | [What is VPC peering?](#what-is-vpc-peering) |
| 154 | [What is Shared VPC?](#what-is-shared-vpc) |
| 155 | [When would you use Shared VPC in an enterprise environment?](#when-would-you-use-shared-vpc-in-an-enterprise-environment) |
| 156 | [What is Cloud Load Balancing?](#what-is-cloud-load-balancing) |
| 157 | [What is the difference between global and regional load balancers?](#what-is-the-difference-between-global-and-regional-load-balancers) |
| 158 | [What is the difference between external and internal load balancing?](#what-is-the-difference-between-external-and-internal-load-balancing) |
| 159 | [What is an HTTP(S) Load Balancer?](#what-is-an-https-load-balancer) |
| 160 | [What is a TCP/UDP Network Load Balancer?](#what-is-a-tcpudp-network-load-balancer) |
| 161 | [What is Cloud CDN?](#what-is-cloud-cdn) |
| 162 | [How does Cloud CDN improve application performance?](#how-does-cloud-cdn-improve-application-performance) |
| 163 | [What is Cloud DNS?](#what-is-cloud-dns) |
| 164 | [What is Cloud Armor?](#what-is-cloud-armor) |
| 165 | [How does Cloud Armor protect backend applications?](#how-does-cloud-armor-protect-backend-applications) |
|     | **Pub/Sub and Event-Driven Architecture** |
| 166 | [What is Pub/Sub?](#what-is-pubsub) |
| 167 | [What is the difference between a topic and a subscription?](#what-is-the-difference-between-a-topic-and-a-subscription) |
| 168 | [What is a publisher in Pub/Sub?](#what-is-a-publisher-in-pubsub) |
| 169 | [What is a subscriber in Pub/Sub?](#what-is-a-subscriber-in-pubsub) |
| 170 | [What is the difference between push and pull subscriptions?](#what-is-the-difference-between-push-and-pull-subscriptions) |
| 171 | [What is acknowledgement in Pub/Sub?](#what-is-acknowledgement-in-pubsub) |
| 172 | [What happens if a Pub/Sub message is not acknowledged?](#what-happens-if-a-pubsub-message-is-not-acknowledged) |
| 173 | [What is acknowledgement deadline?](#what-is-acknowledgement-deadline) |
| 174 | [What is message retention in Pub/Sub?](#what-is-message-retention-in-pubsub) |
| 175 | [What is dead-letter topic in Pub/Sub?](#what-is-dead-letter-topic-in-pubsub) |
| 176 | [What is ordering key in Pub/Sub?](#what-is-ordering-key-in-pubsub) |
| 177 | [How does Pub/Sub support at-least-once delivery?](#how-does-pubsub-support-at-least-once-delivery) |
| 178 | [How do you make Pub/Sub consumers idempotent?](#how-do-you-make-pubsub-consumers-idempotent) |
| 179 | [How do you handle duplicate messages in Pub/Sub?](#how-do-you-handle-duplicate-messages-in-pubsub) |
| 180 | [What is Eventarc?](#what-is-eventarc) |
| 181 | [How is Eventarc related to Cloud Run?](#how-is-eventarc-related-to-cloud-run) |
| 182 | [How would you design an event-driven order processing system on GCP?](#how-would-you-design-an-event-driven-order-processing-system-on-gcp) |
| 183 | [How do you retry failed event processing safely?](#how-do-you-retry-failed-event-processing-safely) |
|     | **DevOps, CI/CD and Infrastructure as Code** |
| 184 | [What is Cloud Build?](#what-is-cloud-build) |
| 185 | [How does Cloud Build work with source repositories?](#how-does-cloud-build-work-with-source-repositories) |
| 186 | [What is a cloudbuild.yaml file?](#what-is-a-cloudbuildyaml-file) |
| 187 | [How do you build and push a Docker image to Artifact Registry?](#how-do-you-build-and-push-a-docker-image-to-artifact-registry) |
| 188 | [What is Artifact Registry?](#what-is-artifact-registry) |
| 189 | [How is Artifact Registry different from Container Registry?](#how-is-artifact-registry-different-from-container-registry) |
| 190 | [What is Cloud Deploy?](#what-is-cloud-deploy) |
| 191 | [How do you implement progressive delivery using Cloud Deploy?](#how-do-you-implement-progressive-delivery-using-cloud-deploy) |
| 192 | [How do you deploy a Cloud Run service using Cloud Build?](#how-do-you-deploy-a-cloud-run-service-using-cloud-build) |
| 193 | [How do you deploy to GKE using a CI/CD pipeline?](#how-do-you-deploy-to-gke-using-a-cicd-pipeline) |
| 194 | [What is Infrastructure as Code?](#what-is-infrastructure-as-code) |
| 195 | [How do you use Terraform with Google Cloud?](#how-do-you-use-terraform-with-google-cloud) |
| 196 | [What is a Terraform provider for Google Cloud?](#what-is-a-terraform-provider-for-google-cloud) |
| 197 | [How do you manage Terraform state for GCP projects?](#how-do-you-manage-terraform-state-for-gcp-projects) |
| 198 | [What is Infrastructure Manager in Google Cloud?](#what-is-infrastructure-manager-in-google-cloud) |
| 199 | [How do you manage secrets in CI/CD pipelines?](#how-do-you-manage-secrets-in-cicd-pipelines) |
| 200 | [How do you handle environment-specific configuration in GCP deployments?](#how-do-you-handle-environment-specific-configuration-in-gcp-deployments) |
| 201 | [How do you implement rollback in a GCP deployment pipeline?](#how-do-you-implement-rollback-in-a-gcp-deployment-pipeline) |
| 202 | [How do you enforce approvals before production deployment?](#how-do-you-enforce-approvals-before-production-deployment) |
| 203 | [How do you design a CI/CD pipeline for a Spring Boot microservice on GCP?](#how-do-you-design-a-cicd-pipeline-for-a-spring-boot-microservice-on-gcp) |
|     | **Observability, Logging, Monitoring and SRE** |
| 204 | [What is Cloud Logging?](#what-is-cloud-logging) |
| 205 | [What is Cloud Monitoring?](#what-is-cloud-monitoring) |
| 206 | [What are log-based metrics?](#what-are-log-based-metrics) |
| 207 | [What are uptime checks?](#what-are-uptime-checks) |
| 208 | [What are alerting policies in Cloud Monitoring?](#what-are-alerting-policies-in-cloud-monitoring) |
| 209 | [What is Cloud Trace?](#what-is-cloud-trace) |
| 210 | [What is Cloud Profiler?](#what-is-cloud-profiler) |
| 211 | [What is Error Reporting?](#what-is-error-reporting) |
| 212 | [How do you monitor a Cloud Run service?](#how-do-you-monitor-a-cloud-run-service) |
| 213 | [How do you monitor a GKE workload?](#how-do-you-monitor-a-gke-workload) |
| 214 | [How do you define SLI, SLO and SLA?](#how-do-you-define-sli-slo-and-sla) |
| 215 | [What is an error budget?](#what-is-an-error-budget) |
| 216 | [How do you troubleshoot high latency in a GCP backend service?](#how-do-you-troubleshoot-high-latency-in-a-gcp-backend-service) |
| 217 | [How do you troubleshoot increased 5xx errors behind a load balancer?](#how-do-you-troubleshoot-increased-5xx-errors-behind-a-load-balancer) |
| 218 | [How do you correlate application logs with request IDs?](#how-do-you-correlate-application-logs-with-request-ids) |
| 219 | [How do you design observability for microservices on GCP?](#how-do-you-design-observability-for-microservices-on-gcp) |
|     | **Security and Compliance** |
| 220 | [What is Secret Manager?](#what-is-secret-manager) |
| 221 | [Why should secrets not be stored in environment variables or source code?](#why-should-secrets-not-be-stored-in-environment-variables-or-source-code) |
| 222 | [How do you rotate secrets in Secret Manager?](#how-do-you-rotate-secrets-in-secret-manager) |
| 223 | [What is Cloud KMS?](#what-is-cloud-kms) |
| 224 | [What is the difference between Google-managed keys and customer-managed encryption keys?](#what-is-the-difference-between-google-managed-keys-and-customer-managed-encryption-keys) |
| 225 | [What is CMEK?](#what-is-cmek) |
| 226 | [What is VPC Service Controls?](#what-is-vpc-service-controls) |
| 227 | [How does VPC Service Controls reduce data exfiltration risk?](#how-does-vpc-service-controls-reduce-data-exfiltration-risk) |
| 228 | [What is Security Command Center?](#what-is-security-command-center) |
| 229 | [What is Binary Authorization?](#what-is-binary-authorization) |
| 230 | [How does Binary Authorization secure container deployments?](#how-does-binary-authorization-secure-container-deployments) |
| 231 | [What is Container Analysis?](#what-is-container-analysis) |
| 232 | [What is vulnerability scanning in Artifact Registry?](#what-is-vulnerability-scanning-in-artifact-registry) |
| 233 | [How do you secure a public API deployed on Cloud Run?](#how-do-you-secure-a-public-api-deployed-on-cloud-run) |
| 234 | [How do you protect backend APIs from DDoS and abusive traffic?](#how-do-you-protect-backend-apis-from-ddos-and-abusive-traffic) |
| 235 | [How do you audit access to sensitive resources in GCP?](#how-do-you-audit-access-to-sensitive-resources-in-gcp) |
|     | **Data, Analytics and AI Integration** |
| 236 | [What is BigQuery?](#what-is-bigquery) |
| 237 | [When would you use BigQuery instead of Cloud SQL?](#when-would-you-use-bigquery-instead-of-cloud-sql) |
| 238 | [What is partitioning in BigQuery?](#what-is-partitioning-in-bigquery) |
| 239 | [What is clustering in BigQuery?](#what-is-clustering-in-bigquery) |
| 240 | [What is Dataflow?](#what-is-dataflow) |
| 241 | [How is Dataflow related to Apache Beam?](#how-is-dataflow-related-to-apache-beam) |
| 242 | [What is Dataproc?](#what-is-dataproc) |
| 243 | [How can backend applications integrate with Vertex AI on GCP?](#how-can-backend-applications-integrate-with-vertex-ai-on-gcp) |
|     | **Architecture, Reliability, Cost and Migration** |
| 244 | [How do you design a highly available backend system on GCP?](#how-do-you-design-a-highly-available-backend-system-on-gcp) |
| 245 | [How do you design a multi-region disaster recovery architecture on GCP?](#how-do-you-design-a-multi-region-disaster-recovery-architecture-on-gcp) |
| 246 | [What is the difference between active-active and active-passive architecture?](#what-is-the-difference-between-active-active-and-active-passive-architecture) |
| 247 | [How do you estimate and optimize cost for a GCP backend system?](#how-do-you-estimate-and-optimize-cost-for-a-gcp-backend-system) |
| 248 | [How do you migrate an on-premise Java application to GCP?](#how-do-you-migrate-an-on-premise-java-application-to-gcp) |
| 249 | [How do you choose between Compute Engine, GKE, Cloud Run and App Engine?](#how-do-you-choose-between-compute-engine-gke-cloud-run-and-app-engine) |
| 250 | [How would you design a scalable order management system on GCP?](#how-would-you-design-a-scalable-order-management-system-on-gcp) |

</details>

---

## GCP Fundamentals

1. ### What is Google Cloud Platform, and how is it different from traditional data centers?

   **Google Cloud Platform (GCP)** is a suite of managed cloud services running on Google's global infrastructure that lets you run applications and store data without owning physical hardware. Unlike traditional on-premises data centers where you buy, rack, power, cool, and patch your own servers, GCP delivers compute, storage, networking, and higher-level services (AI, analytics, databases) as **elastic, pay-as-you-go resources**.

   | Aspect | Traditional Data Center | Google Cloud Platform |
   | --- | --- | --- |
   | **Capital cost** | High upfront CapEx (buy servers) | Pay-as-you-go OpEx |
   | **Scaling** | Manual capacity planning, weeks | Elastic, on-demand, seconds |
   | **Maintenance** | You patch and operate everything | Google maintains the platform |
   | **Global reach** | Build your own DCs | 40+ regions, instant deployment |
   | **Automation** | Limited / custom scripts | Rich APIs, CLI, IaC support |

   ```java
   // Programmatic access via the Google Cloud client library (Compute Engine example)
   import com.google.cloud.compute.v1.InstancesClient;
   import com.google.cloud.compute.v1.Instance;

   try (InstancesClient client = InstancesClient.create()) {
       // List all VM instances in a zone — no physical hardware required
       for (Instance instance : client.list("my-project", "us-central1-a").iterateAll()) {
           System.out.println("Instance: " + instance.getName());
       }
   }
   ```

   **[⬆ Back to Top](#table-of-contents)**

2. ### What is the difference between a Google Cloud project, folder and organization?

   GCP arranges resources in a three-level **resource hierarchy**:

   | Level | Role |
   | --- | --- |
   | **Organization** | Root node, usually maps to a company domain (e.g., `example.com`). Root for IAM, org policies, and billing. |
   | **Folder** | Optional grouping under the organization — e.g., per department (`Engineering`, `Finance`) or environment (`dev`, `prod`). Folders can nest. |
   | **Project** | The fundamental unit where resources (VMs, buckets, Cloud Run services) live. Has its own billing link, APIs, and IAM. |

   Resources **inherit policies** from their parent folder and organization. An IAM role granted at the organization level cascades down to every folder and project beneath it.

   ```
   Organization (example.com)
   ├── Folder: Engineering
   │   ├── Project: myapp-dev
   │   ├── Project: myapp-staging
   │   └── Project: myapp-prod
   └── Folder: Finance
       └── Project: billing-analytics
   ```

   **[⬆ Back to Top](#table-of-contents)**

3. ### Why is a project considered the main boundary for billing, IAM and APIs in GCP?

   Every GCP resource belongs to **exactly one project**, which makes the project the natural isolation boundary:

   - **Billing** — usage is aggregated and charged at the project level via the linked billing account. Separate projects = separate cost tracking.
   - **IAM** — policies are defined at the project level and inherited by all resources inside. This gives a clean scope for granting or revoking access.
   - **APIs** — enabling Compute Engine or Cloud Run applies only to that project's resources, limiting attack surface and accidental charges.
   - **Quotas** — service quotas (CPUs, IPs, API calls) are tracked per project, preventing one app from exhausting another's capacity.

   By keeping environments or applications in separate projects, you **isolate their billing, quotas, and security blast radius**.

   **[⬆ Back to Top](#table-of-contents)**

4. ### What are regions and zones in Google Cloud?

   - A **region** is a geographic area (e.g., `us-central1` in Iowa, `asia-south1` in Mumbai) containing one or more zones.
   - A **zone** is a single isolated deployment area (essentially a data center) within a region, named like `us-central1-a`.

   **Zonal resources** (Compute Engine VMs, local SSDs) live in one zone; if that zone fails, they become unavailable. **Regional resources** (Regional Persistent Disks, regional MIGs, Cloud SQL HA) replicate across multiple zones in a region for resilience.

   ```bash
   # List available regions and zones
   gcloud compute regions list
   gcloud compute zones list --filter="region:us-central1"
   # Output: us-central1-a, us-central1-b, us-central1-c, us-central1-f
   ```

   **Best practice:** spread workloads across **multiple zones** (and sometimes regions) so a single-zone outage doesn't take down your service.

   **[⬆ Back to Top](#table-of-contents)**

5. ### How do you choose a region for a production backend application?

   Key considerations when selecting a region:

   - **Latency to users** — pick the region closest to your primary user base to minimize round-trip time. For users in India, `asia-south1` (Mumbai) or `asia-south2` (Delhi).
   - **Service availability** — not every GCP service exists in every region; confirm your required services (e.g., a specific GPU, AlloyDB) are present.
   - **Cost** — compute, storage, and egress prices vary by region; balance latency against cost.
   - **Data residency & compliance** — regulations (GDPR, India's data localization) may require data to stay within a geographic boundary.
   - **Multi-region strategy** — for HA/DR, deploy across multiple regions using active-active or active-passive patterns.

   **[⬆ Back to Top](#table-of-contents)**

6. ### What is the difference between regional and zonal resources?

   | | Zonal Resource | Regional Resource |
   | --- | --- | --- |
   | **Scope** | Single zone | Spans multiple zones in a region |
   | **Failure impact** | Lost if the zone fails | Survives single-zone failure |
   | **Examples** | Compute Engine VM, Local SSD, zonal MIG | Regional Persistent Disk, Cloud SQL HA, regional MIG |
   | **Cost** | Lower | Slightly higher (replication overhead) |
   | **Use case** | Stateless / fault-tolerant workloads | Stateful data needing redundancy |

   A **Regional Persistent Disk** synchronously replicates across two zones, so if one zone goes down, your data is still accessible from the other. This is the foundation for highly available stateful applications.

   **[⬆ Back to Top](#table-of-contents)**

7. ### What happens if a single zone goes down in GCP?

   When a zone fails:

   - **All zonal resources** in that zone (VMs, local SSDs, zonal disks) become **unavailable**.
   - **Regional resources** keep operating because they replicate across other zones in the region.
   - **Load balancers** automatically reroute traffic to healthy backends in surviving zones.

   **Architecting for zone failure:**
   - Use **regional managed instance groups** that distribute VMs across multiple zones.
   - Store stateful data on **Regional Persistent Disks** or multi-zone databases like **Cloud Spanner** / **Cloud SQL HA**.
   - Place backends behind a **load balancer** with health checks for automatic failover.

   ```bash
   # Create a regional MIG spanning 3 zones for zone-failure resilience
   gcloud compute instance-groups managed create my-mig \
       --template=my-template \
       --size=6 \
       --region=us-central1 \
       --zones=us-central1-a,us-central1-b,us-central1-c
   ```

   **[⬆ Back to Top](#table-of-contents)**

8. ### What is the purpose of resource hierarchy in Google Cloud?

   The **resource hierarchy** is a tree — Organization → Folders → Projects → Resources — that serves several purposes:

   - **Policy inheritance** — IAM and organization policies set at a higher level automatically apply to descendants, reducing repetitive configuration.
   - **Logical structure** — organize by department, team, environment, or cost center.
   - **Centralized governance** — enforce security and compliance constraints org-wide from a single point.
   - **Access delegation** — grant a team admin rights over their folder without exposing the rest of the org.

   This structure scales cleanly from a handful of projects to thousands across a large enterprise.

   **[⬆ Back to Top](#table-of-contents)**

9. ### What are labels and tags in Google Cloud?

   - **Labels** are key–value pairs attached to resources for **metadata and organization** (e.g., `env:prod`, `team:payments`, `cost-center:1234`). They're used for cost reporting, filtering logs, and building dashboards. Labels work across almost all GCP services.
   - **Network tags** are simple strings applied to Compute Engine instances and referenced by **firewall rules and routes** to target a subset of VMs (e.g., a rule allowing port 443 only to instances tagged `web`).

   ```bash
   # Add a label to a bucket for cost tracking
   gcloud storage buckets update gs://my-bucket --update-labels=env=prod,team=payments

   # Add a network tag to a VM, then a firewall rule targeting it
   gcloud compute instances add-tags web-server --tags=web --zone=us-central1-a
   gcloud compute firewall-rules create allow-https \
       --allow=tcp:443 --target-tags=web --network=default
   ```

   **Note:** GCP also has resource-level **Tags** (distinct from network tags) used for conditional IAM and org policies — but in interviews "tags" usually means network tags for firewalls.

   **[⬆ Back to Top](#table-of-contents)**

10. ### How do you organize multiple environments like dev, QA, staging and production in GCP?

    The recommended pattern is **separate projects per environment** (e.g., `myapp-dev`, `myapp-qa`, `myapp-staging`, `myapp-prod`), often grouped into **folders** for shared policy:

    - **Isolation** — each environment gets its own IAM, quotas, billing, and blast radius. A mistake in dev cannot touch prod.
    - **Separation of duties** — developers get broad access in dev, restricted access in prod.
    - **Consistent provisioning** — use **Infrastructure as Code** (Terraform or Infrastructure Manager) to deploy the same resource definitions into each project with environment-specific variables.

    ```hcl
    # Terraform: one module reused per environment with different variables
    module "backend" {
      source     = "./modules/backend"
      project_id = var.project_id   # myapp-dev, myapp-prod, etc.
      env        = var.env
      machine_type = var.env == "prod" ? "n2-standard-4" : "e2-small"
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

11. ### What is the difference between Google Cloud Console, gcloud CLI and client libraries?

    | Tool | Type | Best For |
    | --- | --- | --- |
    | **Cloud Console** | Web UI | Visual exploration, one-off tasks, dashboards |
    | **gcloud CLI** | Command-line | Scripting, automation, CI/CD pipelines |
    | **Client libraries** | Language SDKs (Java, Python, Go…) | Application code calling GCP APIs programmatically |

    The Console is great for learning and ad-hoc management. The `gcloud` CLI shines in scripts and pipelines. Client libraries handle **authentication, retries, and idiomatic constructs** so your app can call GCP services natively.

    ```java
    // Java client library — upload an object to Cloud Storage
    import com.google.cloud.storage.*;

    Storage storage = StorageOptions.getDefaultInstance().getService();
    BlobId blobId = BlobId.of("my-bucket", "hello.txt");
    BlobInfo blobInfo = BlobInfo.newBuilder(blobId).setContentType("text/plain").build();
    storage.create(blobInfo, "Hello GCP".getBytes());
    ```

    **[⬆ Back to Top](#table-of-contents)**

12. ### What are Google Cloud APIs, and why do they need to be enabled?

    Every GCP service exposes its functionality through a **REST/gRPC API**. Before you can use a service in a project, its API must be **enabled**, which:

    - Activates the backend service for the project.
    - Provisions quotas and billing for it.
    - Allows service account credentials to call it.

    APIs are **disabled by default** to reduce attack surface and avoid accidental charges.

    ```bash
    # Enable required APIs for a backend app
    gcloud services enable \
        compute.googleapis.com \
        run.googleapis.com \
        sqladmin.googleapis.com \
        secretmanager.googleapis.com

    # List enabled APIs
    gcloud services list --enabled
    ```

    **[⬆ Back to Top](#table-of-contents)**

13. ### What is a service account in GCP?

    A **service account** is a special non-human Google account used by **applications and workloads** to authenticate to GCP APIs. Key points:

    - Identified by an email like `my-app@my-project.iam.gserviceaccount.com`.
    - Granted **IAM roles** to control what it can do.
    - Can be **attached** to Compute Engine VMs, Cloud Run services, or GKE pods (via Workload Identity) so code authenticates automatically without keys.
    - Follow **least privilege** — create purpose-specific accounts with minimal roles.

    ```bash
    # Create a service account and grant it a narrow role
    gcloud iam service-accounts create order-service \
        --display-name="Order Processing Service"

    gcloud projects add-iam-policy-binding my-project \
        --member="serviceAccount:order-service@my-project.iam.gserviceaccount.com" \
        --role="roles/pubsub.publisher"
    ```

    **[⬆ Back to Top](#table-of-contents)**

14. ### What is Application Default Credentials?

    **Application Default Credentials (ADC)** is the mechanism Google client libraries and the `gcloud` CLI use to **automatically discover credentials** without hard-coding them. ADC looks for credentials in this order:

    1. The `GOOGLE_APPLICATION_CREDENTIALS` environment variable (path to a key file).
    2. User credentials from `gcloud auth application-default login` (local dev).
    3. The **attached service account** via the metadata server (when running on GCP compute like a VM, Cloud Run, or GKE).

    This means the **same code** runs locally and in production without changes — on GCP it transparently uses the workload's service account.

    ```java
    // No explicit credentials needed — ADC resolves them automatically
    Storage storage = StorageOptions.getDefaultInstance().getService();
    // On a VM/Cloud Run → uses attached SA; locally → uses gcloud user creds
    ```

    **[⬆ Back to Top](#table-of-contents)**

15. ### How does Google Cloud handle billing and cost attribution?

    - Each **project links to exactly one billing account**; all resource usage in the project is charged there.
    - **Cloud Billing reports** and **BigQuery billing export** let you analyze costs by project, service, or **label**.
    - **Budgets and alerts** notify you when spending crosses thresholds.
    - **Quotas** cap resource usage to prevent runaway costs.
    - **Discounts** reduce cost: **sustained use discounts** (automatic for long-running VMs) and **committed use discounts** (1- or 3-year commitments).

    ```bash
    # Create a budget alert at 80% of $1000/month
    gcloud billing budgets create \
        --billing-account=XXXXXX-XXXXXX-XXXXXX \
        --display-name="Monthly Backend Budget" \
        --budget-amount=1000USD \
        --threshold-rule=percent=0.8
    ```

    **Tip:** label every resource with `team`, `env`, and `cost-center` so billing export queries in BigQuery can attribute spend accurately.

    **[⬆ Back to Top](#table-of-contents)**


## IAM, Identity and Governance

16. ### What is IAM in Google Cloud?

    **Identity and Access Management (IAM)** is GCP's authorization system. It answers the question: **"who can do what on which resource?"** IAM lets you grant granular **roles** (collections of permissions) to **principals** (users, groups, service accounts) on resources like projects, folders, and individual services. This enables **least-privilege access** and **separation of duties**.

    ```bash
    # Grant a user the ability to view (but not modify) Compute Engine resources
    gcloud projects add-iam-policy-binding my-project \
        --member="user:alice@example.com" \
        --role="roles/compute.viewer"
    ```

    **[⬆ Back to Top](#table-of-contents)**

17. ### What is the difference between a principal, role and permission?

    | Term | Definition | Example |
    | --- | --- | --- |
    | **Principal** | An identity that can be granted access | `user:alice@example.com`, `serviceAccount:app@...`, `group:devs@...` |
    | **Permission** | The ability to perform one specific operation | `compute.instances.create` |
    | **Role** | A named collection of permissions | `roles/compute.instanceAdmin` |

    You **bind a role to a principal on a resource**. The principal then receives all permissions in that role for that resource. Roles come in three flavors: **basic**, **predefined**, and **custom**.

    **[⬆ Back to Top](#table-of-contents)**

18. ### What is the difference between basic roles, predefined roles and custom roles?

    | Role Type | Scope | Description |
    | --- | --- | --- |
    | **Basic** (Owner, Editor, Viewer) | All services | Broad, legacy roles. Owner manages everything incl. IAM; Editor modifies most resources; Viewer is read-only. **Discouraged in production.** |
    | **Predefined** | Per service | Curated by Google for specific services, e.g. `roles/storage.objectViewer`. Automatically updated as features ship. Follow naming like Admin/Editor/Viewer. |
    | **Custom** | Your choice | You hand-pick the exact permissions. Useful when no predefined role fits, but you must maintain them as services add permissions. |

    ```bash
    # Create a custom role with a minimal permission set
    gcloud iam roles create orderProcessor --project=my-project \
        --title="Order Processor" \
        --permissions=pubsub.topics.publish,pubsub.subscriptions.consume
    ```

    **[⬆ Back to Top](#table-of-contents)**

19. ### Why should basic roles like Owner, Editor and Viewer be avoided in production?

    Basic roles are **"primitive"** — they span **all GCP services** at once. Granting `Editor`, for instance, gives modify rights to Compute Engine, Cloud Storage, networking, databases, and more.

    Risks in production:

    - **Violates least privilege** — principals get far more access than they need.
    - **Large blast radius** — a compromised or careless account can damage many services.
    - **Harder audits** — broad grants obscure who can actually do what.

    Instead, assign **predefined roles** scoped to specific services, or **custom roles** with minimal permissions, at the **narrowest resource scope** (e.g., a single bucket rather than the whole project).

    **[⬆ Back to Top](#table-of-contents)**

20. ### What is the principle of least privilege in GCP IAM?

    The **principle of least privilege (PoLP)** states that each identity should have **only the minimum permissions needed** to do its job — nothing more. In GCP this means:

    - Use **predefined roles** targeted to a service/function rather than basic roles.
    - Grant roles at the **narrowest scope** (a single bucket, topic, or dataset — not the whole project).
    - Prefer **short-lived credentials** (Workload Identity, impersonation) over long-lived keys.

    PoLP **reduces blast radius**, simplifies compliance audits, and improves overall security posture. Tools like **IAM Recommender** suggest removing unused permissions.

    **[⬆ Back to Top](#table-of-contents)**

21. ### How do IAM policies inherit across organization, folder and project levels?

    IAM policies set at a **higher level cascade down** to all descendants:

    ```
    Organization  ── grant roles/bigquery.admin to data-team@
        ↓ (inherited)
    Folder: Analytics
        ↓ (inherited)
    Project: warehouse-prod  → data-team@ automatically has BigQuery Admin here
    ```

    - A role granted at the **organization** applies to every folder, project, and resource under it.
    - A role granted at a **folder** applies to all projects in that folder.
    - The **effective policy** on a resource is the **union** of all inherited bindings plus its own.

    **IAM Conditions** and **Deny policies** lower in the tree can constrain or block inherited access. You cannot "subtract" an allow grant by re-granting — you must use a **Deny policy**.

    **[⬆ Back to Top](#table-of-contents)**

22. ### What happens when conflicting IAM permissions are applied at different hierarchy levels?

    - **Allow grants are additive** — the effective set of permissions is the **union** of all allow bindings across org, folder, and project.
    - **Deny policies take precedence** — an IAM **Deny rule** blocks a permission even if it's granted by an allow binding elsewhere. Deny is evaluated **before** allow.
    - **IAM Conditions** add context-based constraints (time, IP, resource attributes) that must evaluate to `true` for the grant to apply.

    So if a user is granted `storage.objects.delete` at the project level but a Deny policy at the folder blocks it, the **deny wins** and the user cannot delete objects.

    **[⬆ Back to Top](#table-of-contents)**

23. ### What is the difference between a user account and a service account?

    | | User Account | Service Account |
    | --- | --- | --- |
    | **Represents** | A human | An application / workload |
    | **Authentication** | Google sign-in (interactive) | Keys, tokens, or attached identity |
    | **Console login** | Yes | No |
    | **Use case** | People managing resources | Long-running programmatic access |

    Both can be **principals** in IAM policies. For workloads (VMs, Cloud Run, GKE), **service accounts** are strongly recommended — ideally via **Workload Identity** so no key files are needed.

    **[⬆ Back to Top](#table-of-contents)**

24. ### What is service account impersonation?

    **Impersonation** lets a principal **temporarily act as a service account** without holding its private key. The impersonator calls the **IAM Credentials API** to mint short-lived OAuth tokens for the target service account.

    Benefits:
    - **No long-lived keys** to distribute or leak.
    - **Central audit and revocation** — impersonation is logged and can be disabled instantly.
    - Common in **Workload Identity Federation** and bridging on-prem identities to GCP.

    ```bash
    # Grant a user permission to impersonate a service account
    gcloud iam service-accounts add-iam-policy-binding \
        order-service@my-project.iam.gserviceaccount.com \
        --member="user:alice@example.com" \
        --role="roles/iam.serviceAccountTokenCreator"

    # Run a command as the impersonated SA
    gcloud storage ls --impersonate-service-account=order-service@my-project.iam.gserviceaccount.com
    ```

    **[⬆ Back to Top](#table-of-contents)**

25. ### What is Workload Identity Federation?

    **Workload Identity Federation (WIF)** lets workloads running **outside GCP** (in AWS, Azure, on-prem, GitHub Actions, etc.) obtain **short-lived GCP credentials without a service account key**. It works by exchanging an external identity provider's token (OIDC or AWS IAM) for a Google access token that maps to a GCP service account.

    Why it matters:
    - **No static keys** to store, rotate, or leak.
    - **Short-lived, scoped tokens** that expire automatically.
    - Centralized trust between your external IdP and Google.

    ```
    External workload (e.g. GitHub Actions)
        → presents OIDC token to GCP STS
        → STS validates against the Workload Identity Pool
        → returns a short-lived Google access token (mapped to a GCP SA)
    ```

    **[⬆ Back to Top](#table-of-contents)**

26. ### How is Workload Identity Federation different from downloading service account keys?

    | | Service Account Keys | Workload Identity Federation |
    | --- | --- | --- |
    | **Credential type** | Long-lived JSON key file | Short-lived exchanged token |
    | **Leak risk** | High — abusable until revoked | Low — tokens expire quickly |
    | **Rotation** | Manual, error-prone | Automatic (no key to rotate) |
    | **Key management** | You store and protect files | No key to manage |

    With WIF, your external workload uses its **existing identity** (e.g., GitHub's OIDC token) to obtain Google credentials, eliminating the dangerous practice of committing or distributing key files.

    **[⬆ Back to Top](#table-of-contents)**

27. ### Why should service account keys be avoided?

    Service account keys are **static, long-lived secrets**. If a key file is:

    - **Committed to source control** — attackers can impersonate the account indefinitely.
    - **Leaked in logs or images** — same risk, often undetected for months.

    They also require **manual rotation**, which is error-prone and frequently neglected. Safer alternatives provide **keyless, auto-expiring** authentication:

    - **Workload Identity** (GKE) and attached service accounts (VMs, Cloud Run).
    - **Workload Identity Federation** (external workloads).
    - **Service account impersonation** (short-lived tokens).

    Use the org policy `iam.disableServiceAccountKeyCreation` to block key creation entirely.

    **[⬆ Back to Top](#table-of-contents)**

28. ### How do you rotate service account keys safely?

    If you must use keys, rotate them with a **make-before-break** approach to avoid downtime:

    1. **Create** a new key while the old one is still valid.
    2. **Distribute** the new key to all consuming applications.
    3. **Verify** all apps use the new key successfully.
    4. **Delete** the old key.

    ```bash
    # 1. Create new key
    gcloud iam service-accounts keys create new-key.json \
        --iam-account=order-service@my-project.iam.gserviceaccount.com

    # 2-3. Deploy new-key.json everywhere, verify...

    # 4. List keys and delete the old one
    gcloud iam service-accounts keys list \
        --iam-account=order-service@my-project.iam.gserviceaccount.com
    gcloud iam service-accounts keys delete OLD_KEY_ID \
        --iam-account=order-service@my-project.iam.gserviceaccount.com
    ```

    Minimize the overlap window and rotate on a regular schedule. Better still — eliminate keys with Workload Identity.

    **[⬆ Back to Top](#table-of-contents)**

29. ### What are IAM conditions?

    **IAM Conditions** add **context-aware, attribute-based logic** to role bindings. A condition is a CEL (Common Expression Language) expression that must evaluate to `true` for the permission to apply. Conditions can check:

    - **Request time** (`request.time`) — business hours only.
    - **Request IP / device** — only from corporate network.
    - **Resource attributes** (`resource.name`, `resource.type`, labels) — only a specific bucket prefix.

    ```bash
    # Grant Storage Object Viewer only for buckets whose name starts with "public-"
    gcloud projects add-iam-policy-binding my-project \
        --member="user:alice@example.com" \
        --role="roles/storage.objectViewer" \
        --condition='expression=resource.name.startsWith("projects/_/buckets/public-"),title=public-buckets-only'
    ```

    **[⬆ Back to Top](#table-of-contents)**

30. ### How can IAM conditions be used for time-based or resource-based access?

    - **Time-based access** — use `request.time` to restrict when a permission applies:

      ```
      request.time.getHours("America/New_York") >= 8 &&
      request.time.getHours("America/New_York") < 18
      ```
      This grants access only between 8 AM and 6 PM Eastern.

    - **Resource-based access** — use `resource.name`, `resource.type`, or labels to scope access to specific resources:

      ```
      resource.name.startsWith("projects/_/buckets/finance-")
      ```
      This limits access to buckets in the `finance-` namespace.

    Conditions let you implement **fine-grained, just-in-time** access without creating many narrowly-scoped roles.

    **[⬆ Back to Top](#table-of-contents)**

31. ### What are organization policies in GCP?

    **Organization policies** enforce **constraints** on what resources and configurations are allowed across projects. Unlike IAM (which controls *who* can act), org policies control *what* is permitted. Examples:

    - Disable creation of VMs with external IPs.
    - Restrict which regions resources can be created in.
    - Require specific OS images or disable serial-port access.
    - Limit IAM grants to principals from approved domains.

    Policies are set at the **organization or folder** level and **inherited** by descendant projects, ensuring consistent compliance.

    **[⬆ Back to Top](#table-of-contents)**

32. ### How can organization policies restrict resource creation?

    You apply **constraints** that GCP enforces automatically whenever a resource is created or modified. Common examples:

    | Constraint | Effect |
    | --- | --- |
    | `compute.vmExternalIpAccess` | Prevents VMs from getting public IPs |
    | `compute.disableSerialPortAccess` | Blocks serial console access |
    | `gcp.resourceLocations` | Restricts which regions/zones can be used |
    | `iam.allowedPolicyMemberDomains` | Limits IAM bindings to specific domains |
    | `iam.disableServiceAccountKeyCreation` | Blocks SA key creation |

    ```bash
    # Enforce: VMs cannot have external IPs (org-wide)
    gcloud resource-manager org-policies enable-enforce \
        compute.vmExternalIpAccess --organization=ORG_ID
    ```

    **[⬆ Back to Top](#table-of-contents)**

33. ### What is Cloud Identity?

    **Cloud Identity** is Google's managed **identity and directory service**. It provides enterprise-grade user, group, and device management and can:

    - Act as a **standalone identity provider** (IdP).
    - **Federate** with on-prem Active Directory or third-party IdPs (Okta, Azure AD) via SSO/SAML.
    - Centrally manage **users, groups, devices, and security settings**.

    Cloud Identity accounts become **principals** in GCP IAM, so you manage human access to GCP resources from one place. It's the foundation for organizing users into groups that receive IAM roles.

    **[⬆ Back to Top](#table-of-contents)**

34. ### What are Cloud Audit Logs?

    **Cloud Audit Logs** record **who did what, where, and when** across GCP services. There are four types:

    | Log Type | Records | Default |
    | --- | --- | --- |
    | **Admin Activity** | Config changes (create/delete/modify) | Always on, free |
    | **Data Access** | Reads/writes of user data | Off by default (high volume) |
    | **System Event** | Google-initiated system actions | Always on |
    | **Policy Denied** | Denied access attempts | On when access is denied |

    They integrate with **Cloud Logging** and **Cloud Monitoring** for analysis and alerting, and can be exported to BigQuery for long-term retention and compliance.

    **[⬆ Back to Top](#table-of-contents)**

35. ### What is the difference between Admin Activity logs and Data Access logs?

    | | Admin Activity Logs | Data Access Logs |
    | --- | --- | --- |
    | **Captures** | Configuration changes (create/delete/update) | Reads and writes of user data |
    | **Examples** | Creating a VM, deleting a bucket, changing IAM | Reading a BigQuery table, downloading a GCS object |
    | **Default** | Always enabled, no cost | Disabled by default (must opt in) |
    | **Volume** | Lower | Very high (can be costly) |

    **Admin Activity logs** are essential for security and always recorded. **Data Access logs** are powerful for forensics but generate huge volumes, so you enable them selectively on sensitive services.

    ```bash
    # Enable Data Access logging for Cloud Storage in the project's IAM policy
    # (configured via the auditConfigs section of the policy)
    gcloud projects get-iam-policy my-project --format=yaml > policy.yaml
    # add auditConfigs for storage.googleapis.com, then:
    gcloud projects set-iam-policy my-project policy.yaml
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Compute Engine

36. ### What is Compute Engine in Google Cloud?

    **Compute Engine** is GCP's **Infrastructure-as-a-Service (IaaS)** offering that lets you provision virtual machines on demand. It provides:

    - **Customizable machine types** (vCPU/memory combinations).
    - **Attached storage** (Persistent Disks, Local SSDs).
    - **Networking** (VPC, load balancers, firewall rules).
    - **Accelerators** (GPUs, TPUs) and **autoscaling**.

    You create VMs via Console, `gcloud`, Terraform, or REST APIs and connect them to VPCs and other services.

    ```bash
    gcloud compute instances create app-server \
        --zone=us-central1-a \
        --machine-type=e2-standard-2 \
        --image-family=debian-12 --image-project=debian-cloud \
        --tags=web
    ```

    **[⬆ Back to Top](#table-of-contents)**

37. ### What is a VM instance in Compute Engine?

    A **VM instance** is a virtual machine running on Google's infrastructure. Each instance has:

    - A **machine type** (defines vCPUs and memory).
    - A **boot disk** (from an OS image).
    - Optional **additional disks** and **network interfaces**.
    - **Metadata** (including startup scripts).

    Instances can be **standard on-demand**, **Spot** (low-cost, preemptible), and you can start/stop/restart them and manage them with startup scripts or config-management tools.

    **[⬆ Back to Top](#table-of-contents)**

38. ### What is the difference between machine families in Compute Engine?

    | Family | Examples | Best For |
    | --- | --- | --- |
    | **General-purpose** | E2, N1, N2, N2D | Web servers, microservices, balanced workloads |
    | **Compute-optimized** | C2, C3 | CPU-bound: HPC, gaming servers, video transcoding |
    | **Memory-optimized** | M1, M2, M3 | In-memory DBs, SAP HANA, large analytics |
    | **Accelerator-optimized** | A2, A3 (NVIDIA GPUs) | ML training/inference, HPC |
    | **Tau (scale-out)** | T2D, T2A (Arm) | Cost-efficient scale-out workloads |

    Each family has different **price/performance** characteristics. Choose based on your CPU, memory, network, and accelerator needs.

    **[⬆ Back to Top](#table-of-contents)**

39. ### How do you choose between general-purpose, compute-optimized and memory-optimized machines?

    Match the machine type to your **resource profile**:

    - **CPU-intensive** (video encoding, scientific computing) → **compute-optimized** (C2/C3) for higher clock speeds and larger caches.
    - **Memory-bound** (in-memory databases, big-data analytics) → **memory-optimized** (M-series) for large RAM.
    - **Balanced** (web servers, microservices, typical Java/Spring Boot backends) → **general-purpose** (E2/N2) for best cost efficiency.

    Also factor in **sustained use discounts** and **committed use discounts** when estimating cost for predictable workloads. Start small and right-size using monitoring data.

    **[⬆ Back to Top](#table-of-contents)**

40. ### What is a managed instance group?

    A **Managed Instance Group (MIG)** is a set of **identical VM instances** managed as a single entity from an **instance template**. MIGs provide:

    - **Autoscaling** based on load.
    - **Autohealing** — recreates unhealthy instances.
    - **Rolling updates** — gradual, zero-downtime deployments.
    - **Regional distribution** across multiple zones.

    MIGs integrate with load balancers and are the standard way to run resilient, scalable VM fleets.

    ```bash
    gcloud compute instance-groups managed create web-mig \
        --template=web-template --size=3 --zone=us-central1-a
    ```

    **[⬆ Back to Top](#table-of-contents)**

41. ### What is the difference between managed and unmanaged instance groups?

    | | Managed (MIG) | Unmanaged |
    | --- | --- | --- |
    | **Instances** | Identical, from a template | Arbitrary existing VMs |
    | **Autoscaling** | Yes | No |
    | **Autohealing** | Yes | No |
    | **Rolling updates** | Yes | No |
    | **Use case** | Production, scalable workloads | Legacy / heterogeneous grouping |

    **MIGs are preferred** for production because they automate scaling, healing, and updates. **Unmanaged groups** are just a collection of dissimilar VMs behind a load balancer and are rarely used today.

    **[⬆ Back to Top](#table-of-contents)**

42. ### How does autoscaling work in a managed instance group?

    The MIG **autoscaler** monitors metrics and adjusts instance count to hit a target:

    - **Metrics** — CPU utilization, load balancer request rate, or **Cloud Monitoring custom metrics**.
    - **Scale out** when metrics exceed the target threshold; **scale in** when below.
    - **Scheduled scaling** — e.g., add capacity during business hours.
    - **Predictive autoscaling** — anticipates load based on history.
    - **Cool-down periods** prevent thrashing.

    ```bash
    gcloud compute instance-groups managed set-autoscaling web-mig \
        --zone=us-central1-a \
        --max-num-replicas=10 --min-num-replicas=2 \
        --target-cpu-utilization=0.6 --cool-down-period=60
    ```

    **[⬆ Back to Top](#table-of-contents)**

43. ### What is an instance template?

    An **instance template** is a **reusable, immutable configuration** defining machine type, image, boot disk, metadata, network settings, and service account for VMs. MIGs use templates to create consistent instances.

    To change the configuration (e.g., a new image version), you **create a new template** and perform a **rolling update** — templates themselves cannot be edited.

    ```bash
    gcloud compute instance-templates create web-template-v2 \
        --machine-type=e2-standard-2 \
        --image-family=debian-12 --image-project=debian-cloud \
        --metadata-from-file=startup-script=init.sh \
        --tags=web
    ```

    **[⬆ Back to Top](#table-of-contents)**

44. ### How do you perform a rolling update in Compute Engine?

    In a MIG, a **rolling update** gradually replaces instances with ones from a new template, controlled by an **update policy**:

    - **`max-surge`** — how many extra instances can be created above the target.
    - **`max-unavailable`** — how many instances can be down at once.

    ```bash
    # Roll out a new template gradually, never dropping below capacity
    gcloud compute instance-groups managed rolling-action start-update web-mig \
        --zone=us-central1-a \
        --version=template=web-template-v2 \
        --max-surge=2 --max-unavailable=0
    ```

    Setting `max-unavailable=0` ensures new instances are healthy before old ones are removed — achieving **zero-downtime** deployments. You can also use **canary** updates by specifying a `--canary-version` for a subset of instances.

    **[⬆ Back to Top](#table-of-contents)**

45. ### What is a startup script in Compute Engine?

    A **startup script** runs automatically when a VM boots, automating configuration — installing software, updating packages, writing config files. You provide it via instance metadata (`startup-script`) or reference a script in Cloud Storage.

    ```bash
    # init.sh
    #!/bin/bash
    apt-get update
    apt-get install -y nginx
    systemctl enable nginx
    systemctl start nginx
    ```

    ```bash
    # Create a VM with the startup script
    gcloud compute instances create webserver \
        --zone=us-central1-a \
        --machine-type=e2-small \
        --metadata-from-file=startup-script=init.sh \
        --tags=web
    ```

    For Java workloads, a startup script might install the JRE, pull your JAR from a bucket, and start it as a `systemd` service.

    **[⬆ Back to Top](#table-of-contents)**

46. ### What are Shielded VMs?

    **Shielded VMs** are hardened VMs that protect against rootkits and boot-level attacks using three features:

    - **Secure Boot** — ensures the VM boots only trusted, signed bootloader and kernel images.
    - **vTPM (virtual Trusted Platform Module)** — stores cryptographic measurements used to verify boot integrity.
    - **Integrity Monitoring** — surfaces attestation events when the boot sequence changes unexpectedly.

    ```bash
    gcloud compute instances create secure-vm \
        --zone=us-central1-a \
        --shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring
    ```

    They're recommended for security-sensitive workloads and are the default for many hardened images.

    **[⬆ Back to Top](#table-of-contents)**

47. ### What are sole-tenant nodes?

    A **sole-tenant node** is a **physical Compute Engine host dedicated entirely to your organization** — no other customer's workloads share it. Use cases:

    - **Regulatory compliance** requiring hardware isolation.
    - **Bring-Your-Own-License (BYOL)** for software licensed per physical core (e.g., some Microsoft/Oracle products).
    - **Control over VM placement** for performance or licensing.

    ```bash
    gcloud compute sole-tenancy node-templates create my-node-template \
        --node-type=n2-node-80-640 --region=us-central1
    ```

    You pay for the entire physical node regardless of how many VMs you place on it.

    **[⬆ Back to Top](#table-of-contents)**

48. ### What is the difference between Persistent Disks and local SSDs?

    | | Persistent Disk | Local SSD |
    | --- | --- | --- |
    | **Attachment** | Network-attached | Physically attached to host |
    | **Durability** | Survives VM stop/restart/migration | **Lost** when VM stops or migrates |
    | **Performance** | Good, scales with size | Very high IOPS, very low latency |
    | **Snapshots** | Yes | No |
    | **Use case** | Boot disks, databases, durable data | Caching, scratch, temp data |

    **Persistent Disks** are durable block storage that persists independently of the VM and can be detached/reattached. **Local SSDs** offer extreme performance but are **ephemeral** — never store data you can't lose on them.

    **[⬆ Back to Top](#table-of-contents)**

49. ### How do snapshots work for Persistent Disks?

    A **snapshot** captures the state of a Persistent Disk at a point in time. Key properties:

    - **Incremental** — after the first full snapshot, only changed blocks are stored, saving cost and time.
    - Stored in **multi-region or regional** Cloud Storage.
    - Used to **create new disks** or **restore** data, even across zones/regions.
    - Can be **automated** via resource policies (snapshot schedules).

    ```bash
    # Create a snapshot
    gcloud compute disks snapshot data-disk \
        --zone=us-central1-a --snapshot-names=data-disk-backup

    # Schedule daily snapshots with 14-day retention
    gcloud compute resource-policies create snapshot-schedule daily-backup \
        --region=us-central1 --max-retention-days=14 \
        --daily-schedule --start-time=02:00
    ```

    **[⬆ Back to Top](#table-of-contents)**

50. ### What is the difference between Standard, Balanced, SSD and Extreme Persistent Disks?

    | Type | Backing | Performance | Best For |
    | --- | --- | --- | --- |
    | **Standard (pd-standard)** | HDD | Low IOPS, cheapest | Cold data, backups, sequential I/O |
    | **Balanced (pd-balanced)** | SSD | Good IOPS, cost-balanced | Web servers, small DBs, dev environments |
    | **SSD (pd-ssd)** | SSD | High IOPS, low latency | Transactional databases, analytics |
    | **Extreme (pd-extreme)** | SSD | Highest IOPS, provisionable | Mission-critical enterprise DBs (SAP HANA) |

    **Balanced** is the sensible default for most general workloads. **Extreme** lets you provision a specific IOPS target for the most demanding databases.

    **[⬆ Back to Top](#table-of-contents)**

51. ### What are Spot VMs?

    **Spot VMs** are deeply discounted (up to ~60–91% off) compute instances that **Google can preempt at any time** when it needs the capacity back. They:

    - Give a **30-second preemption notice**.
    - Are ideal for **fault-tolerant, interruptible** workloads.
    - Can run for an **unlimited duration** (subject to availability) — the successor to older "preemptible VMs."

    Design your app to **checkpoint work** and resume after interruption.

    ```bash
    gcloud compute instances create batch-worker \
        --zone=us-central1-a --machine-type=e2-standard-4 \
        --provisioning-model=SPOT --instance-termination-action=STOP
    ```

    **[⬆ Back to Top](#table-of-contents)**

52. ### When would you use Spot VMs in backend systems?

    Use Spot VMs for **stateless or distributed workloads that tolerate interruption**:

    - **Batch data processing** and ETL jobs.
    - **Monte Carlo / HPC simulations**.
    - **CI/CD build workers** and horizontal test runners.
    - **Rendering** and media transcoding farms.

    **Avoid** Spot VMs for databases or stateful services unless you have replication/failover. Combine them with **MIGs** using `--max-surge`/`--max-unavailable` so preempted instances are automatically replaced, dramatically cutting costs for elastic batch workloads.

    **[⬆ Back to Top](#table-of-contents)**

53. ### How do you design a highly available application using Compute Engine?

    Combine several techniques:

    - **Regional MIG** spreading instances across **multiple zones**.
    - **Global or regional load balancer** distributing traffic and detecting unhealthy instances via health checks.
    - **Regional Persistent Disks** or multi-zone databases (**Cloud SQL HA**, **Cloud Spanner**) for stateful data.
    - **Autohealing and autoscaling** for self-recovery and elasticity.
    - **Automated backups** (snapshot schedules) and a documented **DR plan**.

    ```bash
    # Regional MIG + autoscaling + health-check-based autohealing
    gcloud compute instance-groups managed create ha-mig \
        --template=web-template --size=6 --region=us-central1 \
        --health-check=web-hc --initial-delay=120

    gcloud compute instance-groups managed set-autoscaling ha-mig \
        --region=us-central1 --max-num-replicas=12 --min-num-replicas=4 \
        --target-cpu-utilization=0.6
    ```

    **[⬆ Back to Top](#table-of-contents)**


## GKE and Containers

54. ### What is Google Kubernetes Engine?

    **Google Kubernetes Engine (GKE)** is a **managed Kubernetes service** on GCP. It provisions and operates Kubernetes clusters, managing the **control plane** (API server, scheduler, etcd) and integrating with GCP networking, IAM, and monitoring. You deploy containerized workloads using Kubernetes objects (Deployments, StatefulSets, DaemonSets) and get automatic scaling, rolling updates, and service discovery.

    ```bash
    gcloud container clusters create-auto my-cluster --region=us-central1
    gcloud container clusters get-credentials my-cluster --region=us-central1
    kubectl get nodes
    ```

    **[⬆ Back to Top](#table-of-contents)**

55. ### What is the difference between GKE Standard and GKE Autopilot?

    | | GKE Standard | GKE Autopilot |
    | --- | --- | --- |
    | **Node management** | You manage node pools, machine types, upgrades | Fully managed by Google |
    | **Billing** | Per **node** (VMs), idle or busy | Per **pod** resource request (CPU/mem/disk) |
    | **Control** | Full — custom kernels, GPUs, daemonsets | Limited node customization |
    | **Ops overhead** | Higher | Lower |

    **Autopilot** removes node provisioning, upgrades, and capacity management — you just declare pod resource requests. Choose **Standard** when you need custom kernels, specific GPU configs, or node-level daemons; choose **Autopilot** for reduced operational overhead.

    **[⬆ Back to Top](#table-of-contents)**

56. ### When would you choose GKE over Cloud Run?

    Choose **GKE** when you need full Kubernetes flexibility:

    - **Stateful workloads** (StatefulSets, persistent volumes).
    - **Custom networking** (Calico, service mesh like Istio).
    - **GPU/TPU** support and advanced scheduling.
    - **Sidecars and DaemonSets** (logging agents, proxies).
    - Migrating **existing Kubernetes** workloads or using the K8s ecosystem.

    Choose **Cloud Run** for **stateless HTTP services**, event-driven workloads, and microservices that benefit from **scale-to-zero** and minimal ops. GKE = maximum control; Cloud Run = maximum simplicity.

    **[⬆ Back to Top](#table-of-contents)**

57. ### What is a GKE cluster?

    A **GKE cluster** consists of:

    - A **control plane** (managed by Google) — API server, scheduler, controller manager, etcd.
    - A **data plane** of **nodes** (Compute Engine VMs) where your pods run.

    You interact with the cluster via `kubectl` or the Cloud Console. Google handles control-plane availability, patching, and backups, while you manage your workloads.

    **[⬆ Back to Top](#table-of-contents)**

58. ### What is a node pool in GKE?

    A **node pool** is a group of nodes within a cluster that share the **same configuration** (machine type, accelerators, labels). Node pools let you:

    - Run **different workloads** on different hardware (e.g., a GPU pool for ML, a general pool for web).
    - Mix **on-demand and Spot** nodes.
    - **Scale each pool independently**.

    ```bash
    # Add a GPU node pool to an existing cluster
    gcloud container node-pools create gpu-pool \
        --cluster=my-cluster --region=us-central1 \
        --machine-type=a2-highgpu-1g --accelerator=type=nvidia-tesla-a100,count=1 \
        --num-nodes=1 --enable-autoscaling --min-nodes=0 --max-nodes=4
    ```

    **[⬆ Back to Top](#table-of-contents)**

59. ### How does GKE manage Kubernetes control plane availability?

    GKE runs the control plane in a **Google-managed project**, separate from your cluster's project, and keeps it highly available and backed up:

    - **Regional clusters** replicate the control plane across **three zones** for resilience.
    - **Zonal clusters** keep the control plane in a single zone but with automatic repairs.
    - Google handles **upgrades, patching, and scaling** of the control plane transparently.

    This means you never operate etcd or the API server yourself.

    **[⬆ Back to Top](#table-of-contents)**

60. ### What is the difference between regional and zonal GKE clusters?

    | | Zonal Cluster | Regional Cluster |
    | --- | --- | --- |
    | **Control plane** | Single zone | Replicated across 3 zones |
    | **Nodes** | One zone (or multi-zonal nodes) | Spread across zones |
    | **Availability** | Lower (zone failure = downtime) | Higher, with SLA |
    | **Cost** | Cheaper | More expensive |

    **Regional clusters** are recommended for production due to control-plane HA. **Autopilot clusters are regional by default.** Zonal clusters suit dev/test where cost matters more than uptime.

    **[⬆ Back to Top](#table-of-contents)**

61. ### What are Kubernetes pods, deployments, services and ingress resources?

    | Object | Purpose |
    | --- | --- |
    | **Pod** | Smallest deployable unit; one or more containers sharing network and storage |
    | **Deployment** | Manages stateless pod replicas; handles updates, scaling, rollback |
    | **Service** | Stable network endpoint (ClusterIP/NodePort/LoadBalancer) for a set of pods |
    | **Ingress** | HTTP(S) layer-7 routing and TLS termination, backed by Cloud Load Balancing |

    ```yaml
    apiVersion: apps/v1
    kind: Deployment
    metadata:
      name: order-api
    spec:
      replicas: 3
      selector:
        matchLabels: { app: order-api }
      template:
        metadata:
          labels: { app: order-api }
        spec:
          containers:
          - name: order-api
            image: us-central1-docker.pkg.dev/my-project/repo/order-api:v1
            ports:
            - containerPort: 8080
    ```

    **[⬆ Back to Top](#table-of-contents)**

62. ### How does horizontal pod autoscaling work in GKE?

    The **Horizontal Pod Autoscaler (HPA)** monitors a metric (CPU, memory, or custom/Prometheus metrics) and adjusts the **number of pod replicas** to maintain a target utilization. It uses an averaging period and stabilization window to avoid thrashing.

    ```yaml
    apiVersion: autoscaling/v2
    kind: HorizontalPodAutoscaler
    metadata:
      name: order-api-hpa
    spec:
      scaleTargetRef:
        apiVersion: apps/v1
        kind: Deployment
        name: order-api
      minReplicas: 2
      maxReplicas: 10
      metrics:
      - type: Resource
        resource:
          name: cpu
          target: { type: Utilization, averageUtilization: 60 }
    ```

    Here HPA keeps average CPU near 60%, scaling between 2 and 10 replicas.

    **[⬆ Back to Top](#table-of-contents)**

63. ### How does cluster autoscaling work in GKE?

    **Cluster Autoscaler** adjusts the **number of nodes** based on pod scheduling:

    - If a pod **can't schedule** due to insufficient resources, it **adds nodes** to a node pool.
    - If nodes are **underutilized** and pods can be consolidated elsewhere, it **removes nodes**.

    It works with both Standard (you see the nodes) and Autopilot (nodes hidden). Combined with HPA: HPA adds pods → if no room, cluster autoscaler adds nodes.

    ```bash
    gcloud container clusters update my-cluster --region=us-central1 \
        --enable-autoscaling --node-pool=default-pool --min-nodes=1 --max-nodes=10
    ```

    **[⬆ Back to Top](#table-of-contents)**

64. ### What is the difference between HPA, VPA and cluster autoscaler?

    | Autoscaler | Scales | Operates On |
    | --- | --- | --- |
    | **HPA (Horizontal Pod Autoscaler)** | Number of pod replicas | Workload |
    | **VPA (Vertical Pod Autoscaler)** | Pod CPU/memory requests & limits (right-sizing) | Workload |
    | **Cluster Autoscaler** | Number of nodes | Infrastructure |

    **HPA** scales out/in horizontally. **VPA** resizes individual pods (on restart or in-place). **Cluster Autoscaler** adds/removes nodes. HPA + Cluster Autoscaler is the common combo; VPA is used when load is hard to parallelize. Note: HPA and VPA on the same metric (CPU) can conflict.

    **[⬆ Back to Top](#table-of-contents)**

65. ### What is Workload Identity in GKE?

    **Workload Identity** links a **Kubernetes service account (KSA)** to a **Google Cloud service account (GSA)**. Pods authenticate to GCP services using the KSA token, which is exchanged for Google access tokens — **no JSON key files mounted in pods**. It's the recommended, most secure way for GKE workloads to access GCP APIs and is enabled by default on Autopilot.

    ```bash
    # Bind a KSA to a GSA
    gcloud iam service-accounts add-iam-policy-binding \
        order-gsa@my-project.iam.gserviceaccount.com \
        --role=roles/iam.workloadIdentityUser \
        --member="serviceAccount:my-project.svc.id.goog[default/order-ksa]"

    kubectl annotate serviceaccount order-ksa \
        iam.gke.io/gcp-service-account=order-gsa@my-project.iam.gserviceaccount.com
    ```

    **[⬆ Back to Top](#table-of-contents)**

66. ### How does Workload Identity improve security compared to node service accounts?

    Without Workload Identity, **all pods on a node inherit the node's service account**, which often has broad permissions — any compromised pod gets that access. Workload Identity instead:

    - Gives **each pod its own GSA** with least-privilege permissions.
    - Provides **short-lived credentials** from Google's metadata server.
    - **Eliminates key files**, reducing leak risk.
    - **Prevents pods from impersonating each other**.

    This isolates blast radius per workload rather than per node.

    **[⬆ Back to Top](#table-of-contents)**

67. ### What is a Kubernetes service account?

    A **Kubernetes service account (KSA)** is an identity for **processes running in pods**. It provides a JWT that pods use to authenticate to the **Kubernetes API**. You assign a KSA to a workload via the pod's `serviceAccountName` field. With **Workload Identity**, the KSA is bound to a Google service account so the pod can also call GCP APIs.

    ```yaml
    apiVersion: v1
    kind: ServiceAccount
    metadata:
      name: order-ksa
    ---
    apiVersion: apps/v1
    kind: Deployment
    spec:
      template:
        spec:
          serviceAccountName: order-ksa   # pod uses this identity
    ```

    **[⬆ Back to Top](#table-of-contents)**

68. ### How do you expose a GKE workload to the internet?

    Several options:

    - **Service of type `LoadBalancer`** — GKE provisions an external L4 load balancer with a public IP.
    - **Ingress** — define HTTP(S) routing rules and TLS certificates; GKE provisions an HTTP(S) load balancer with URL maps.
    - **Internal load balancer** — for internal-only access (annotation `networking.gke.io/load-balancer-type: "Internal"`).

    ```yaml
    apiVersion: v1
    kind: Service
    metadata:
      name: order-api-svc
    spec:
      type: LoadBalancer
      selector: { app: order-api }
      ports:
      - port: 80
        targetPort: 8080
    ```

    **[⬆ Back to Top](#table-of-contents)**

69. ### What is the difference between ClusterIP, NodePort, LoadBalancer and Ingress?

    | Type | Exposure | Use Case |
    | --- | --- | --- |
    | **ClusterIP** | Internal virtual IP, cluster-only | Internal service-to-service |
    | **NodePort** | Static port on each node's IP | Basic external access, dev |
    | **LoadBalancer** | Cloud LB with public/internal IP | Production external L4 access |
    | **Ingress** | HTTP(S) LB with routing & TLS | L7 path/host routing, single entry point |

    **ClusterIP** is the default. **Ingress** is the most powerful for HTTP apps, supporting host/path-based routing, TLS termination, and a single load balancer for many services (cost-efficient).

    **[⬆ Back to Top](#table-of-contents)**

70. ### How does GKE integrate with Cloud Load Balancing?

    When you create a `LoadBalancer` Service or an **Ingress**, the GKE controller automatically provisions **Cloud Load Balancing** resources:

    - For **Ingress** → a global **HTTP(S) Load Balancer** with URL maps, backend services, health checks, and managed SSL certs.
    - Backends point to **Network Endpoint Groups (NEGs)** — container-native load balancing routes traffic directly to pod IPs (skipping the node hop) for better performance.

    Health checks, SSL certificates, and URL maps are managed by the controller, so you declare intent in YAML and GKE handles the cloud plumbing.

    **[⬆ Back to Top](#table-of-contents)**

71. ### What is a readiness probe?

    A **readiness probe** checks whether a container is **ready to serve traffic**. If it fails, Kubernetes **removes the pod from Service endpoints** (no traffic) **without restarting** it. Readiness probes are essential for workloads that need warm-up time or must wait for dependencies (e.g., a DB connection pool).

    ```yaml
    readinessProbe:
      httpGet:
        path: /actuator/health/readiness   # Spring Boot Actuator
        port: 8080
      initialDelaySeconds: 10
      periodSeconds: 5
    ```

    **[⬆ Back to Top](#table-of-contents)**

72. ### What is a liveness probe?

    A **liveness probe** checks whether a container is **healthy / alive**. If it fails, Kubernetes **restarts the container**. Use it to detect deadlocks or hung processes that a restart can fix. Probes can be HTTP, TCP, or exec-based and run periodically after an initial delay.

    ```yaml
    livenessProbe:
      httpGet:
        path: /actuator/health/liveness
        port: 8080
      initialDelaySeconds: 30
      periodSeconds: 10
      failureThreshold: 3
    ```

    **Caution:** an overly aggressive liveness probe can cause restart loops; tune `initialDelaySeconds` and `failureThreshold` for slow-starting apps.

    **[⬆ Back to Top](#table-of-contents)**

73. ### What is a startup probe?

    A **startup probe** runs **during application startup** and **supersedes liveness and readiness checks until it succeeds**. It's ideal for containers with **long initialization** (e.g., a JVM loading a large context), preventing the liveness probe from prematurely killing a slow-starting container.

    ```yaml
    startupProbe:
      httpGet:
        path: /actuator/health
        port: 8080
      failureThreshold: 30   # allow up to 30 * 10s = 5 min to start
      periodSeconds: 10
    ```

    Once the startup probe passes, liveness and readiness probes take over.

    **[⬆ Back to Top](#table-of-contents)**

74. ### How do you perform zero-downtime deployments in GKE?

    - Use **Deployments** with **rolling updates** configured via `maxSurge` and `maxUnavailable`.
    - Set `maxUnavailable: 0` and `maxSurge: 25%` so new pods start before old ones terminate.
    - Define **readiness probes** so traffic only goes to healthy pods.
    - For stateful apps or risky changes, use **blue-green** or **canary** strategies (Argo Rollouts, Cloud Deploy).

    ```yaml
    spec:
      strategy:
        type: RollingUpdate
        rollingUpdate:
          maxSurge: 25%
          maxUnavailable: 0
    ```

    **[⬆ Back to Top](#table-of-contents)**

75. ### What is a rolling update in Kubernetes?

    A **rolling update** gradually replaces old pod replicas with new ones. The Deployment controller creates new pods from the updated template while scaling down old pods, controlled by:

    - **`maxSurge`** — extra pods allowed above desired count.
    - **`maxUnavailable`** — pods allowed to be unavailable during the update.

    This **minimizes downtime** and supports **rollback** to the previous revision.

    ```bash
    # Trigger and monitor a rolling update
    kubectl set image deployment/order-api order-api=...:v2
    kubectl rollout status deployment/order-api
    kubectl rollout undo deployment/order-api   # rollback if needed
    ```

    **[⬆ Back to Top](#table-of-contents)**

76. ### What is a blue-green deployment in GKE?

    **Blue-green deployment** runs the **new version (green)** alongside the **old version (blue)**. After verifying green, you **switch all traffic** from blue to green at once (e.g., by changing a Service selector or Ingress backend). If something's wrong, you switch back instantly.

    ```yaml
    # Service initially points to blue; flip selector to green after validation
    apiVersion: v1
    kind: Service
    metadata: { name: order-api-svc }
    spec:
      selector:
        app: order-api
        version: green   # was "blue"
    ```

    Pros: instant rollback, no mixed versions. Cons: requires double the resources during cutover.

    **[⬆ Back to Top](#table-of-contents)**

77. ### What is a canary deployment in GKE?

    A **canary deployment** routes a **small percentage of traffic** to the new version first. If metrics look healthy, you gradually increase the share until 100%, then retire the old version. This limits the blast radius of a bad release.

    Implement with weighted routing via **Cloud Deploy**, **Argo Rollouts**, or a service mesh (Istio). A simple GKE approach runs a small number of canary pods behind the same Service so a fraction of requests hit the new version.

    ```yaml
    # 1 canary pod alongside 9 stable pods ≈ 10% canary traffic
    # stable Deployment: replicas: 9 (version: v1)
    # canary Deployment: replicas: 1 (version: v2), same Service selector
    ```

    **[⬆ Back to Top](#table-of-contents)**

78. ### How do you troubleshoot a pod stuck in CrashLoopBackOff?

    `CrashLoopBackOff` means a container repeatedly starts and crashes. Diagnose systematically:

    1. **Check logs** — `kubectl logs <pod> --previous` to see the crash output from the last run.
    2. **Describe the pod** — `kubectl describe pod <pod>` for events, exit codes, probe failures.
    3. **Common causes** — missing config/secrets, failing dependencies, insufficient resources (OOMKilled), bad command, or failing health probes.
    4. **Fix** — correct env vars/secrets, adjust resource requests/limits, fix the startup command, relax probes.
    5. **Debug interactively** — `kubectl run -it debug --image=<your-image> -- bash` to inspect the image.

    ```bash
    kubectl logs order-api-xyz --previous
    kubectl describe pod order-api-xyz
    kubectl get events --sort-by=.lastTimestamp
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Cloud Run and Serverless

79. ### What is Cloud Run?

    **Cloud Run** is a fully managed **serverless platform for running stateless containers**. You package your app as a container image, deploy it, and Cloud Run automatically handles provisioning, **scaling (including to zero)**, load balancing, and HTTPS. You pay only for CPU, memory, and requests **while your code is running**.

    ```bash
    gcloud run deploy order-api \
        --image=us-central1-docker.pkg.dev/my-project/repo/order-api:v1 \
        --region=us-central1 --platform=managed --allow-unauthenticated
    ```

    Any language works as long as it's containerized and listens on the port from the `PORT` env var.

    **[⬆ Back to Top](#table-of-contents)**

80. ### How is Cloud Run different from App Engine?

    | | App Engine | Cloud Run |
    | --- | --- | --- |
    | **Model** | PaaS, language-specific runtimes | Container-based serverless |
    | **Flexibility** | Runtime constraints | Any language/runtime via container |
    | **Scale to zero** | Standard: yes; Flexible: no | Yes |
    | **Portability** | GCP-specific | Containers run anywhere (built on Knative) |

    **App Engine Standard** runs in sandboxed language runtimes with constraints (read-only FS). **Cloud Run** gives you full container flexibility with per-request scale-to-zero and supports background work while a request is open. Cloud Run is the modern successor for most new serverless workloads.

    **[⬆ Back to Top](#table-of-contents)**

81. ### How is Cloud Run different from Cloud Functions?

    | | Cloud Functions | Cloud Run |
    | --- | --- | --- |
    | **Unit** | Single-purpose function | Full container |
    | **Trigger** | Events (HTTP, Pub/Sub, GCS) | HTTP, events (via Eventarc) |
    | **Concurrency** | One request per instance (Gen 1) | Multiple concurrent requests (default 80) |
    | **Runtime** | Fixed language runtimes | Any container |
    | **Max duration** | Shorter | Up to 60 minutes |

    **Cloud Functions** is great for small event handlers and glue code. **Cloud Run** is better for microservices, web APIs, and containerized apps needing concurrency and longer execution. (Note: Cloud Functions 2nd gen is actually built on Cloud Run.)

    **[⬆ Back to Top](#table-of-contents)**

82. ### When would you choose Cloud Run for a backend service?

    Choose Cloud Run when you want to:

    - Deploy **stateless HTTP services** (REST/GraphQL APIs, webhooks) quickly.
    - **Scale to zero** to save cost during idle periods.
    - **Avoid managing infrastructure** (no clusters, no nodes).
    - Run **any language/runtime** via a container.
    - Integrate easily with other GCP services, custom domains, and private connectivity.

    Ideal for microservices, event-driven processing (Cloud Scheduler + Pub/Sub), and APIs with variable traffic. A Spring Boot JAR containerized into Cloud Run is a very common pattern.

    **[⬆ Back to Top](#table-of-contents)**

83. ### What is container-based serverless?

    **Container-based serverless** means running **containers** on a serverless platform — you supply the image, and the platform handles provisioning, scaling, and usage-based billing. Cloud Run implements this by running each container instance in a secure **microVM (gVisor sandbox)**, scaling from **zero to N** based on concurrency.

    It combines the **portability of containers** (any language, runs anywhere) with the **operational simplicity of serverless** (no servers to manage, pay-per-use).

    **[⬆ Back to Top](#table-of-contents)**

84. ### How does autoscaling work in Cloud Run?

    Cloud Run uses a **concurrency-aware autoscaler** that scales container instances based on **incoming request volume and concurrency settings**:

    - Monitors **request queue length and CPU utilization**.
    - **Scales up** during traffic spikes, **scales down to zero** when idle.
    - You configure **max concurrency** (requests per instance) and **min/max instances**.

    ```bash
    gcloud run deploy order-api \
        --image=...:v1 --region=us-central1 \
        --concurrency=80 --min-instances=0 --max-instances=100
    ```

    Higher concurrency means fewer instances for the same traffic, lowering cost.

    **[⬆ Back to Top](#table-of-contents)**

85. ### What is scale-to-zero in Cloud Run?

    **Scale-to-zero** means Cloud Run **terminates all container instances when there are no incoming requests** — zero running compute, zero compute cost during idle periods. You're billed only for requests served. When a new request arrives, Cloud Run starts a fresh instance, which may incur a **cold start**.

    This is a key serverless cost advantage, perfect for spiky or low-traffic workloads. For latency-sensitive services, set **minimum instances** to keep some warm.

    **[⬆ Back to Top](#table-of-contents)**

86. ### What is a cold start in Cloud Run?

    A **cold start** happens when a request arrives but **no instance exists**, so Cloud Run must:

    1. Spin up a new container.
    2. Pull the image (if not cached).
    3. Initialize your application.
    4. Handle the request.

    Cold-start latency depends on **image size** and **startup time**. JVM apps (Spring Boot) can have noticeable cold starts due to class loading and context initialization — mitigations include smaller images, lazy initialization, and minimum instances.

    **[⬆ Back to Top](#table-of-contents)**

87. ### How can you reduce cold starts in Cloud Run?

    - **Minimum instances** — keep 1–2 warm instances always running (`--min-instances=1`) to eliminate most cold starts.
    - **Smaller images** — use slim base images (e.g., `eclipse-temurin:21-jre-alpine`) and few layers to cut image-pull time.
    - **Fast startup** — lazy-load non-critical modules; for Spring Boot, enable lazy initialization (`spring.main.lazy-initialization=true`) or consider **GraalVM native images**.
    - **Higher concurrency** — serve more requests per instance to reduce how often new instances spin up.
    - **Startup CPU boost** — `--cpu-boost` allocates extra CPU during startup.

    ```bash
    gcloud run deploy order-api --image=...:v1 --region=us-central1 \
        --min-instances=1 --cpu-boost --concurrency=80
    ```

    **[⬆ Back to Top](#table-of-contents)**

88. ### What is concurrency in Cloud Run?

    **Concurrency** is the **maximum number of simultaneous requests a single instance can handle** (default **80**). Tuning it trades cost against per-request performance:

    - **Higher concurrency** → fewer instances needed → lower cost, but risks latency if the app can't handle many parallel requests.
    - **Lower concurrency** (e.g., 1) → request isolation → more instances → higher cost.

    Set concurrency based on your app's **throughput and memory** profile. A well-tuned async Java service can comfortably handle high concurrency.

    ```bash
    gcloud run deploy order-api --concurrency=40 ...
    ```

    **[⬆ Back to Top](#table-of-contents)**

89. ### How do CPU allocation settings affect Cloud Run performance?

    Cloud Run offers two **CPU allocation** models:

    | Mode | CPU Allocated | Cost | Use Case |
    | --- | --- | --- | --- |
    | **CPU only during requests** (default) | Only while processing a request | Lower | Pure request/response services |
    | **CPU always allocated** | Throughout instance lifetime | Higher | Background tasks, cache warming, async work |

    With the default, background threads pause between requests. Use **always-on CPU** when you need to process work between requests (e.g., batching, pre-warming, async event consumers).

    ```bash
    gcloud run deploy worker --no-cpu-throttling ...   # CPU always allocated
    ```

    **[⬆ Back to Top](#table-of-contents)**

90. ### How do you secure a Cloud Run service?

    - **Ingress control** — set `--ingress=internal` or `internal-and-cloud-load-balancing` to restrict traffic to VPC/LB sources.
    - **Authentication** — require IAM-authenticated invocations; or use **Identity-Aware Proxy (IAP)** / API Gateway for user auth.
    - **IAM roles** — grant only specific principals `roles/run.invoker`.
    - **HTTPS** — automatic TLS, including for custom domains.
    - **Private connectivity** — use **Serverless VPC Access** to reach private resources.

    ```bash
    # Remove public access and grant invoke to a specific service account only
    gcloud run services remove-iam-policy-binding order-api \
        --member=allUsers --role=roles/run.invoker --region=us-central1
    gcloud run services add-iam-policy-binding order-api \
        --member="serviceAccount:gateway@my-project.iam.gserviceaccount.com" \
        --role=roles/run.invoker --region=us-central1
    ```

    **[⬆ Back to Top](#table-of-contents)**

91. ### How do you make a Cloud Run service private?

    1. Set ingress to internal: `--ingress=internal` (or `internal-and-cloud-load-balancing`).
    2. Create a **Serverless VPC Access connector** and route traffic through it.
    3. **Remove public IAM bindings** — no `allUsers` or `allAuthenticatedUsers`.
    4. Grant `roles/run.invoker` only to **specific principals**.

    ```bash
    gcloud run deploy internal-api --image=...:v1 --region=us-central1 \
        --ingress=internal --no-allow-unauthenticated \
        --vpc-connector=my-connector
    ```

    Now only callers inside your VPC (and authorized identities) can reach the service.

    **[⬆ Back to Top](#table-of-contents)**

92. ### How do you connect Cloud Run to a VPC?

    Use **Serverless VPC Access**. Create a **VPC access connector** in your project/region, then attach it to the service with `--vpc-connector`. This lets Cloud Run instances send traffic **into your VPC** to reach private resources like Cloud SQL (private IP), Memorystore, or internal services.

    ```bash
    # Create a connector
    gcloud compute networks vpc-access connectors create my-connector \
        --region=us-central1 --network=default --range=10.8.0.0/28

    # Attach it to the Cloud Run service
    gcloud run deploy order-api --image=...:v1 --region=us-central1 \
        --vpc-connector=my-connector --vpc-egress=private-ranges-only
    ```

    **[⬆ Back to Top](#table-of-contents)**

93. ### What is Serverless VPC Access?

    **Serverless VPC Access** is a managed service that lets **serverless products** (Cloud Run, Cloud Functions, App Engine Standard) connect to resources in a **VPC via internal IP**. It provisions an elastic fleet of **proxy VMs** that bridge serverless instances to your VPC subnets, with NAT for traffic flow.

    This enables serverless apps to securely reach **private databases, caches, and internal APIs** without exposing them publicly.

    **[⬆ Back to Top](#table-of-contents)**

94. ### How can Cloud Run access Cloud SQL privately?

    1. Create a **Cloud SQL instance with private IP** enabled.
    2. Provision a **Serverless VPC Access connector** in the same region.
    3. Deploy Cloud Run with `--vpc-connector` and `--vpc-egress=all` (or private-ranges) to route DB traffic through the connector.
    4. Connect using the private IP or Cloud SQL connection name.

    ```bash
    gcloud run deploy order-api --image=...:v1 --region=us-central1 \
        --vpc-connector=my-connector --vpc-egress=all \
        --add-cloudsql-instances=my-project:us-central1:orders-db \
        --set-env-vars=DB_HOST=10.x.x.x,DB_NAME=orders
    ```

    ```java
    // Spring Boot datasource pointing at the private IP via the connector
    // application.properties:
    // spring.datasource.url=jdbc:postgresql://10.x.x.x:5432/orders
    ```

    **[⬆ Back to Top](#table-of-contents)**

95. ### What is Cloud Functions?

    **Cloud Functions** is an **event-driven serverless compute** platform that runs small, single-purpose functions in response to events — HTTP requests, Pub/Sub messages, Cloud Storage changes, Firestore updates, etc. Functions **scale automatically**, run in managed runtimes, and bill per **execution time, memory, and invocation count**. Ideal for glue code, data-processing triggers, and lightweight APIs.

    ```java
    // Java HTTP Cloud Function (Functions Framework)
    public class HelloWorld implements HttpFunction {
        @Override
        public void service(HttpRequest request, HttpResponse response) throws Exception {
            response.getWriter().write("Hello from Cloud Functions");
        }
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

96. ### What are event-driven Cloud Functions?

    **Event-driven functions** trigger automatically on events from GCP services rather than HTTP. Examples:

    - A **Cloud Storage** object-finalize event triggers a function to generate a thumbnail.
    - A **Pub/Sub** message triggers a function to process an event.
    - A **Firestore** document write triggers downstream logic.

    You specify the event type and resource at deploy time; the platform invokes your code when matching events occur.

    ```bash
    gcloud functions deploy thumbnailGenerator \
        --gen2 --runtime=java21 --region=us-central1 \
        --trigger-event-filters="type=google.cloud.storage.object.v1.finalized" \
        --trigger-event-filters="bucket=my-uploads" \
        --entry-point=com.example.ThumbnailFunction
    ```

    **[⬆ Back to Top](#table-of-contents)**

97. ### What is App Engine Standard?

    **App Engine Standard** runs apps in **language-specific sandboxed runtimes** (Java, Python, Go, Node.js) with **automatic scaling, versioning, and zero server management**. It can **scale to zero** and bills per usage. The sandbox imposes restrictions (read-only file system, limited network/syscalls). It suits PaaS workloads where you accept runtime constraints for operational simplicity.

    ```yaml
    # app.yaml for a Java app
    runtime: java21
    instance_class: F2
    automatic_scaling:
      min_instances: 0
      max_instances: 10
    ```

    **[⬆ Back to Top](#table-of-contents)**

98. ### What is App Engine Flexible?

    **App Engine Flexible** runs your app in a **container on Compute Engine VMs** managed by Google. You can supply a custom Dockerfile or use language runtimes. It offers more control (write access to disk, custom packages, background processing) but instances are **longer-lived** — it does **not** scale to zero and runs at least a minimum number of instances. Use it when you need custom system packages or background work that the Standard sandbox can't accommodate.

    | | Standard | Flexible |
    | --- | --- | --- |
    | **Runtime** | Sandboxed | Container on VMs |
    | **Scale to zero** | Yes | No (min instances) |
    | **Customization** | Limited | High (custom Docker) |
    | **Startup** | Fast | Slower (VM-based) |

    **[⬆ Back to Top](#table-of-contents)**


## Cloud Storage and File Storage

99. ### What is Cloud Storage?

    **Cloud Storage** is GCP's **object storage** service for unstructured data (files, images, backups, videos). You create **buckets** (in a region or multi-region) and store **objects** within them. It offers:

    - **11 nines (99.999999999%) durability** and high availability.
    - **Storage classes** (Standard, Nearline, Coldline, Archive) for cost/access trade-offs.
    - Features like **lifecycle policies, versioning, signed URLs, and retention**.

    ```java
    // Upload an object with the Java client library
    Storage storage = StorageOptions.getDefaultInstance().getService();
    BlobInfo blob = BlobInfo.newBuilder("my-bucket", "report.pdf")
        .setContentType("application/pdf").build();
    storage.create(blob, Files.readAllBytes(Paths.get("report.pdf")));
    ```

    **[⬆ Back to Top](#table-of-contents)**

100. ### What is the difference between object storage and block storage?

     | | Object Storage (Cloud Storage) | Block Storage (Persistent Disk) |
     | --- | --- | --- |
     | **Structure** | Objects + metadata, flat namespace | Fixed-size blocks, appears as a disk |
     | **Access** | HTTP API, key-based | Random read/write, mounted to VM |
     | **Best for** | Files, media, backups, static content | Databases, OS drives, low-latency I/O |
     | **Mutability** | Whole-object writes | In-place block updates |

     **Object storage** scales infinitely and is ideal for immutable files. **Block storage** behaves like a traditional disk for applications needing low-latency random access (databases, file systems).

     **[⬆ Back to Top](#table-of-contents)**

101. ### What is a Cloud Storage bucket?

     A **bucket** is a logical container for objects. Each bucket has:

     - A **globally unique name**.
     - A **location** (region or multi-region).
     - A **default storage class**.
     - **Access control** (IAM, optionally ACLs) and optional **retention policy**.

     Buckets can host static websites, store logs, or serve as backup targets.

     ```bash
     gcloud storage buckets create gs://my-unique-bucket-name \
         --location=us-central1 --default-storage-class=STANDARD \
         --uniform-bucket-level-access
     ```

     **[⬆ Back to Top](#table-of-contents)**

102. ### What are Cloud Storage storage classes?

     | Class | Availability | Min Storage Duration | Best For |
     | --- | --- | --- | --- |
     | **Standard** | Highest | None | Frequently accessed data, websites |
     | **Nearline** | High | 30 days | Accessed < once/month, backups |
     | **Coldline** | High | 90 days | Accessed < once/quarter |
     | **Archive** | High | 365 days | Long-term archival, compliance |

     As you move from Standard → Archive, **storage cost drops** but **retrieval cost and minimum-duration fees rise**. Objects can be transitioned automatically between classes using **lifecycle rules**.

     **[⬆ Back to Top](#table-of-contents)**

103. ### How do you choose between Standard, Nearline, Coldline and Archive storage?

     Decide based on **access frequency** and **retrieval needs**:

     - **Standard** — active data: web assets, logs, content being served.
     - **Nearline** — accessed roughly **monthly**: backups, longer-tail content.
     - **Coldline** — accessed roughly **quarterly**: infrequent backups.
     - **Archive** — accessed **yearly or less**: compliance archives, disaster-recovery copies.

     Also weigh **retrieval costs** and **minimum storage durations** (Coldline 90 days, Archive 365 days) — deleting early incurs fees. Use **lifecycle rules** to transition data as it ages.

     **[⬆ Back to Top](#table-of-contents)**

104. ### What is object versioning in Cloud Storage?

     **Object versioning** keeps **multiple versions** of an object. When enabled, overwriting or deleting an object doesn't permanently remove the prior version — it becomes a **noncurrent version** you can list, restore, or permanently delete. This protects against **accidental deletion or overwrite**.

     ```bash
     gcloud storage buckets update gs://my-bucket --versioning
     # List all versions including noncurrent
     gcloud storage ls -a gs://my-bucket/important.json
     ```

     Combine with lifecycle rules to auto-delete old versions after N days to control cost.

     **[⬆ Back to Top](#table-of-contents)**

105. ### What is lifecycle management in Cloud Storage?

     **Lifecycle rules** automatically **transition or delete** objects based on conditions like age, name prefix, or version state. Examples: move objects older than 30 days to Nearline, delete objects older than 365 days, or delete noncurrent versions after 7 days. This optimizes cost and cleans up stale data without manual effort.

     ```json
     {
       "rule": [
         { "action": {"type": "SetStorageClass", "storageClass": "NEARLINE"},
           "condition": {"age": 30} },
         { "action": {"type": "Delete"},
           "condition": {"age": 365} }
       ]
     }
     ```

     ```bash
     gcloud storage buckets update gs://my-bucket --lifecycle-file=lifecycle.json
     ```

     **[⬆ Back to Top](#table-of-contents)**

106. ### How do signed URLs work in Cloud Storage?

     A **signed URL** grants **temporary, time-limited access** to a private object without requiring the caller to have GCP credentials. You sign the URL with a service account's private key, specifying the HTTP method, path, and expiration. Anyone with the URL can use it until it expires — perfect for letting users **upload or download** specific objects.

     ```java
     // Generate a V4 signed URL valid for 15 minutes (download)
     Storage storage = StorageOptions.getDefaultInstance().getService();
     BlobInfo blob = BlobInfo.newBuilder(BlobId.of("my-bucket", "report.pdf")).build();
     URL url = storage.signUrl(blob, 15, TimeUnit.MINUTES,
         Storage.SignUrlOption.withV4Signature());
     System.out.println("Download URL: " + url);
     ```

     **[⬆ Back to Top](#table-of-contents)**

107. ### What is uniform bucket-level access?

     **Uniform bucket-level access (UBLA)** simplifies access control by **disabling object-level ACLs** and relying solely on **IAM at the bucket level**. When enabled, object ACLs are ignored and IAM roles (e.g., `roles/storage.objectViewer`) govern all read/write access. UBLA reduces complexity, prevents accidental public exposure via stray ACLs, and is the **recommended** setting for most buckets.

     ```bash
     gcloud storage buckets update gs://my-bucket --uniform-bucket-level-access
     ```

     **[⬆ Back to Top](#table-of-contents)**

108. ### How is Cloud Storage secured using IAM?

     IAM controls who can **list, read, or write** objects via roles granted at the bucket or project level:

     | Role | Allows |
     | --- | --- |
     | `roles/storage.admin` | Full control of buckets and objects |
     | `roles/storage.objectAdmin` | Manage objects (read/write/delete) |
     | `roles/storage.objectCreator` | Create objects only |
     | `roles/storage.objectViewer` | Read objects |

     Combined with **UBLA**, IAM provides a single, consistent way to manage access. Apply **least privilege** — e.g., give an upload service only `objectCreator`, not `admin`.

     ```bash
     gcloud storage buckets add-iam-policy-binding gs://my-bucket \
         --member="serviceAccount:uploader@my-project.iam.gserviceaccount.com" \
         --role="roles/storage.objectCreator"
     ```

     **[⬆ Back to Top](#table-of-contents)**

109. ### What is the difference between bucket-level IAM and object ACLs?

     | | Bucket-level IAM | Object ACLs |
     | --- | --- | --- |
     | **Scope** | All objects in the bucket | Per-object permissions |
     | **Granularity** | Coarse, consistent | Fine, object-specific |
     | **Management** | Simple, scalable | Error-prone at scale |
     | **Status** | Recommended | Legacy; disabled by UBLA |

     **Bucket-level IAM** applies uniformly to all objects and is easier to audit. **Object ACLs** allow per-object exceptions (e.g., one public image in a private bucket) but are hard to manage safely. Enabling **UBLA** disables ACLs entirely, leaving IAM as the sole mechanism. Use ACLs only when truly necessary.

     **[⬆ Back to Top](#table-of-contents)**

110. ### What is a retention policy in Cloud Storage?

     A **retention policy** prevents objects from being **deleted or overwritten until a specified period elapses** (e.g., 30 days). Once **locked**, the policy cannot be reduced or removed — supporting compliance requirements that mandate data immutability for a minimum period.

     ```bash
     # Set a 30-day retention policy, then optionally lock it
     gcloud storage buckets update gs://compliance-bucket --retention-period=30d
     gcloud storage buckets update gs://compliance-bucket --lock-retention-period
     ```

     **[⬆ Back to Top](#table-of-contents)**

111. ### What is object lock in Cloud Storage?

     **Object lock** provides **WORM (Write Once, Read Many)** semantics at the **individual object level**. You can set a **retention period** and **legal hold** on specific objects, preventing deletion or modification until the hold is released or the period expires. It's used for regulatory compliance (financial records, audit data) where individual objects must be tamper-proof.

     This differs from a bucket retention policy in that it targets **specific objects** rather than the whole bucket.

     **[⬆ Back to Top](#table-of-contents)**

112. ### What is Filestore?

     **Filestore** is a managed **Network Attached Storage (NAS)** service providing **file shares over NFS**. It offers tiers (Basic, Zonal, Regional, Enterprise) with different performance and availability. Filestore is ideal for workloads needing a **shared POSIX file system** — content management, media processing, HPC, and lift-and-shift apps that expect a mounted file share.

     ```bash
     gcloud filestore instances create my-fileshare \
         --zone=us-central1-a --tier=BASIC_SSD \
         --file-share=name=share1,capacity=1TB \
         --network=name=default
     ```

     **[⬆ Back to Top](#table-of-contents)**

113. ### When would you use Filestore instead of Cloud Storage?

     Use **Filestore** when your application needs:

     - **POSIX file semantics** — directory structures, file locking, partial writes, atomic renames.
     - A **shared file system** mounted by multiple VMs or GKE pods simultaneously (NFS).
     - **Consistent low-latency** I/O.

     Use **Cloud Storage** for static files, large objects, backups, and web content where object semantics suffice. Rule of thumb: if your code does `open()/read()/write()` on a mounted path and needs concurrent shared access → Filestore; if it uploads/downloads whole objects via API → Cloud Storage.

     **[⬆ Back to Top](#table-of-contents)**

114. ### What is Cloud Storage FUSE?

     **Cloud Storage FUSE** is an open-source adapter that **mounts a Cloud Storage bucket as a local file system**, letting applications read/write objects via file operations. However, it **does not provide full POSIX semantics** — e.g., renames are non-atomic and there's no file locking. Use it for **simple integrations** (e.g., ML training jobs reading data); for high-throughput or heavily POSIX-dependent workloads, prefer **Filestore**.

     ```bash
     gcsfuse my-bucket /mnt/gcs   # mount the bucket at /mnt/gcs
     ```

     **[⬆ Back to Top](#table-of-contents)**

115. ### How do you design a secure file upload system using Cloud Storage?

     A robust, secure design:

     - **Signed URLs** — generate them server-side so clients **upload directly to the bucket**, keeping file bytes off your app servers.
     - **Naming conventions** — prefix object names with a user ID or UUID to prevent collisions and **path traversal**.
     - **Validation** — use IAM conditions or a Cloud Functions/Eventarc trigger to validate **file type and size** after upload.
     - **Quarantine bucket** — upload to a separate bucket with versioning and lifecycle rules; **scan content** before promoting to the main bucket.
     - **Least privilege** — the upload SA gets only `objectCreator`.

     ```java
     // Server generates a V4 signed URL for upload (PUT)
     BlobInfo blob = BlobInfo.newBuilder(BlobId.of("uploads", userId + "/" + UUID.randomUUID()))
         .setContentType("image/jpeg").build();
     URL uploadUrl = storage.signUrl(blob, 10, TimeUnit.MINUTES,
         Storage.SignUrlOption.httpMethod(HttpMethod.PUT),
         Storage.SignUrlOption.withV4Signature());
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Databases and Caching

116. ### What is Cloud SQL?

     **Cloud SQL** is a fully managed **relational database** service supporting **MySQL, PostgreSQL, and SQL Server**. Google manages patching, backups, replication, high availability, and failover. You connect via private IP, public IP (with SSL), the **Cloud SQL Auth Proxy**, or built-in Cloud Run integration.

     ```bash
     gcloud sql instances create orders-db \
         --database-version=POSTGRES_16 --tier=db-custom-2-7680 \
         --region=us-central1 --availability-type=REGIONAL
     ```

     **[⬆ Back to Top](#table-of-contents)**

117. ### Which database engines are supported by Cloud SQL?

     Cloud SQL supports three engines:

     | Engine | Versions (representative) |
     | --- | --- |
     | **MySQL** | 5.7, 8.0, 8.4 |
     | **PostgreSQL** | 9.6 through 16 |
     | **SQL Server** | 2017, 2019, 2022 |

     Exact version availability can vary by region. For new Java/Spring Boot backends, **PostgreSQL** is a popular choice for its features and standards compliance.

     **[⬆ Back to Top](#table-of-contents)**

118. ### When would you choose Cloud SQL over Cloud Spanner?

     Choose **Cloud SQL** when you need a **managed relational database** with familiar engines, ACID transactions, and **moderate scale** (up to tens of TB). It's ideal for typical OLTP apps, CMS/WordPress, CRM, and anything using standard MySQL/PostgreSQL features.

     Choose **Cloud Spanner** when you need **horizontal scalability, global distribution, strong consistency across regions, and very high throughput** (beyond a single node, often >~20 TB). Spanner costs more and uses a different operational model.

     | | Cloud SQL | Cloud Spanner |
     | --- | --- | --- |
     | **Scale** | Vertical, tens of TB | Horizontal, unlimited |
     | **Distribution** | Regional | Global |
     | **Cost** | Lower | Higher |
     | **Use case** | Standard OLTP | Global, high-scale OLTP |

     **[⬆ Back to Top](#table-of-contents)**

119. ### What is the difference between Cloud SQL high availability and read replicas?

     | | High Availability (HA) | Read Replicas |
     | --- | --- | --- |
     | **Purpose** | Automatic failover | Offload read traffic |
     | **Config** | Primary + standby in another zone | Separate async-replicating instances |
     | **Failover** | Automatic | Manual promotion (for DR) |
     | **Replication** | Synchronous (regional disk) | Asynchronous |

     **HA** keeps a synchronous standby in another zone; if the primary fails, the standby is promoted automatically with minimal downtime. **Read replicas** are asynchronous copies that serve read queries to scale reads — they can be promoted to standalone instances for DR but aren't used for automatic failover.

     **[⬆ Back to Top](#table-of-contents)**

120. ### How does Cloud SQL failover work?

     In an **HA configuration**, Cloud SQL **synchronously replicates** data to a standby instance in another zone. When health checks detect a primary failure:

     1. The **standby is promoted** to primary.
     2. The instance's IP is **moved** to the new primary.
     3. Client connections may need to **reconnect** (connection pools re-establish).

     Failover is **automatic** but causes a brief outage (typically tens of seconds). Design your app with **connection retry logic** to handle the reconnect gracefully.

     **[⬆ Back to Top](#table-of-contents)**

121. ### What are Cloud SQL backups?

     Cloud SQL performs **automated daily backups** and supports **on-demand backups**. Backups are stored in **multi-region Cloud Storage**. You configure:

     - **Backup window** (when daily backups run).
     - **Retention** (e.g., keep the last 7 backups).
     - **Binary/transaction logging** to enable **point-in-time recovery**.

     ```bash
     # On-demand backup
     gcloud sql backups create --instance=orders-db
     # Configure automated backups with PITR
     gcloud sql instances patch orders-db \
         --backup-start-time=02:00 --enable-point-in-time-recovery
     ```

     **[⬆ Back to Top](#table-of-contents)**

122. ### What is point-in-time recovery in Cloud SQL?

     **Point-in-time recovery (PITR)** lets you restore an instance to a **specific timestamp** within the retention window. It combines a **base backup** with **binary/transaction logs** to replay changes up to the target time. PITR is invaluable for recovering from accidental data loss — e.g., rewinding to just before an erroneous `DROP TABLE`.

     ```bash
     gcloud sql instances clone orders-db orders-db-recovered \
         --point-in-time="2026-06-21T10:30:00Z"
     ```

     **[⬆ Back to Top](#table-of-contents)**

123. ### How do you connect a Spring Boot application to Cloud SQL securely?

     Two main approaches:

     - **Cloud SQL JDBC Socket Factory** — add the dependency and specify the instance connection name; it handles IAM auth and TLS transparently.
     - **Cloud SQL Auth Proxy** — run as a sidecar; your app connects to `localhost` and the proxy secures the tunnel.

     Use **IAM database authentication** or a service account; never embed DB passwords in code (use Secret Manager).

     ```properties
     # application.properties using the Cloud SQL Socket Factory (PostgreSQL)
     spring.datasource.url=jdbc:postgresql:///orders?\
     cloudSqlInstance=my-project:us-central1:orders-db&\
     socketFactory=com.google.cloud.sql.postgres.SocketFactory&\
     user=app-user
     ```

     ```xml
     <!-- pom.xml -->
     <dependency>
       <groupId>com.google.cloud.sql</groupId>
       <artifactId>postgres-socket-factory</artifactId>
       <version>1.x.x</version>
     </dependency>
     ```

     **[⬆ Back to Top](#table-of-contents)**

124. ### What is the Cloud SQL Auth Proxy?

     The **Cloud SQL Auth Proxy** is a utility that **authenticates and encrypts** connections to Cloud SQL using IAM/service-account credentials, establishing a secure tunnel. Your application connects to a **local port** instead of the database's IP, and the proxy handles auth and TLS.

     ```bash
     ./cloud-sql-proxy --port=5432 \
         my-project:us-central1:orders-db \
         --credentials-file=service-account.json
     # App connects to localhost:5432
     ```

     It's commonly run as a **sidecar container** alongside the app in GKE or Cloud Run.

     **[⬆ Back to Top](#table-of-contents)**

125. ### What is private IP connectivity for Cloud SQL?

     **Private IP connectivity** assigns an **internal IP** to a Cloud SQL instance and connects it to your **VPC** via **private services access (VPC peering)**. Traffic stays entirely within Google's private network — **no public IP** is exposed. This is the **recommended** setup for security-sensitive workloads, eliminating public attack surface.

     ```bash
     gcloud sql instances patch orders-db \
         --network=projects/my-project/global/networks/default \
         --no-assign-ip   # private IP only
     ```

     **[⬆ Back to Top](#table-of-contents)**

126. ### What is Cloud Spanner?

     **Cloud Spanner** is a **globally distributed, horizontally scalable relational database**. It uniquely combines:

     - **ACID transactions** and **SQL** support.
     - **Strong global consistency** (external consistency).
     - **Automatic sharding** and **multi-region replication**.

     Spanner is built for large-scale OLTP needing high throughput, high availability, and global distribution — e.g., financial systems and global SaaS.

     **[⬆ Back to Top](#table-of-contents)**

127. ### When would you choose Cloud Spanner?

     Choose Spanner when you need to **scale beyond a single-node relational database** while keeping relational semantics:

     - **Tens of TB to petabytes** of data.
     - **Very high write throughput**.
     - **Global replication** with strong consistency.
     - **99.999% availability** (multi-region).

     Typical use cases: global financial ledgers, large-scale multi-tenant SaaS, gaming backends, and inventory systems spanning continents.

     **[⬆ Back to Top](#table-of-contents)**

128. ### How is Cloud Spanner different from a traditional relational database?

     | | Traditional RDBMS | Cloud Spanner |
     | --- | --- | --- |
     | **Scaling** | Vertical (bigger server) | Horizontal (add nodes) |
     | **Sharding** | Manual | Automatic (splits) |
     | **Replication** | Primary–replica | Distributed consensus (Paxos) |
     | **Consistency** | Single-node strong; cross-region hard | Global strong (TrueTime) |

     Spanner **shards data automatically across nodes** and uses **distributed consensus plus the TrueTime API** (globally synchronized clocks with bounded uncertainty) to deliver **strong consistency across regions** — something extremely hard to achieve in self-managed databases. It uses MVCC and two-phase commits across shards.

     **[⬆ Back to Top](#table-of-contents)**

129. ### What is horizontal scalability in Cloud Spanner?

     **Horizontal scalability** means you add **nodes (or processing units)** to increase Spanner's storage and compute capacity. Spanner divides data into **splits** and automatically **rebalances** them across nodes. As you add/remove nodes, throughput scales **roughly linearly** without manual resharding or downtime — a key advantage over vertically-scaled databases.

     ```bash
     gcloud spanner instances update my-instance --nodes=6   # scale up
     ```

     **[⬆ Back to Top](#table-of-contents)**

130. ### What is strong consistency in Cloud Spanner?

     **Strong (external) consistency** means that once a write transaction commits, **any subsequent read anywhere in the world sees that change immediately** — no eventual-consistency lag. Spanner achieves this via **multi-phase commit** and the **TrueTime API**, which provides a bounded clock-uncertainty interval. This gives globally consistent transactions without the trade-offs typical of distributed systems.

     **[⬆ Back to Top](#table-of-contents)**

131. ### What is AlloyDB?

     **AlloyDB for PostgreSQL** is a managed, **PostgreSQL-compatible** database delivering high performance and availability. It features:

     - A **distributed architecture** separating storage and compute.
     - **Columnar acceleration** for analytical queries.
     - **Automatic failover** and a **99.99% availability SLA**.

     AlloyDB targets **analytics-heavy transactional (HTAP)** workloads, offering significantly better performance than standard PostgreSQL for mixed workloads.

     **[⬆ Back to Top](#table-of-contents)**

132. ### When would you choose AlloyDB over Cloud SQL for PostgreSQL?

     Choose **AlloyDB** when your PostgreSQL workload needs:

     - **Higher throughput** and better performance than Cloud SQL can offer.
     - **Fast analytical queries** alongside transactions (HTAP) via its columnar engine.
     - **Scale-out** read capacity beyond Cloud SQL's limits.

     Choose **Cloud SQL** for simpler, smaller PostgreSQL workloads where its managed simplicity and lower cost suffice. AlloyDB is the step up when you outgrow Cloud SQL but want to stay PostgreSQL-compatible (avoiding a Spanner rewrite).

     **[⬆ Back to Top](#table-of-contents)**

133. ### What is Firestore?

     **Firestore** is a serverless **NoSQL document database** for mobile, web, and server apps. It stores data as **collections of documents** (JSON-like), supports **rich queries, offline support, and real-time listeners**, and scales automatically. It has two modes: **Native mode** (real-time, mobile-optimized) and **Datastore mode** (server-side, high-scale, strongly consistent).

     ```java
     // Firestore Java client — write a document
     Firestore db = FirestoreOptions.getDefaultInstance().getService();
     Map<String, Object> order = Map.of("orderId", "123", "status", "PLACED", "amount", 99.99);
     db.collection("orders").document("123").set(order).get();
     ```

     **[⬆ Back to Top](#table-of-contents)**

134. ### What is the difference between Firestore Native mode and Datastore mode?

     | | Native Mode | Datastore Mode |
     | --- | --- | --- |
     | **Optimized for** | Mobile/web, real-time sync | Server-side, high scale |
     | **Real-time listeners** | Yes | No |
     | **Data model** | Documents + subcollections | Entities (next-gen Datastore) |
     | **Offline SDKs** | Yes (mobile) | No |
     | **Consistency** | Strong | Strong |

     **Native mode** supports hierarchical data, real-time updates, and mobile SDKs — best for client-facing apps. **Datastore mode** is the evolution of Datastore for server-side, schemaless, high-throughput workloads. You pick a mode per project at creation and cannot switch later.

     **[⬆ Back to Top](#table-of-contents)**

135. ### When would you choose Firestore for backend application development?

     Choose Firestore when you need:

     - **Real-time updates** — chat apps, collaborative editing, live dashboards.
     - **Offline support** for mobile clients.
     - **Flexible, hierarchical** data structures (documents and subcollections).
     - Tight integration with **Cloud Functions** triggers for serverless event-driven logic.

     It's excellent for serverless architectures and rapidly-evolving schemas, but less suited to complex multi-row transactional joins (use a relational DB for those).

     **[⬆ Back to Top](#table-of-contents)**

136. ### What is Bigtable?

     **Cloud Bigtable** is a **wide-column NoSQL database** based on Google's internal Bigtable, designed for **massive scale (petabytes)** with **low latency and high throughput**. Data is identified by **row keys**, with columns grouped into **column families**. It's not relational — no joins or multi-row transactions. Ideal for **time-series data, IoT telemetry, ad-tech, and large-scale analytics**.

     ```java
     // Bigtable: write a row (HBase-compatible client)
     try (Connection connection = BigtableConfiguration.connect("my-project", "my-instance")) {
         Table table = connection.getTable(TableName.valueOf("sensor-data"));
         Put put = new Put(Bytes.toBytes("sensor#001#20260621T1000"));
         put.addColumn(Bytes.toBytes("metrics"), Bytes.toBytes("temp"), Bytes.toBytes("22.5"));
         table.put(put);
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

137. ### When would you use Bigtable instead of Firestore?

     | | Bigtable | Firestore |
     | --- | --- | --- |
     | **Scale** | Petabytes, very high throughput | Large, but document-oriented |
     | **Access pattern** | Range reads over ordered keys | Rich queries, real-time listeners |
     | **Data model** | Wide-column, key-based | Documents + subcollections |
     | **Transactions** | Single-row | Multi-document |

     Choose **Bigtable** for **high-throughput, petabyte-scale** workloads with **ordered-key range scans** (e.g., time-series). Choose **Firestore** for hierarchical data, complex queries, and real-time mobile/web apps. Bigtable trades query flexibility for raw scale and throughput.

     **[⬆ Back to Top](#table-of-contents)**

138. ### What is Memorystore?

     **Memorystore** is a fully managed **in-memory caching** service supporting **Redis and Valkey**. It provides sub-millisecond data access to offload databases and speed up applications. Tiers include **Basic** (single node) and **Standard/HA** (replicated). You connect via internal IP and integrate with GKE or Compute Engine.

     ```bash
     gcloud redis instances create session-cache \
         --size=5 --region=us-central1 --tier=STANDARD_HA --redis-version=redis_7_0
     ```

     **[⬆ Back to Top](#table-of-contents)**

139. ### What is the difference between Memorystore for Redis and Memorystore for Valkey?

     - **Memorystore for Redis** runs the open-source **Redis** engine — mature, widely supported, huge client ecosystem.
     - **Memorystore for Valkey** runs **Valkey**, a community fork of Redis created by former Redis maintainers after Redis Labs changed its licensing. Valkey stays open-source (BSD) and is Redis-protocol compatible, so existing Redis clients work.

     Choose based on **ecosystem compatibility, licensing preferences, and desired features**. Both offer similar caching capabilities; Valkey is the open-source-forward path going forward.

     **[⬆ Back to Top](#table-of-contents)**

140. ### How do you use Memorystore for caching session data?

     Store session data in a Memorystore (Redis) instance and configure your app's session library to use it:

     1. Connect to the instance's **internal IP and port**.
     2. Set appropriate **TTLs** so sessions expire automatically.
     3. Use the **Standard/HA tier** for resilience; handle connection timeouts with **retry logic**.

     ```java
     // Spring Boot — Spring Session backed by Redis (Memorystore)
     // application.properties:
     // spring.data.redis.host=10.x.x.x
     // spring.data.redis.port=6379
     // spring.session.store-type=redis
     // spring.session.timeout=30m

     @EnableRedisHttpSession
     @Configuration
     public class SessionConfig {
         @Bean
         public LettuceConnectionFactory connectionFactory() {
             return new LettuceConnectionFactory(
                 new RedisStandaloneConfiguration("10.x.x.x", 6379));
         }
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Networking, Load Balancing, DNS and CDN

141. ### What is a VPC in Google Cloud?

     A **Virtual Private Cloud (VPC)** is a **logically isolated network** in GCP providing IP ranges, subnets, routing, and firewall policies. All Compute Engine, GKE, and serverless resources attach to a VPC to communicate internally and externally. GCP VPCs are **global** (one VPC spans all regions), support **private access** to Google services, and use software-defined networking.

     ```bash
     gcloud compute networks create my-vpc --subnet-mode=custom
     gcloud compute networks subnets create web-subnet \
         --network=my-vpc --region=us-central1 --range=10.0.1.0/24
     ```

     **[⬆ Back to Top](#table-of-contents)**

142. ### How is a Google Cloud VPC different from a traditional VPC?

     A GCP VPC is **global** — a single VPC spans **all regions**, with **regional subnets** allocating IP ranges per region. Google manages the underlying network fabric and **cross-region communication automatically**. This contrasts with other clouds where a VPC is regional and you must create one per region and peer them. The global model **simplifies multi-region networking** dramatically.

     **[⬆ Back to Top](#table-of-contents)**

143. ### What is the difference between auto mode and custom mode VPC?

     | | Auto Mode | Custom Mode |
     | --- | --- | --- |
     | **Subnets** | Auto-created in every region | You create them manually |
     | **IP ranges** | Predefined (10.x.x.x) | You choose CIDR blocks |
     | **Control** | Low | High |
     | **Production** | Discouraged | **Recommended** |

     **Auto mode** is convenient for quick starts but uses large default ranges that may conflict with on-prem networks. **Custom mode** gives full control over CIDR allocation and is recommended for production and hybrid connectivity.

     **[⬆ Back to Top](#table-of-contents)**

144. ### What are subnets in GCP?

     **Subnets** partition a VPC's address space into smaller IP ranges **within a specific region**. Each subnet defines the IP range for resources placed in it and can have its own routes and firewall rules. Because the **VPC is global** but **subnets are regional**, resources in different regions of the same VPC can still communicate **privately** over Google's backbone.

     **[⬆ Back to Top](#table-of-contents)**

145. ### Why are GCP subnets regional?

     Subnets are **regional** to enable **fine-grained IP allocation and isolation per region**, aligning with the fact that resources (like VMs) need IPs in a specific region where they run. Since the VPC itself is **global**, cross-region resources still communicate privately without separate VPCs or peering. This design **simplifies multi-region deployments** while keeping IP management localized.

     **[⬆ Back to Top](#table-of-contents)**

146. ### What are firewall rules in GCP?

     **Firewall rules** control ingress and egress traffic to VPC resources. Each rule has:

     - **Priority** (lower number = higher precedence).
     - **Action** (allow/deny).
     - **Direction** (ingress/egress).
     - **Match criteria** — IP ranges, ports, protocols, **target tags** or **service accounts**.

     Rules are evaluated in **priority order**; the first match wins.

     ```bash
     gcloud compute firewall-rules create allow-https \
         --network=my-vpc --direction=INGRESS --action=ALLOW \
         --rules=tcp:443 --source-ranges=0.0.0.0/0 --target-tags=web --priority=1000
     ```

     **[⬆ Back to Top](#table-of-contents)**

147. ### What is the difference between ingress and egress firewall rules?

     - **Ingress rules** control traffic **entering** a resource (e.g., internet → VM on port 443).
     - **Egress rules** control traffic **leaving** a resource (e.g., VM → external API).

     By default, GCP **allows all egress** and **denies all ingress** (except internal). You add egress deny rules when you need to restrict outbound traffic — e.g., forcing all traffic through a NAT or security appliance, or blocking access to specific external endpoints.

     **[⬆ Back to Top](#table-of-contents)**

148. ### What are network tags and service accounts used for in firewall rules?

     Firewall rules can **target** resources by:

     - **Network tags** — string labels on VMs. A rule with `--target-tags=web` applies only to instances tagged `web`.
     - **Service accounts** — a rule targeting a service account applies to all VMs running as that SA.

     This enables **micro-segmentation** without managing IP addresses directly. Service-account targeting is generally **more secure** than tags because tags can be added by anyone with instance-edit permissions, whereas changing a VM's service account requires higher privilege.

     **[⬆ Back to Top](#table-of-contents)**

149. ### What is Cloud NAT?

     **Cloud NAT (Network Address Translation)** provides **outbound internet connectivity for private resources** (VMs/GKE nodes without external IPs). It:

     - **Scales automatically** and is fully managed.
     - Allows **outbound** connections while **blocking inbound** ones.
     - Logs to Cloud Logging for audit.

     It's required when you disable external IPs but still need package updates or external API calls.

     ```bash
     gcloud compute routers create nat-router --network=my-vpc --region=us-central1
     gcloud compute routers nats create my-nat \
         --router=nat-router --region=us-central1 \
         --nat-all-subnet-ip-ranges --auto-allocate-nat-external-ips
     ```

     **[⬆ Back to Top](#table-of-contents)**

150. ### Why is Cloud NAT used for private workloads?

     Cloud NAT lets **private VMs/GKE nodes without public IPs reach the internet** for updates and API calls while remaining **unreachable from outside**. Benefits:

     - **Improved security** — no inbound access, smaller attack surface.
     - **Centralized egress** — simplifies network design and IP management.
     - **Auditability** — NAT logs can be exported for analysis.

     It's a core building block for secure private architectures where instances should never have public IPs.

     **[⬆ Back to Top](#table-of-contents)**

151. ### What is Private Google Access?

     **Private Google Access** allows VMs in subnets **without external IPs** to reach **Google APIs and services** (Cloud Storage, BigQuery, etc.) using **internal IPs**. When enabled on a subnet, traffic to Google APIs is routed privately over Google's network instead of the public internet — so private workloads can call GCP services without needing external IPs or NAT for that traffic.

     ```bash
     gcloud compute networks subnets update web-subnet \
         --region=us-central1 --enable-private-ip-google-access
     ```

     **[⬆ Back to Top](#table-of-contents)**

152. ### What is Private Service Connect?

     **Private Service Connect (PSC)** lets you access Google services or third-party/published services **privately using internal IPs** in your VPC. PSC creates **endpoints** in your VPC that map to:

     - **Google APIs** (e.g., a private endpoint for `storage.googleapis.com`).
     - **Published services** in another VPC (producer/consumer model).

     Traffic stays **inside Google's network**, avoiding the public internet and NAT traversal — ideal for security-sensitive, multi-tenant, or SaaS connectivity.

     **[⬆ Back to Top](#table-of-contents)**

153. ### What is VPC peering?

     **VPC peering** connects two VPC networks (same or different projects/orgs) so resources communicate **privately via internal IPs**. Key properties:

     - **Non-transitive** — if A peers with B and B peers with C, A cannot reach C.
     - No overlapping IP ranges allowed.
     - Used for **shared services, cross-project communication**, and connecting to managed services (e.g., Cloud SQL private IP uses peering).

     ```bash
     gcloud compute networks peerings create peer-a-to-b \
         --network=vpc-a --peer-network=vpc-b
     ```

     **[⬆ Back to Top](#table-of-contents)**

154. ### What is Shared VPC?

     **Shared VPC** lets you define a **host project** whose VPC networks are shared with **service projects**. Service projects create resources (VMs, GKE clusters) in the host project's subnets. This **centralizes network administration** (firewall rules, routing, connectivity) while letting teams own their own projects and resources — a clean separation of network and application ownership.

     **[⬆ Back to Top](#table-of-contents)**

155. ### When would you use Shared VPC in an enterprise environment?

     Use **Shared VPC** when multiple teams/projects must **share common network infrastructure**:

     - **Centralized connectivity** — on-prem links (VPN/Interconnect), Private Service Connect, NAT, load balancers.
     - **Consistent security** — network admins enforce firewall and routing policies centrally.
     - **Hub-and-spoke model** — network admins control the host project; app teams deploy in service projects.

     It supports **separation of duties** at scale: each team gets its own project for resources while the organization maintains uniform network governance.

     **[⬆ Back to Top](#table-of-contents)**

156. ### What is Cloud Load Balancing?

     **Cloud Load Balancing** is a fully distributed, software-defined load balancing service. It offers:

     - **Global HTTP(S)** load balancing with cross-region routing and automatic failover.
     - **TCP/UDP proxy** and **Network** load balancing.
     - **Internal** load balancing for private services.

     You define a **forwarding rule, backend service, and health checks**; the LB routes traffic to the **healthy backend in the closest region**. It scales automatically with no pre-warming.

     **[⬆ Back to Top](#table-of-contents)**

157. ### What is the difference between global and regional load balancers?

     | | Global LB | Regional LB |
     | --- | --- | --- |
     | **Scope** | Multiple regions, single anycast IP | Single region |
     | **Routing** | Nearest healthy backend, auto failover | Within region |
     | **Layer** | L7 (HTTP/S) | L4 (TCP/UDP) or internal |
     | **Use case** | Global web apps | Non-HTTP, internal, regional |

     **Global load balancers** (HTTP(S)) provide one anycast IP and route users to the nearest healthy region, handling region failover automatically. **Regional load balancers** operate within a single region for low latency, non-HTTP protocols, or internal traffic.

     **[⬆ Back to Top](#table-of-contents)**

158. ### What is the difference between external and internal load balancing?

     - **External load balancers** expose services to the **public internet** with an external IP.
     - **Internal load balancers** distribute traffic **privately within a VPC** (or connected networks) using internal IPs.

     Internal LBs are used for **microservices and internal applications** that should not be publicly accessible — e.g., a backend tier reachable only by other services in the VPC.

     **[⬆ Back to Top](#table-of-contents)**

159. ### What is an HTTP(S) Load Balancer?

     An **HTTP(S) Load Balancer** is a **globally distributed L7 load balancer** that:

     - **Terminates TLS** (with Google-managed or self-managed certs).
     - Performs **URL/host-based routing** to backend services.
     - Balances across **Compute Engine groups, GKE (NEGs), and Cloud Run**.
     - Uses **Google Front Ends (GFEs)** at the edge.
     - Integrates with **Cloud CDN** (caching) and **Cloud Armor** (WAF/DDoS).

     It's the standard front door for global web applications and APIs.

     **[⬆ Back to Top](#table-of-contents)**

160. ### What is a TCP/UDP Network Load Balancer?

     A **TCP/UDP Network Load Balancer** is a **regional L4 load balancer** that forwards TCP or UDP traffic to backend instances or NEG endpoints. It provides a **single regional IP**, supports **cross-zone** balancing, and is used for **high-throughput, latency-sensitive non-HTTP workloads** — game servers, streaming protocols, custom TCP services.

     **[⬆ Back to Top](#table-of-contents)**

161. ### What is Cloud CDN?

     **Cloud CDN** is Google's **content delivery network** integrated with the HTTP(S) Load Balancer. It **caches content at edge points of presence** worldwide, reducing latency and offloading origin servers. You enable it on a backend service, set cache policies, and can protect content with **signed URLs/cookies**. It supports **negative caching** and **origin shield** for dynamic content acceleration.

     ```bash
     gcloud compute backend-services update web-backend \
         --enable-cdn --cache-mode=CACHE_ALL_STATIC
     ```

     **[⬆ Back to Top](#table-of-contents)**

162. ### How does Cloud CDN improve application performance?

     Cloud CDN improves performance by:

     - **Serving cached content from an edge location** close to the user, cutting round-trip latency.
     - **Reducing origin load** and **egress costs** by handling repeat requests at the edge.
     - **Caching static assets** (images, CSS, JS) and, where configured, dynamic content.
     - **Compressing responses** and handling **TLS termination** at the edge for higher throughput.

     The result is faster page loads and a more scalable, cost-efficient backend.

     **[⬆ Back to Top](#table-of-contents)**

163. ### What is Cloud DNS?

     **Cloud DNS** is a scalable, reliable, managed **Domain Name System** service. It hosts DNS **zones and records** (A, AAAA, CNAME, MX, TXT, etc.) on **global anycast name servers** for low-latency resolution worldwide. You manage records via Console, `gcloud`, or API, and it integrates with Cloud Domains and Cloud CDN. It offers a 100% availability SLA.

     ```bash
     gcloud dns managed-zones create my-zone --dns-name=example.com. --description="Prod zone"
     gcloud dns record-sets create app.example.com. --zone=my-zone \
         --type=A --ttl=300 --rrdatas=34.120.0.1
     ```

     **[⬆ Back to Top](#table-of-contents)**

164. ### What is Cloud Armor?

     **Cloud Armor** is a distributed **Web Application Firewall (WAF) and DDoS protection** service integrated with Google's load balancers. It lets you define **security policies** to allow/block traffic based on L7 rules, IP lists, geolocation, or **preconfigured WAF rule sets** (OWASP Top 10). It also offers **Adaptive Protection** — ML-based detection of anomalous traffic — and absorbs volumetric DDoS attacks at Google's edge.

     **[⬆ Back to Top](#table-of-contents)**

165. ### How does Cloud Armor protect backend applications?

     Cloud Armor evaluates incoming requests **before they reach your backends**:

     - **Block by IP, country, or WAF rule** — drop malicious IPs, restrict regions, inspect headers/payloads.
     - **Rate limiting** — throttle abusive clients.
     - **Adaptive Protection** — automatically detects and mitigates anomalous patterns (DDoS, scraping).
     - **Logging** — request metadata to Cloud Logging for analysis.

     ```bash
     gcloud compute security-policies create web-policy
     gcloud compute security-policies rules create 1000 \
         --security-policy=web-policy \
         --expression="origin.region_code == 'XX'" --action=deny-403
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Pub/Sub and Event-Driven Architecture

166. ### What is Pub/Sub?

     **Pub/Sub** is GCP's asynchronous, fully managed **messaging service** that decouples **publishers** (producers) from **subscribers** (consumers). Publishers send messages to **topics**; subscribers create **subscriptions** and receive messages via **pull** (polling) or **push** (HTTP). Pub/Sub enables event-driven architectures, smooths traffic spikes by buffering, and scales to millions of messages per second.

     ```java
     // Publish a message with the Java client
     Publisher publisher = Publisher.newBuilder(TopicName.of("my-project", "orders")).build();
     PubsubMessage msg = PubsubMessage.newBuilder()
         .setData(ByteString.copyFromUtf8("{\"orderId\":\"123\"}")).build();
     ApiFuture<String> messageId = publisher.publish(msg);
     System.out.println("Published: " + messageId.get());
     publisher.shutdown();
     ```

     **[⬆ Back to Top](#table-of-contents)**

167. ### What is the difference between a topic and a subscription?

     - A **topic** is a named resource where publishers send messages.
     - A **subscription** represents the stream of messages from a topic to a particular subscriber.

     **Multiple subscriptions** can attach to one topic; each subscription receives **every message** independently (fan-out). One subscription can be at a different processing point than another, and each delivers messages once to its subscriber (subject to at-least-once semantics).

     **[⬆ Back to Top](#table-of-contents)**

168. ### What is a publisher in Pub/Sub?

     A **publisher** is any client that **sends messages to a topic** — via client libraries, REST API, or `gcloud pubsub topics publish`. Publishers are **fully decoupled** from subscribers; they don't know who (if anyone) consumes the messages. This decoupling is what makes Pub/Sub ideal for loosely-coupled microservices.

     **[⬆ Back to Top](#table-of-contents)**

169. ### What is a subscriber in Pub/Sub?

     A **subscriber** is a client that **receives messages from a subscription**. In **pull** subscriptions, the subscriber polls for messages; in **push** subscriptions, Pub/Sub delivers messages to an HTTP endpoint. The subscriber processes each message and must **acknowledge (ack)** it when done to prevent redelivery.

     ```java
     // Pull subscriber with a message handler
     MessageReceiver receiver = (message, consumer) -> {
         System.out.println("Received: " + message.getData().toStringUtf8());
         consumer.ack();   // acknowledge after successful processing
     };
     Subscriber subscriber = Subscriber.newBuilder(
         ProjectSubscriptionName.of("my-project", "orders-sub"), receiver).build();
     subscriber.startAsync().awaitRunning();
     ```

     **[⬆ Back to Top](#table-of-contents)**

170. ### What is the difference between push and pull subscriptions?

     | | Pull | Push |
     | --- | --- | --- |
     | **Delivery** | Subscriber calls Pull API | Pub/Sub POSTs to HTTP endpoint |
     | **Control** | Subscriber controls fetch rate | Pub/Sub controls delivery |
     | **Setup** | More client code, concurrency control | Easier; needs public/authorized endpoint |
     | **Best for** | High throughput, batch processing | Serverless (Cloud Run/Functions) |

     **Pull** gives the subscriber control over when and how many messages to fetch (good for throughput). **Push** delivers to an endpoint that returns HTTP 200 on success (good for serverless targets like Cloud Run).

     **[⬆ Back to Top](#table-of-contents)**

171. ### What is acknowledgement in Pub/Sub?

     **Acknowledgement (ack)** confirms to Pub/Sub that a message was **successfully processed**. The subscriber must ack before the **ack deadline** expires; otherwise Pub/Sub **redelivers** the message. Acks enable **at-least-once delivery** — messages are retried until acknowledged, guaranteeing no loss (but allowing duplicates).

     **[⬆ Back to Top](#table-of-contents)**

172. ### What happens if a Pub/Sub message is not acknowledged?

     If the subscriber doesn't ack before the **ack deadline**, Pub/Sub treats the message as **undelivered** and **redelivers** it (possibly to another subscriber instance). This ensures **no message loss**, but means **duplicates can occur**. Subscribers must therefore be designed to be **idempotent** so reprocessing the same message is harmless.

     **[⬆ Back to Top](#table-of-contents)**

173. ### What is acknowledgement deadline?

     The **ack deadline** is the time window in which a subscriber must ack a message. The default is **10 seconds** for pull subscriptions; the **maximum is 10 minutes**. If processing takes longer, the subscriber can **extend the deadline** (modify ack deadline) to avoid premature redelivery. If the deadline passes without an ack, the message is redelivered.

     ```bash
     gcloud pubsub subscriptions create orders-sub \
         --topic=orders --ack-deadline=60
     ```

     **[⬆ Back to Top](#table-of-contents)**

174. ### What is message retention in Pub/Sub?

     **Message retention** controls how long Pub/Sub stores messages. Unacknowledged messages are retained for a configurable period (**default 7 days**, max 31 days). You can also **retain acknowledged messages** to allow **seek/replay** to a past timestamp. After retention expires, messages are removed even if never delivered.

     ```bash
     gcloud pubsub subscriptions update orders-sub \
         --message-retention-duration=7d --retain-acked-messages
     ```

     **[⬆ Back to Top](#table-of-contents)**

175. ### What is dead-letter topic in Pub/Sub?

     A **dead-letter topic (DLT)** is a secondary topic configured on a subscription. When a message **fails delivery/processing repeatedly** (exceeds the max delivery attempts), Pub/Sub **moves it to the dead-letter topic** instead of redelivering forever. This isolates poison messages for separate inspection and prevents them from blocking the main subscription.

     ```bash
     gcloud pubsub subscriptions create orders-sub --topic=orders \
         --dead-letter-topic=orders-dlt --max-delivery-attempts=5
     ```

     **[⬆ Back to Top](#table-of-contents)**

176. ### What is ordering key in Pub/Sub?

     An **ordering key** is a string that tells Pub/Sub to **deliver messages with the same key in publish order**. When ordering is enabled on the topic, all messages sharing an ordering key are delivered sequentially to the subscriber. This is essential for event sequences that must be processed in order — e.g., all events for a single bank account or order.

     ```java
     PubsubMessage msg = PubsubMessage.newBuilder()
         .setData(ByteString.copyFromUtf8(payload))
         .setOrderingKey("account-42")   // same key → ordered
         .build();
     ```

     **[⬆ Back to Top](#table-of-contents)**

177. ### How does Pub/Sub support at-least-once delivery?

     By default Pub/Sub uses **at-least-once delivery**: messages are **retried until acknowledged**. If the ack isn't received before the deadline, Pub/Sub **redelivers**. This guarantees **no message loss**, but **duplicates can occur** (e.g., if processing succeeds but the ack is lost). Subscribers must implement **idempotent processing or deduplication** to handle duplicates. (Pub/Sub also offers an optional **exactly-once** delivery mode per subscription.)

     **[⬆ Back to Top](#table-of-contents)**

178. ### How do you make Pub/Sub consumers idempotent?

     Design subscribers so processing the **same message multiple times yields the same result**:

     - **Dedup by ID** — store processed message/event IDs in a database or cache (e.g., Redis); skip if already seen.
     - **Database upserts** — use `INSERT ... ON CONFLICT DO NOTHING` (PostgreSQL) so duplicate inserts are no-ops.
     - **Commutative operations** — design business logic where reapplying has no extra effect.

     ```java
     // Dedup using a unique message ID stored in a cache
     String msgId = message.getMessageId();
     if (redis.setIfAbsent("processed:" + msgId, "1", Duration.ofDays(1))) {
         process(message);   // only the first time
     }
     consumer.ack();
     ```

     **[⬆ Back to Top](#table-of-contents)**

179. ### How do you handle duplicate messages in Pub/Sub?

     - **Idempotent processing** — dedup by ID or use upserts (as above).
     - **Exactly-once delivery** — enable it on the subscription (uses supported client libraries) to eliminate duplicates within the ack window.
     - **Stream deduplication** — for data pipelines, use **Cloud Dataflow**, which can dedup events based on a key and window.

     ```bash
     gcloud pubsub subscriptions create orders-sub --topic=orders \
         --enable-exactly-once-delivery
     ```

     **[⬆ Back to Top](#table-of-contents)**

180. ### What is Eventarc?

     **Eventarc** is a fully managed **event routing** service that delivers events from GCP services (and beyond) to **Cloud Run, Cloud Functions, or GKE**. It uses the standardized **CloudEvents** format and supports **audit-log events** and **direct events** from sources like Cloud Storage, Firestore, and Pub/Sub. Eventarc simplifies event-driven architectures by handling the routing plumbing for you.

     ```bash
     gcloud eventarc triggers create gcs-trigger \
         --destination-run-service=processor --location=us-central1 \
         --event-filters="type=google.cloud.storage.object.v1.finalized" \
         --event-filters="bucket=my-uploads" \
         --service-account=eventarc-sa@my-project.iam.gserviceaccount.com
     ```

     **[⬆ Back to Top](#table-of-contents)**

181. ### How is Eventarc related to Cloud Run?

     Eventarc can **route events to Cloud Run services**. You configure an Eventarc trigger specifying the **target Cloud Run service**, **event type** (e.g., GCS object finalize), and optional filters. Behind the scenes Eventarc provisions Pub/Sub topics/subscriptions and **pushes events** to the service's endpoint as an **HTTP POST with a CloudEvents envelope**. This lets stateless Cloud Run services react to GCP events without manual Pub/Sub wiring.

     **[⬆ Back to Top](#table-of-contents)**

182. ### How would you design an event-driven order processing system on GCP?

     **Architecture:**

     ```
     Order API (Cloud Run) ──publish──> [orders topic] ──> inventory-sub  → Inventory Service
                                                        ──> payment-sub    → Payment Service
                                                        ──> notify-sub     → Notification Service
     ```

     **Design decisions:**

     - **Pub/Sub topics** per event type (`order-created`, `payment-processed`, `item-shipped`).
     - **Separate subscriptions** per microservice so each consumes independently; design all consumers **idempotent**.
     - **Cloud Run or GKE** for the microservices; optionally **Eventarc** to trigger from Cloud Storage/Firestore.
     - **Ordering keys** (e.g., `orderId`) where event order matters.
     - **Dead-letter topics** + retries for poison messages.
     - **Cloud Functions** for lightweight tasks like confirmation emails.

     ```java
     // Order API publishes an event after persisting the order
     publisher.publish(PubsubMessage.newBuilder()
         .setData(ByteString.copyFromUtf8(orderJson))
         .setOrderingKey(orderId)
         .putAttributes("eventType", "ORDER_CREATED")
         .build());
     ```

     **[⬆ Back to Top](#table-of-contents)**

183. ### How do you retry failed event processing safely?

     - **Subscriber retry** — Pub/Sub automatically retries until ack or max delivery attempts.
     - **Dead-letter topic** — after N failed attempts, route the message to a DLT for separate inspection/reprocessing.
     - **Exponential backoff + jitter** — configure retry policy to avoid thundering-herd retries.
     - **Idempotency** — ensure retried processing is safe (dedup/upserts).

     ```bash
     gcloud pubsub subscriptions update orders-sub \
         --min-retry-delay=10s --max-retry-delay=600s
     ```

     A separate handler then processes DLT messages — fixing data, alerting, or discarding as appropriate.

     **[⬆ Back to Top](#table-of-contents)**


## DevOps, CI/CD and Infrastructure as Code

184. ### What is Cloud Build?

     **Cloud Build** is a fully managed **CI/CD** service that runs your build steps in containers. You define steps in a `cloudbuild.yaml` — building Docker images, running tests, deploying to Cloud Run/GKE. It integrates with **Cloud Source Repositories, GitHub, Bitbucket**, and **Artifact Registry**. Builds run in isolated worker VMs and can be triggered by commits, tags, or manually.

     ```yaml
     steps:
     - name: 'gcr.io/cloud-builders/mvn'
       args: ['clean', 'package']
     - name: 'gcr.io/cloud-builders/docker'
       args: ['build', '-t', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA', '.']
     images: ['us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA']
     ```

     **[⬆ Back to Top](#table-of-contents)**

185. ### How does Cloud Build work with source repositories?

     You configure **build triggers** that start a build when code is **pushed to a branch or tag**. The trigger references a `cloudbuild.yaml` or `Dockerfile` in the repo. Cloud Build **clones the repo at the specified commit**, runs the steps, and stores artifacts in **Artifact Registry** or Cloud Storage. Logs appear in the Console and Cloud Logging.

     ```bash
     gcloud builds triggers create github \
         --repo-name=my-repo --repo-owner=my-org \
         --branch-pattern="^main$" --build-config=cloudbuild.yaml
     ```

     **[⬆ Back to Top](#table-of-contents)**

186. ### What is a cloudbuild.yaml file?

     `cloudbuild.yaml` (or `.json`) **defines the build pipeline** as a sequence of **steps**, each with a container image and arguments. It supports environment variables, secret management, and substitutions (`$PROJECT_ID`, `$COMMIT_SHA`, `$BUILD_ID`). Steps run **sequentially** by default (use `waitFor` for parallelism).

     ```yaml
     steps:
     - name: 'gcr.io/cloud-builders/mvn'
       args: ['test']
     - name: 'gcr.io/cloud-builders/mvn'
       args: ['clean', 'package', '-DskipTests']
     - name: 'gcr.io/cloud-builders/docker'
       args: ['build', '-t', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA', '.']
     images: ['us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA']
     options:
       machineType: 'E2_HIGHCPU_8'
     ```

     **[⬆ Back to Top](#table-of-contents)**

187. ### How do you build and push a Docker image to Artifact Registry?

     Use Cloud Build or the `gcloud`/`docker` CLI:

     ```bash
     # Authenticate Docker to Artifact Registry
     gcloud auth configure-docker us-central1-docker.pkg.dev

     # Build, tag, and push
     docker build -t us-central1-docker.pkg.dev/my-project/my-repo/app:v1 .
     docker push us-central1-docker.pkg.dev/my-project/my-repo/app:v1
     ```

     Create the repository first if needed:

     ```bash
     gcloud artifacts repositories create my-repo \
         --repository-format=docker --location=us-central1
     ```

     Artifact Registry stores images securely with fine-grained IAM and vulnerability scanning.

     **[⬆ Back to Top](#table-of-contents)**

188. ### What is Artifact Registry?

     **Artifact Registry** is the unified repository service for storing **container images, language packages** (npm, Maven, Python), and **OCI artifacts**. It replaces Container Registry and offers **regional/multi-regional** repositories, **fine-grained IAM**, **vulnerability scanning**, and **CMEK encryption**. It integrates with Cloud Build, Cloud Deploy, and GKE.

     ```bash
     # Maven repository for Java artifacts
     gcloud artifacts repositories create java-libs \
         --repository-format=maven --location=us-central1
     ```

     **[⬆ Back to Top](#table-of-contents)**

189. ### How is Artifact Registry different from Container Registry?

     | | Container Registry (legacy) | Artifact Registry |
     | --- | --- | --- |
     | **Storage** | Single GCS bucket (`gcr.io`) | Separate per-format repositories |
     | **IAM** | Coarse (bucket-level) | Fine-grained per repository |
     | **Formats** | Docker only | Docker, Maven, npm, Python, OCI |
     | **Location** | Multi-regional only | Regional or multi-regional |
     | **Features** | Basic | Vulnerability scanning, CMEK |

     **Container Registry is deprecated** — use **Artifact Registry** for new work. It provides better security, regional control, and multi-format support.

     **[⬆ Back to Top](#table-of-contents)**

190. ### What is Cloud Deploy?

     **Cloud Deploy** is a managed **continuous delivery** service for deploying to **GKE, Cloud Run, and Anthos**. You define **delivery pipelines** (stages and targets); Cloud Deploy orchestrates **rollouts, approvals, and rollbacks**. It integrates with Cloud Build for artifacts and supports **blue-green and canary** strategies with metrics-based promotion.

     ```yaml
     # clouddeploy.yaml — pipeline with dev → staging → prod
     apiVersion: deploy.cloud.google.com/v1
     kind: DeliveryPipeline
     metadata:
       name: order-api-pipeline
     serialPipeline:
       stages:
       - targetId: dev
       - targetId: staging
       - targetId: prod
         strategy:
           canary:
             runtimeConfig:
               cloudRun: {}
             canaryDeployment:
               percentages: [10, 50]
     ```

     **[⬆ Back to Top](#table-of-contents)**

191. ### How do you implement progressive delivery using Cloud Deploy?

     Define a pipeline with **multiple stages** (dev, staging, prod) and **targets** (clusters/regions), then configure **rollout strategies**:

     - **Canary** — deploy to e.g. 10% of traffic, wait for metrics/approval, then 50%, then 100%.
     - **Blue-green** — deploy a new "green" set, verify, switch traffic.

     Cloud Deploy monitors **Cloud Monitoring** metrics and can **auto-abort/roll back** if SLOs are violated. **Approval gates** require a human to promote between stages.

     **[⬆ Back to Top](#table-of-contents)**

192. ### How do you deploy a Cloud Run service using Cloud Build?

     Add a build step that runs `gcloud run deploy` after building the image:

     ```yaml
     steps:
     - name: 'gcr.io/cloud-builders/docker'
       args: ['build', '-t', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$BUILD_ID', '.']
     - name: 'gcr.io/cloud-builders/docker'
       args: ['push', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$BUILD_ID']
     - name: 'gcr.io/google.com/cloudsdktool/cloud-sdk'
       entrypoint: gcloud
       args:
       - 'run'
       - 'deploy'
       - 'order-api'
       - '--image=us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$BUILD_ID'
       - '--region=us-central1'
       - '--platform=managed'
       - '--allow-unauthenticated'
     ```

     **[⬆ Back to Top](#table-of-contents)**

193. ### How do you deploy to GKE using a CI/CD pipeline?

     Build and push the image, then apply manifests via `kubectl` (authenticated through Workload Identity or `get-credentials`):

     ```yaml
     steps:
     - name: 'gcr.io/cloud-builders/docker'
       args: ['build', '-t', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA', '.']
     - name: 'gcr.io/cloud-builders/docker'
       args: ['push', 'us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA']
     - name: 'gcr.io/cloud-builders/gke-deploy'
       args:
       - 'run'
       - '--filename=k8s/'
       - '--image=us-central1-docker.pkg.dev/$PROJECT_ID/repo/app:$COMMIT_SHA'
       - '--cluster=my-cluster'
       - '--location=us-central1'
     ```

     For production, prefer **GitOps** with **Cloud Deploy** or **Argo CD** managing manifests declaratively.

     **[⬆ Back to Top](#table-of-contents)**

194. ### What is Infrastructure as Code?

     **Infrastructure as Code (IaC)** means defining infrastructure (VMs, networks, IAM, DNS) in **declarative configuration files** managed via version control. Tools like **Terraform**, **Infrastructure Manager**, and **Pulumi** provision and update resources consistently across environments. IaC improves **reproducibility, reviewability, and automation** — infrastructure changes go through pull requests like application code.

     **[⬆ Back to Top](#table-of-contents)**

195. ### How do you use Terraform with Google Cloud?

     Configure the Google provider and define resources in `.tf` files:

     ```hcl
     provider "google" {
       project = var.project_id
       region  = var.region
     }

     resource "google_storage_bucket" "data" {
       name          = "${var.project_id}-data"
       location      = "US"
       storage_class = "STANDARD"
       versioning { enabled = true }
     }

     resource "google_cloud_run_v2_service" "api" {
       name     = "order-api"
       location = var.region
       template {
         containers {
           image = "us-central1-docker.pkg.dev/${var.project_id}/repo/app:v1"
         }
       }
     }
     ```

     Run `terraform init`, `terraform plan`, `terraform apply`. Store state in a **remote backend** (GCS) for collaboration.

     **[⬆ Back to Top](#table-of-contents)**

196. ### What is a Terraform provider for Google Cloud?

     A **Terraform provider** is a plugin that knows how to **create, read, update, and delete** resources via a platform's APIs. The **`google`** provider manages GCP resources; the **`google-beta`** provider exposes preview/beta features. Providers handle authentication, translate config to API calls, and track state. You can combine providers (e.g., `google`, `kubernetes`, `helm`) in one configuration.

     ```hcl
     terraform {
       required_providers {
         google = { source = "hashicorp/google", version = "~> 5.0" }
       }
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

197. ### How do you manage Terraform state for GCP projects?

     Store state in a **remote backend** — typically a **Cloud Storage bucket** — with **state locking** to prevent concurrent modifications:

     ```hcl
     terraform {
       backend "gcs" {
         bucket = "my-project-tfstate"
         prefix = "prod/backend"
       }
     }
     ```

     Best practices: **enable versioning** on the state bucket, use **separate state files/workspaces** per environment, and **restrict IAM** on the bucket since state can contain sensitive values.

     **[⬆ Back to Top](#table-of-contents)**

198. ### What is Infrastructure Manager in Google Cloud?

     **Infrastructure Manager** is a managed service for **deploying infrastructure using Terraform** (it runs and manages Terraform for you on GCP). It stores state, manages execution, and integrates with IAM and source repos — giving you a managed IaC workflow without self-hosting Terraform runners. (Its predecessor, **Config Controller**, used Config Connector/KRM to reconcile GCP resources declaratively via Kubernetes Custom Resources, GitOps-style.)

     **[⬆ Back to Top](#table-of-contents)**

199. ### How do you manage secrets in CI/CD pipelines?

     Use **Secret Manager** (never plaintext in repos). In Cloud Build, reference secrets via `availableSecrets`:

     ```yaml
     steps:
     - name: 'gcr.io/cloud-builders/mvn'
       entrypoint: bash
       args: ['-c', 'mvn deploy -Drepo.password=$$REPO_PASSWORD']
       secretEnv: ['REPO_PASSWORD']
     availableSecrets:
       secretManager:
       - versionName: projects/$PROJECT_ID/secrets/repo-password/versions/latest
         env: 'REPO_PASSWORD'
     ```

     Best practices: **restrict IAM** on secrets, avoid echoing secrets to logs, and rotate them regularly.

     **[⬆ Back to Top](#table-of-contents)**

200. ### How do you handle environment-specific configuration in GCP deployments?

     - **Parameterize** with variables — Terraform `var.env`, Cloud Build/Deploy **substitutions**, or per-environment YAML.
     - **Externalize config** — store values (DB names, endpoints) in **Secret Manager** or Kubernetes **ConfigMaps**, referenced at runtime.
     - **Reuse modules/overlays** — avoid duplicating resource definitions; use Terraform modules or Kustomize overlays per environment.

     ```hcl
     # Terraform: environment-driven sizing
     locals {
       machine_type = var.env == "prod" ? "n2-standard-4" : "e2-small"
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

201. ### How do you implement rollback in a GCP deployment pipeline?

     Plan rollback at both **application** and **infrastructure** levels:

     - **Application** — keep previous **image versions** in Artifact Registry; redeploy the prior tag. Cloud Run keeps **revisions** you can route traffic back to; GKE supports `kubectl rollout undo`.
     - **Cloud Deploy** — use its built-in **rollback** to a prior release.
     - **Infrastructure** — revert the Terraform config (Git) and `apply`, or restore a previous state.

     ```bash
     # Cloud Run — shift 100% traffic back to the previous revision
     gcloud run services update-traffic order-api --to-revisions=order-api-00041-abc=100
     # GKE
     kubectl rollout undo deployment/order-api
     ```

     Always **test rollbacks in staging**.

     **[⬆ Back to Top](#table-of-contents)**

202. ### How do you enforce approvals before production deployment?

     - **Cloud Deploy approval gates** — require designated approvers to **manually approve** before a rollout promotes to prod.
     - **Cloud Build approvals** — pause a trigger until approved.
     - **GitHub PR reviews** — require code review/approval before merge triggers deploy.
     - **Custom logic** — Cloud Functions reacting to Cloud Build Pub/Sub events.

     ```bash
     # A Cloud Deploy target requiring approval
     gcloud deploy targets create prod --require-approval --region=us-central1
     ```

     **[⬆ Back to Top](#table-of-contents)**

203. ### How do you design a CI/CD pipeline for a Spring Boot microservice on GCP?

     A representative pipeline:

     1. **Source** — code in GitHub; a push to `main` triggers Cloud Build.
     2. **Build** — `mvn clean package` builds the JAR; Docker builds the image; push to **Artifact Registry**.
     3. **Test** — run unit/integration tests (Testcontainers for DB).
     4. **Deploy** — **Cloud Deploy** rolls the image to Cloud Run or GKE.
     5. **Approval** — manual approval gate for production.
     6. **Rollback** — keep previous image tags/revisions for instant rollback if metrics degrade.

     ```yaml
     # cloudbuild.yaml (abridged)
     steps:
     - { name: 'gcr.io/cloud-builders/mvn', args: ['clean','verify'] }
     - { name: 'gcr.io/cloud-builders/docker', args: ['build','-t','us-central1-docker.pkg.dev/$PROJECT_ID/repo/svc:$COMMIT_SHA','.'] }
     - { name: 'gcr.io/cloud-builders/docker', args: ['push','us-central1-docker.pkg.dev/$PROJECT_ID/repo/svc:$COMMIT_SHA'] }
     - { name: 'gcr.io/google.com/cloudsdktool/cloud-sdk', entrypoint: gcloud,
         args: ['deploy','releases','create','rel-$SHORT_SHA','--delivery-pipeline=svc-pipeline','--region=us-central1','--images=svc=us-central1-docker.pkg.dev/$PROJECT_ID/repo/svc:$COMMIT_SHA'] }
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Observability, Logging, Monitoring and SRE

204. ### What is Cloud Logging?

     **Cloud Logging** collects logs from GCP services, Compute Engine VMs, GKE containers, and custom applications. Logs are stored in **log buckets** and queried via the **Logs Explorer**. You can create **log sinks** to route logs to **BigQuery, Pub/Sub, or Cloud Storage** for analysis or long-term retention. It supports **structured (JSON) logs** and integrates with Monitoring and Error Reporting.

     ```java
     // Structured logging from Java (Logback + Cloud Logging appender or stdout JSON)
     Logger logger = LoggerFactory.getLogger(OrderService.class);
     logger.info("Order processed: orderId={}, amount={}", orderId, amount);
     ```

     **[⬆ Back to Top](#table-of-contents)**

205. ### What is Cloud Monitoring?

     **Cloud Monitoring** collects **metrics, events, and metadata** from GCP services and instrumentation libraries (OpenTelemetry, Prometheus). It lets you build **dashboards**, define **alerting policies**, and analyze system health. It supports **uptime checks, custom metrics, and multi-cloud** resources, and integrates with Logging, Trace, and Profiler for a full observability stack.

     **[⬆ Back to Top](#table-of-contents)**

206. ### What are log-based metrics?

     **Log-based metrics** are metrics **derived from log entries**. You define a filter selecting matching logs (e.g., HTTP 500 errors) and create a metric that **counts or measures** those events. These metrics can drive **alerts** and **dashboards**, turning unstructured logs into actionable signals.

     ```bash
     gcloud logging metrics create error5xx \
         --description="Count of 5xx responses" \
         --log-filter='resource.type="cloud_run_revision" AND httpRequest.status>=500'
     ```

     **[⬆ Back to Top](#table-of-contents)**

207. ### What are uptime checks?

     **Uptime checks** monitor endpoint **availability** (HTTP/HTTPS/TCP) from **multiple global locations**. Cloud Monitoring periodically probes the endpoint, recording response codes and latency. You attach **alerting policies** to uptime-check failures to notify on-call teams of outages.

     ```bash
     gcloud monitoring uptime create my-api-check \
         --resource-type=uptime-url --resource-labels=host=api.example.com \
         --path=/healthz --port=443
     ```

     **[⬆ Back to Top](#table-of-contents)**

208. ### What are alerting policies in Cloud Monitoring?

     An **alerting policy** defines conditions that trigger **incidents** when metrics cross thresholds (e.g., CPU > 80% for 5 minutes, error rate spikes). Policies specify **notification channels** (email, PagerDuty, Slack) and documentation. Conditions can be combined with AND/OR logic. When violated, Monitoring creates an incident and notifies the team.

     **[⬆ Back to Top](#table-of-contents)**

209. ### What is Cloud Trace?

     **Cloud Trace** is a **distributed tracing** system capturing latency data across services. It records **traces and spans** for RPC calls and functions, showing where time is spent. It integrates with **OpenTelemetry** and language instrumentation (Java, Go, Node.js), helping you find bottlenecks and optimize latency in microservice call chains.

     ```java
     // OpenTelemetry auto-instruments Spring Boot; spans export to Cloud Trace
     // Add the OpenTelemetry Java agent and configure the GCP exporter
     ```

     **[⬆ Back to Top](#table-of-contents)**

210. ### What is Cloud Profiler?

     **Cloud Profiler** continuously samples **CPU and heap usage** from production applications with low overhead. It produces **flame graphs** showing which functions consume the most CPU time or memory, helping you pinpoint performance hotspots without significant impact. It supports Java, Go, Node.js, and Python.

     **[⬆ Back to Top](#table-of-contents)**

211. ### What is Error Reporting?

     **Error Reporting** aggregates and **groups application errors** (uncaught exceptions, stack traces) across services. It **de-duplicates** similar errors and shows frequency, affected versions, and first/last occurrence. You can alert on new or high-severity errors. It integrates with Cloud Logging and uses source maps for JavaScript stack traces.

     **[⬆ Back to Top](#table-of-contents)**

212. ### How do you monitor a Cloud Run service?

     Cloud Run emits built-in metrics: **request count, latency, CPU/memory usage, and instance count**. To monitor:

     - Build **Cloud Monitoring dashboards** and **alerting policies** (e.g., high latency, 5xx rate).
     - Use **Cloud Logging** for request and application logs.
     - Instrument with **OpenTelemetry** to export custom metrics and traces to Monitoring and Trace.

     ```bash
     # Alert on p99 latency > 1s (illustrative)
     gcloud monitoring policies create --policy-from-file=latency-alert.yaml
     ```

     **[⬆ Back to Top](#table-of-contents)**

213. ### How do you monitor a GKE workload?

     - Enable **GKE Workload Metrics** or run the **managed Prometheus / metrics agent** to export pod/container CPU, memory, disk, and network metrics.
     - Visualize in **Cloud Monitoring dashboards** or **Grafana**.
     - Use **Cloud Logging's GKE integration** to collect container stdout/stderr.
     - Add **Cloud Trace** and **Cloud Profiler** for distributed tracing and profiling.

     ```bash
     gcloud container clusters update my-cluster --region=us-central1 \
         --enable-managed-prometheus
     ```

     **[⬆ Back to Top](#table-of-contents)**

214. ### How do you define SLI, SLO and SLA?

     | Term | Definition | Example |
     | --- | --- | --- |
     | **SLI** (Indicator) | A measured aspect of service quality | Request latency, availability |
     | **SLO** (Objective) | A target value for an SLI over time | 99.9% of requests < 300 ms |
     | **SLA** (Agreement) | A contract with consequences if SLOs aren't met | Credits if availability < 99.9% |

     **SLIs** are what you measure, **SLOs** are your internal targets, and **SLAs** are the external promises (with penalties). SLAs are typically looser than internal SLOs to provide a safety margin.

     **[⬆ Back to Top](#table-of-contents)**

215. ### What is an error budget?

     An **error budget** is the **allowable amount of failure**, defined as **1 − SLO**. For a 99.9% availability SLO, the error budget is **0.1%** of the time window. Teams use it to balance **feature velocity vs. reliability**: if the budget is healthy, ship features faster; if nearly exhausted, prioritize stability and freeze risky changes.

     **[⬆ Back to Top](#table-of-contents)**

216. ### How do you troubleshoot high latency in a GCP backend service?

     1. **Cloud Monitoring** — identify which resource (CPU, memory, network) is saturated.
     2. **Cloud Trace** — see where time is spent in the request path (slow downstream calls).
     3. **Cloud Profiler** — find CPU/memory hotspots in code.
     4. **Logs** — check for errors, slow queries, GC pauses (for Java, watch for long GC).
     5. **Dependencies** — inspect databases and third-party APIs; optimize queries, add caching, tune concurrency/connection pools.

     **[⬆ Back to Top](#table-of-contents)**

217. ### How do you troubleshoot increased 5xx errors behind a load balancer?

     1. **Filter LB logs** in Cloud Logging for 5xx and identify the failing backend.
     2. **Check backend health checks** — unhealthy instances return 5xx until removed.
     3. **Inspect application logs** for exceptions or OOM.
     4. **Check capacity** — the autoscaler may not be scaling fast enough; raise min instances.
     5. **Validate networking** — firewall rules, DNS, and SSL certificate configuration.

     ```bash
     gcloud logging read 'resource.type="http_load_balancer" AND httpRequest.status>=500' --limit=50
     ```

     **[⬆ Back to Top](#table-of-contents)**

218. ### How do you correlate application logs with request IDs?

     Generate a **unique request ID (UUID)** at the edge and include it in **structured logs**, **propagating it** through downstream services via HTTP headers (e.g., `X-Request-Id`). Then filter by that ID across services in the Logs Explorer. GCP also associates a **trace ID** with each Cloud Run/LB request, letting you link logs to traces in Cloud Trace.

     ```java
     // Spring Boot: put a request ID into MDC for structured logs
     String requestId = Optional.ofNullable(request.getHeader("X-Request-Id"))
         .orElse(UUID.randomUUID().toString());
     MDC.put("requestId", requestId);   // appears in every log line for this request
     ```

     **[⬆ Back to Top](#table-of-contents)**

219. ### How do you design observability for microservices on GCP?

     - **Instrument with OpenTelemetry** — collect metrics, logs, and traces uniformly.
     - **Structured logging** — use severity, component, and trace IDs (semantic conventions).
     - **Dashboards** in Cloud Monitoring for service health and SLOs.
     - **Log-based metrics + alerting policies** for critical events.
     - **Cloud Trace** for distributed traces; **Cloud Profiler** for hotspots.
     - **Error Reporting** with actionable alerts.

     The goal is the **three pillars** (metrics, logs, traces) correlated via trace IDs so you can move from a dashboard alert to the exact failing request and code path.

     **[⬆ Back to Top](#table-of-contents)**


## Security and Compliance

220. ### What is Secret Manager?

     **Secret Manager** stores and manages **sensitive data** — API keys, passwords, certificates. Secrets are **encrypted at rest**, access-controlled via **IAM**, and **versioned**. Applications retrieve secrets via API, `gcloud`, or client libraries. It supports **automatic rotation** via Cloud Functions/Scheduler.

     ```java
     // Access a secret version from Java
     try (SecretManagerServiceClient client = SecretManagerServiceClient.create()) {
         SecretVersionName name = SecretVersionName.of("my-project", "db-password", "latest");
         String secret = client.accessSecretVersion(name).getPayload().getData().toStringUtf8();
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

221. ### Why should secrets not be stored in environment variables or source code?

     Storing secrets in **env vars or code** exposes them to:

     - **Version control history** — secrets persist forever once committed.
     - **Logs and process listings** — env vars can leak via `ps`, crash dumps, or log output.
     - **Unauthorized access** — anyone with repo or runtime access sees them.

     Use **Secret Manager** (or a vault) to centralize **access control, auditing, and rotation**. Inject secrets at runtime rather than baking them in.

     **[⬆ Back to Top](#table-of-contents)**

222. ### How do you rotate secrets in Secret Manager?

     1. **Create a new secret version** with the updated value.
     2. **Update applications** to fetch `latest` (or a specific version).
     3. **Verify** the new version works everywhere.
     4. **Disable/destroy** old versions when no longer used.

     Automate with **Cloud Functions/Scheduler** that create new versions and update dependent configs.

     ```bash
     echo -n "new-password" | gcloud secrets versions add db-password --data-file=-
     gcloud secrets versions disable 1 --secret=db-password   # disable old version
     ```

     **[⬆ Back to Top](#table-of-contents)**

223. ### What is Cloud KMS?

     **Cloud Key Management Service (KMS)** manages **cryptographic keys** — create, rotate, and destroy symmetric/asymmetric keys. It integrates with GCP services to **encrypt data at rest** using customer-managed keys, supports **HSM-backed** keys (Cloud HSM), and can **encrypt/decrypt or sign/verify** data via API.

     ```bash
     gcloud kms keyrings create my-keyring --location=us-central1
     gcloud kms keys create my-key --keyring=my-keyring \
         --location=us-central1 --purpose=encryption --rotation-period=90d --next-rotation-time=...
     ```

     **[⬆ Back to Top](#table-of-contents)**

224. ### What is the difference between Google-managed keys and customer-managed encryption keys?

     | | Google-managed Keys | Customer-managed (CMEK) |
     | --- | --- | --- |
     | **Control** | Google handles everything | You create/manage in Cloud KMS |
     | **Rotation** | Automatic, opaque | You set schedules and policies |
     | **Revocation** | Not possible | Disable/destroy key to render data unusable |
     | **Use case** | Default encryption | Compliance requiring key control |

     **Google-managed keys** encrypt data by default with zero effort. **CMEK** gives you control over the key lifecycle and the ability to revoke access — required when regulations mandate customer key control.

     **[⬆ Back to Top](#table-of-contents)**

225. ### What is CMEK?

     **CMEK (Customer-Managed Encryption Key)** lets you encrypt data in GCP services (Cloud Storage, BigQuery, Pub/Sub, Persistent Disk, etc.) with **keys you create and control in Cloud KMS**. You specify the key when creating a resource. CMEK lets you **revoke access** by disabling the key and satisfies **compliance** requirements for key ownership.

     ```bash
     # Create a CMEK-encrypted bucket
     gcloud storage buckets create gs://secure-bucket \
         --location=us-central1 \
         --default-encryption-key=projects/my-project/locations/us-central1/keyRings/my-keyring/cryptoKeys/my-key
     ```

     **[⬆ Back to Top](#table-of-contents)**

226. ### What is VPC Service Controls?

     **VPC Service Controls** create a **security perimeter** around GCP resources to **mitigate data exfiltration**. They restrict how resources inside the perimeter communicate with those outside — even if IAM would otherwise allow it. You define **service perimeters** around projects and restrict access to sensitive services (Cloud Storage, BigQuery), blocking unauthorized data transfer.

     **[⬆ Back to Top](#table-of-contents)**

227. ### How does VPC Service Controls reduce data exfiltration risk?

     By creating a **service perimeter**, you **limit API calls** from outside the perimeter to services inside it and **control egress** from inside to outside. Even if an attacker **steals valid credentials**, they cannot copy data to an external project or service because the perimeter **denies cross-boundary calls**. It integrates with **Access Context Manager** to enforce conditions like device policy and IP allow-lists.

     **[⬆ Back to Top](#table-of-contents)**

228. ### What is Security Command Center?

     **Security Command Center (SCC)** is a centralized **security and risk management** platform. It continuously scans projects for **vulnerabilities** (open buckets, unencrypted disks), **misconfigurations**, and **threats**. It consolidates findings from Web Security Scanner, Security Health Analytics, Event Threat Detection, and third-party sources into a single dashboard, helping you prioritize and remediate risks.

     **[⬆ Back to Top](#table-of-contents)**

229. ### What is Binary Authorization?

     **Binary Authorization** ensures **only trusted container images** are deployed to GKE or Cloud Run. It uses **attestors** to sign images and **policies** specifying which attestations are required. At deploy time, it **verifies signatures** before allowing the image to run, preventing deployment of unverified or tampered images — a supply-chain security control.

     **[⬆ Back to Top](#table-of-contents)**

230. ### How does Binary Authorization secure container deployments?

     You define a **policy** requiring specific **attestations** (e.g., from the CI pipeline and vulnerability scanning). Each **attestor signs the image digest** after its check passes. When a deployment is attempted, Binary Authorization **checks the image's signatures**: if all required attestations are present, the deployment proceeds; otherwise it's **denied**. This guarantees only images that passed your validations reach production.

     ```bash
     gcloud container binauthz attestors create build-attestor \
         --attestation-authority-note=build-note --attestation-authority-note-project=my-project
     ```

     **[⬆ Back to Top](#table-of-contents)**

231. ### What is Container Analysis?

     **Container Analysis** provides **metadata and vulnerability scanning** for container images in Artifact Registry / Container Registry. It automatically scans images for **known vulnerabilities** and attaches findings as metadata. You can query vulnerability occurrences, subscribe to **Pub/Sub notifications**, and enforce policies via **Binary Authorization**.

     **[⬆ Back to Top](#table-of-contents)**

232. ### What is vulnerability scanning in Artifact Registry?

     **Artifact Registry** integrates **vulnerability scanning** (via Container Analysis). When you push an image, it's scanned against vulnerability databases (OS and language packages). Findings include **severity, CVE identifiers, and remediation suggestions**, viewable in the Console or via API. Scanning supports supply-chain security and informs patching priorities.

     ```bash
     gcloud artifacts docker images scan \
         us-central1-docker.pkg.dev/my-project/repo/app:v1
     ```

     **[⬆ Back to Top](#table-of-contents)**

233. ### How do you secure a public API deployed on Cloud Run?

     - **HTTPS/TLS** — automatic via Cloud Run or Cloud Load Balancing managed certs.
     - **AuthN/AuthZ** — use **Identity-Aware Proxy (IAP)**, **API Gateway**, or **Cloud Endpoints** to enforce JWT validation and quotas.
     - **Rate limiting** — via **Cloud Armor** or API Gateway.
     - **IAM** — restrict who can invoke with `roles/run.invoker`.
     - **Monitoring** — watch logs/metrics for abuse and alert.

     ```bash
     gcloud run services add-iam-policy-binding order-api \
         --member="serviceAccount:gateway@my-project.iam.gserviceaccount.com" \
         --role="roles/run.invoker" --region=us-central1
     ```

     **[⬆ Back to Top](#table-of-contents)**

234. ### How do you protect backend APIs from DDoS and abusive traffic?

     - **Cloud Armor** — WAF rules, IP/geo blocking, and **Adaptive Protection** (ML-based anomaly detection) to mitigate DDoS.
     - **Global HTTP(S) LB + Cloud CDN** — absorb and distribute traffic at Google's edge.
     - **Rate limits/quotas** — in API Gateway or Cloud Endpoints.
     - **Autoscaling** — handle legitimate spikes; alert on anomalies.

     Google's network infrastructure inherently helps absorb large **volumetric** attacks before they reach your backends.

     **[⬆ Back to Top](#table-of-contents)**

235. ### How do you audit access to sensitive resources in GCP?

     - Enable **Cloud Audit Logs** (Admin Activity + Data Access) on critical services.
     - Use **Cloud Asset Inventory** to query who has access to what.
     - **Export audit logs to BigQuery** for retention and analysis.
     - Use **IAM Recommender** to find and remove over-privileged principals.
     - Conduct **periodic IAM reviews** and service-account audits.
     - Add **VPC Service Controls** and **Access Context Manager** for extra constraints.

     ```sql
     -- BigQuery: find who accessed a sensitive bucket
     SELECT timestamp, protopayload_auditlog.authenticationInfo.principalEmail, protopayload_auditlog.methodName
     FROM `my-project.audit_logs.cloudaudit_googleapis_com_data_access`
     WHERE resource.labels.bucket_name = 'sensitive-bucket'
     ORDER BY timestamp DESC;
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Data, Analytics and AI Integration

236. ### What is BigQuery?

     **BigQuery** is a fully managed, **serverless data warehouse**. It stores structured data in **columnar format** and runs **SQL queries** with automatic scaling and high performance. It **separates storage and compute** — you pay for storage used and bytes processed per query. It integrates with Cloud Storage, Dataflow, and Pub/Sub, supports **federated queries, streaming ingest, and BigQuery ML**.

     ```java
     // Run a query with the BigQuery Java client
     BigQuery bigquery = BigQueryOptions.getDefaultInstance().getService();
     QueryJobConfiguration query = QueryJobConfiguration.newBuilder(
         "SELECT product, SUM(amount) total FROM `my-project.sales.orders` GROUP BY product").build();
     TableResult result = bigquery.query(query);
     result.iterateAll().forEach(row -> System.out.println(row.get("product").getStringValue()));
     ```

     **[⬆ Back to Top](#table-of-contents)**

237. ### When would you use BigQuery instead of Cloud SQL?

     Use **BigQuery** for **analytical workloads** over large datasets (TB–PB): complex aggregations, ad-hoc queries, and reporting. It excels at scanning massive tables quickly. Use **Cloud SQL** for **OLTP** — transactional apps with many small row-level reads/writes and relational constraints.

     | | BigQuery | Cloud SQL |
     | --- | --- | --- |
     | **Workload** | OLAP / analytics | OLTP / transactions |
     | **Scale** | Petabytes | Tens of TB |
     | **Writes** | Bulk/streaming inserts | Frequent small writes |
     | **Latency** | Seconds (big scans) | Milliseconds (row ops) |

     **[⬆ Back to Top](#table-of-contents)**

238. ### What is partitioning in BigQuery?

     **Partitioning** divides a table into segments based on a **column** (date/time, integer range) or **ingestion time**. Queries that filter on the partition key scan **only relevant partitions**, reducing cost and improving performance. Common strategies: ingestion-time partitioning and column-based (e.g., `PARTITION BY DATE(event_time)`).

     ```sql
     CREATE TABLE sales.orders (order_id STRING, amount NUMERIC, event_time TIMESTAMP)
     PARTITION BY DATE(event_time);
     -- Queries filtering on event_time scan only matching date partitions
     ```

     **[⬆ Back to Top](#table-of-contents)**

239. ### What is clustering in BigQuery?

     **Clustering** organizes data **within partitions** by one or more **clustering columns**, storing it in sorted blocks. When queries filter on clustering columns, BigQuery reads **fewer blocks**, improving performance and cost. Clustering works alongside partitioning — cluster on dimensions commonly used in filters/joins (e.g., user ID, country).

     ```sql
     CREATE TABLE sales.orders (order_id STRING, user_id STRING, country STRING, event_time TIMESTAMP)
     PARTITION BY DATE(event_time)
     CLUSTER BY country, user_id;
     ```

     **[⬆ Back to Top](#table-of-contents)**

240. ### What is Dataflow?

     **Dataflow** is a fully managed **stream and batch** processing service based on **Apache Beam**. It executes Beam pipelines with **automatic scaling and optimization**. Used for ETL, real-time analytics, and event processing, it integrates with Pub/Sub (streaming), BigQuery, Cloud Storage, Spanner, and Bigtable. You write pipelines in **Java** or Python; Dataflow handles provisioning.

     ```java
     // Apache Beam pipeline (Java) — read from Pub/Sub, write to BigQuery
     Pipeline p = Pipeline.create(options);
     p.apply(PubsubIO.readStrings().fromTopic("projects/my-project/topics/orders"))
      .apply(ParDo.of(new ParseOrderFn()))
      .apply(BigQueryIO.writeTableRows().to("my-project:sales.orders")
          .withWriteDisposition(WriteDisposition.WRITE_APPEND));
     p.run();
     ```

     **[⬆ Back to Top](#table-of-contents)**

241. ### How is Dataflow related to Apache Beam?

     **Apache Beam** is an open-source **unified programming model** for batch and streaming, defining pipelines with transforms (`ParDo`, `GroupByKey`, windowing) that run on multiple **runners** (Dataflow, Spark, Flink). **Dataflow is Google's hosted Beam runner**, providing autoscaling, dynamic work rebalancing, and deep GCP integration. You write Beam code once and run it on Dataflow without managing clusters.

     **[⬆ Back to Top](#table-of-contents)**

242. ### What is Dataproc?

     **Dataproc** is a managed **Spark and Hadoop** service that provisions clusters quickly and bills **by the second**. It supports Spark, Hadoop, Hive, Pig, and Presto, automates cluster management, and integrates with Cloud Storage, BigQuery, and Vertex AI. It's ideal for **batch processing, ETL, and ML** workloads that rely on the open-source big-data ecosystem (e.g., lift-and-shift of existing Spark jobs).

     **[⬆ Back to Top](#table-of-contents)**

243. ### How can backend applications integrate with Vertex AI on GCP?

     **Vertex AI** is a unified platform to build, train, and deploy ML models. Backend integration:

     - **Online prediction** — call Vertex AI endpoints via REST/gRPC for real-time inference on deployed models.
     - **Custom training** — run training jobs on managed infrastructure.
     - **Pipelines** — orchestrate ML workflows.
     - **Generative AI** — call foundation models (Gemini) via the Vertex AI API.

     Use **service accounts and IAM** to secure access.

     ```java
     // Call a Vertex AI prediction endpoint (Java)
     try (PredictionServiceClient client = PredictionServiceClient.create(settings)) {
         EndpointName endpoint = EndpointName.of("my-project", "us-central1", "ENDPOINT_ID");
         PredictResponse response = client.predict(endpoint, instances, parameters);
         System.out.println(response.getPredictionsList());
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Architecture, Reliability, Cost and Migration

244. ### How do you design a highly available backend system on GCP?

     - **Load balancing** — regional/global load balancers across multiple zones/regions.
     - **Multi-zone compute** — deploy Compute Engine MIGs, GKE, or Cloud Run across at least two zones.
     - **Managed HA services** — Cloud SQL HA, Cloud Spanner, Filestore Enterprise.
     - **Replicated stateful data** + automated backups.
     - **Health checks, autoscaling, autohealing**, and tested failover.
     - **IaC + observability** — reproducible infra with alerting.

     ```bash
     # Regional GKE Autopilot cluster (control plane + nodes across 3 zones)
     gcloud container clusters create-auto prod-cluster --region=us-central1
     ```

     **[⬆ Back to Top](#table-of-contents)**

245. ### How do you design a multi-region disaster recovery architecture on GCP?

     - **Cross-region data replication** — Cloud Spanner multi-region or Cloud SQL cross-region read replicas.
     - **Multi-region storage** — multi-region Cloud Storage / Filestore Enterprise for durability.
     - **Stateless services in multiple regions** behind **global load balancers**.
     - **Regional message queues** — Pub/Sub stores data across regions.
     - **DNS failover** — Cloud DNS health checks or multi-region LB routing.
     - **Test failover regularly**; define and validate **RPO/RTO** targets.

     | Strategy | RTO | RPO | Cost |
     | --- | --- | --- | --- |
     | Backup & restore | Hours | Hours | Low |
     | Warm standby (active-passive) | Minutes | Seconds | Medium |
     | Active-active multi-region | Near-zero | Near-zero | High |

     **[⬆ Back to Top](#table-of-contents)**

246. ### What is the difference between active-active and active-passive architecture?

     | | Active-Active | Active-Passive |
     | --- | --- | --- |
     | **Traffic** | All regions serve concurrently | Primary serves; standby idle |
     | **Failover** | Automatic, near-instant | Promote standby (slower) |
     | **Complexity** | High (conflict resolution) | Lower |
     | **Cost** | Higher (all active) | Lower (standby) |
     | **Data** | Bidirectional replication | One-way replication |

     **Active-active** maximizes availability and can reduce latency by serving users locally, but requires conflict resolution. **Active-passive** is simpler and cheaper but has longer failover times and possible data loss equal to replication lag.

     **[⬆ Back to Top](#table-of-contents)**

247. ### How do you estimate and optimize cost for a GCP backend system?

     - **Estimate** with the **Pricing Calculator** (compute, storage, network).
     - **Discounts** — sustained use, committed use (1/3-year), and per-second billing.
     - **Right-size** — choose efficient machine types (E2, T2D); tune autoscaling to avoid overprovisioning.
     - **Spot VMs** — for fault-tolerant batch workloads.
     - **Storage classes** — Nearline/Coldline + lifecycle rules for cold data.
     - **Budgets & alerts** — Cloud Billing budgets to track spend.
     - **Scale to zero** — Cloud Run/Functions for spiky workloads.

     ```bash
     gcloud billing budgets create --billing-account=XXXX \
         --display-name="Prod Budget" --budget-amount=5000USD \
         --threshold-rule=percent=0.5 --threshold-rule=percent=0.9
     ```

     **[⬆ Back to Top](#table-of-contents)**

248. ### How do you migrate an on-premise Java application to GCP?

     1. **Assess** — architecture (stateful vs. stateless), dependencies, database, licensing.
     2. **Choose a strategy:**
        - **Lift-and-shift** → Compute Engine (fastest, least change).
        - **Containerize** → GKE or Cloud Run (modernize, better scaling).
        - **Refactor** → App Engine or serverless (most cloud-native).
     3. **Migrate the database** to Cloud SQL or Spanner using **Database Migration Service**.
     4. **Set up networking** (VPN/Interconnect) and **IAM**.
     5. **Use migration tooling** — Migrate to Virtual Machines or Migrate to Containers.
     6. **Test in staging**, then **cut over** with minimal downtime (e.g., DNS switch).

     ```bash
     # Example: containerize a Spring Boot app and deploy to Cloud Run
     gcloud run deploy legacy-app \
         --image=us-central1-docker.pkg.dev/my-project/repo/legacy-app:v1 \
         --region=us-central1 --vpc-connector=my-connector
     ```

     **[⬆ Back to Top](#table-of-contents)**

249. ### How do you choose between Compute Engine, GKE, Cloud Run and App Engine?

     | Service | Choose When |
     | --- | --- |
     | **Compute Engine** | Full OS control, custom software, stateful workloads, BYOL, lift-and-shift |
     | **GKE** | Kubernetes features (StatefulSets, DaemonSets, custom networking), existing K8s workloads |
     | **Cloud Run** | Stateless HTTP services/microservices, scale-to-zero, minimal ops |
     | **App Engine** | PaaS apps in supported runtimes, automatic versioning, task queues |

     **Decision flow:** Need OS-level control or stateful VMs → **Compute Engine**. Need Kubernetes orchestration → **GKE**. Stateless containers with minimal ops → **Cloud Run**. PaaS simplicity within runtime constraints → **App Engine**. For most new stateless microservices, **Cloud Run** is the default sweet spot.

     **[⬆ Back to Top](#table-of-contents)**

250. ### How would you design a scalable order management system on GCP?

     A reference design combining many services:

     | Layer | Choice |
     | --- | --- |
     | **Frontend/API** | Cloud Run or GKE behind a global HTTP(S) LB + Cloud Armor; API Gateway/Endpoints for auth & rate limiting |
     | **Eventing** | Pub/Sub topics for order events (created/paid/shipped); Eventarc triggers for Cloud Run |
     | **Microservices** | Inventory, Payment, Notification — each with its own subscription, idempotent consumers |
     | **Database** | Cloud SQL (read replicas) or Spanner for scale; orders & transactions |
     | **Caching** | Memorystore (Redis) for catalog and sessions |
     | **Storage** | Cloud Storage for invoices/receipts; signed URLs for access |
     | **Observability** | OpenTelemetry → Cloud Monitoring/Logging/Trace; alerts on latency & errors |
     | **Security** | IAM, Secret Manager, Cloud KMS, Cloud Armor; least privilege; Audit Logs |

     ```
     Client → HTTPS LB + Cloud Armor → Order API (Cloud Run)
                                           │ publish
                                           ▼
                                   Pub/Sub: order-events
                        ┌──────────────┼─────────────────┐
                        ▼              ▼                 ▼
                  Inventory Svc    Payment Svc     Notification Svc
                        │              │
                        ▼              ▼
                   Cloud SQL /     Cloud SQL (transactions)
                   Spanner          + Memorystore cache
     ```

     ```java
     // Order API: persist then publish an event atomically (outbox-style)
     @Transactional
     public void placeOrder(Order order) {
         orderRepository.save(order);               // 1. persist to Cloud SQL
         outboxRepository.save(new OutboxEvent(     // 2. write to outbox in same tx
             "ORDER_CREATED", order.getId(), toJson(order)));
     }
     // A separate publisher polls the outbox and publishes to Pub/Sub reliably
     ```

     This architecture **separates concerns, scales with demand, and leverages managed services** for resilience and operational efficiency.

     **[⬆ Back to Top](#table-of-contents)**

---

### Disclaimer

The questions and answers in this repository are a curated summary of commonly asked Google Cloud Platform interview questions. They cover concepts from foundational through advanced architecture-level depth. There is no guarantee that these exact questions will appear in any given interview — the purpose is to help you rapidly review key GCP concepts and build deep understanding across compute, storage, databases, networking, security, DevOps, and data/AI services. Contributions and corrections are welcome.

Good luck with your interview 😊

---
