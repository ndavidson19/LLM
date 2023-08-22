# LLM Documentation

---

### Contents:
1. [Guardrails](#guardrails)
2. [PDF Docs of Release](#pdf-docs-of-release)
3. [Open Source Model / Finetuning](#open-source-model--finetuning)
4. [Vector DB for Semantic Search](#vector-db-for-semantic-search)
5. [Deployment](#deployment)
6. [Resources](#resources)

---

### 1. Guardrails <a name="guardrails"></a>
- Needs to have guardrails.
- Ensure that LLM does not stray from target domain.

### 2. PDF Docs of Release <a name="pdf-docs-of-release"></a>
- Documentation provided in PDF format.
- Documentation can also be provided in pure text or .adoc format.
- Idea of garbage in garbage out -> data must be transformed into a Q/A format (only if training / finetuning)
- If using semantic search, phrases can be queried from the DB

### 3. Open Source Model / Finetuning <a name="open-source-model--finetuning"></a>
- Use Open Source Model. (Ideally Llama-7B-Chat-Q4
- Finetune the model using LoRa to match Cisco Docs and Vocabulary.
- LangChain can be used to bridge the workflow

### 4. Vector DB for Semantic Search <a name="vector-db-for-semantic-search"></a>
- Incorporate Vector DB.
- Allows for no retraining necessary between releases.
- Makes documents queriable using cosine similiarity between embeddings.
- Open source embedding algorithms available, no need to use OpenAI

### 5. Deployment <a name="deployment"></a>
- Utilize Docker containers for the inference build.
- Deployment will be made to Kubernetes clusters.

### 6. Resources <a name="resources"></a>
- https://github.com/antimetal/awsdocsgpt
- https://github.com/ShreyaR/guardrails
- https://github.com/facebookresearch/llama-recipes#multiple-gpus-one-node
- https://arxiv.org/abs/2305.07759
- https://github.com/karpathy/llama2.c
- https://github.com/neuml/txtai
