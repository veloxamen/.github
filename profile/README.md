# ⚡ Veloxamen
**Next-Generation Cloud-Native DFIR Pipeline**

The name **Veloxamen** is a portmanteau of **Velox** (Latin for "swift/fast") and **Examen** (Latin for "examination/investigation"). True to its name, this pipeline aims to automate and accelerate the entire DFIR (Digital Forensics & Incident Response) workflow leveraging cloud-native architectures.

---

### 🗺️ Roadmap
Currently in **Phase 3 (Developing)**. Simple ingestions to BigQuery have been completed (may have some improvements), tackling further evolutional improvements.

#### **Phase 1: Local to Cloud Baseline** `[Done]`
*   **Workflow:** `collector` -> `decryptor` -> `log2timeline/psteal (JSONL)` -> `Timesketch/BigQuery`

#### **Phase 2: Managed Pipeline Optimization** `[Done]`
*   **Workflow:** `collector` -> `GCS (Encrypted)` -> `Cloud Run Jobs (Decrypt)` -> `GCS (Decrypted)` -> `Batch (log2timeline/psteal)` -> `BigQuery (Analysis)`
                                                                                    `GCS (Network)`   -> `Cloud Run Jobs (Parsing)`    -> `BigQuery (Analysis)`

#### **Phase 3: Micro-Parser Distributed Architecture** `[Developing]`
*   **Workflow:** `collector` -> `GCS (Encrypted)` -> `Cloud Run Jobs (Decrypt)` -> `GCS (Decrypted)` -> `Cloud Run Jobs * X (Parallel Artifact Parsers)` -> `BigQuery (Triage)` ->  `Vertex AI (Insight)` -> `Looker (Analysis)`  
    \* Network ingestion will stay almost same but may have some improvements.

---

### 🚀 Core Technologies

*   **Language:** `Go` 
*   **Infrastructure:** Google Cloud (Cloud Run Jobs, Batch, GCS, BigQuery)
*   **Forensics:** Plaso (`log2timeline`) and specialized custom parsers.

---

### 💡 Philosophy: "Automation Freak" Approach

We minimize manual labor in DFIR to allow analysts to focus on high-level decision-making.
*   **Speed:** Massive parallel parsing using cloud compute resources.
*   **Security:** End-to-end encryption for evidence data with secure, automated key orchestration via Cloud KMS within the Cloud Run pipeline.
*   **Scalability:** A seamless pipeline that handles everything from a single host to large-scale enterprise environments.

---

### 📫 Stay Connected

*   **Feedback & Inquiries:** Please open an **Issue** or join our **Discussions** for any questions or collaboration requests regarding `Veloxamen`.
