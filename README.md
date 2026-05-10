# .github
# 🛠️ veloxamen Project
**Next-Generation Cloud-Native Forensic Pipeline**
The name **veloxamen** is a portmanteau of **Velox** (Latin for "swift/fast") and **Examen** (Latin for "examination/investigation"). True to its name, this project aims to automate and accelerate the entire digital forensics workflow leveraging cloud-native architectures.

---

### 📋 Project Roadmap

Currently in **Phase 2 (Testing)**. Following a successful PoC on AWS, the project has shifted to Google Cloud Platform (GCP) to achieve higher processing efficiency and deeper integration with BigQuery.

#### **Phase 1: Local to Cloud Baseline** `[Done]`
*   **Workflow:** `collector` -> `decryptor` -> `log2timeline/psteal (JSONL)` -> `Timesketch/BigQuery`

#### **Phase 2: Managed Pipeline Optimization** `[Testing]`
*   **Workflow:** `collector` -> `GCS (Encrypted)` -> `Cloud Run Jobs (Decrypt)` -> `GCS (Decrypted)` -> `Cloud Run Jobs (log2timeline/psteal)` -> `BigQuery`

#### **Phase 3: Micro-Parser Distributed Architecture** `[Planning]`
*   **Workflow:** `collector` -> `GCS (Encrypted)` -> `Cloud Run Jobs (Decrypt)` -> `GCS (Decrypted)` -> `Cloud Run Jobs * X (Parallel Artifact Parsers)` -> `BigQuery`

---

### 🚀 Core Technologies

*   **Language:** `Go`
*   **Infrastructure:** Google Cloud (Cloud Run Jobs, GCS, BigQuery)
*   **Forensics:** Plaso (`log2timeline`) and specialized custom parsers.

---

### 💡 Philosophy: "Automation Freak" Approach

We minimize manual labor in Incident Response (IR) to allow analysts to focus on high-level decision-making.
*   **Speed:** Massive parallel parsing using cloud compute resources.
*   **Security:** End-to-end encryption for evidence data with secure, automated key orchestration via Cloud KMS within the Cloud Run pipeline.
*   **Scalability:** A seamless pipeline that handles everything from a single host to large-scale enterprise environments.
