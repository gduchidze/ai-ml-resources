# The 18-Month AI Engineering Execution Sheet

**Objective:** Reach Google/DeepMind/OpenAI competency level.  
**Schedule:** 15–18 hours/week (1.5 hrs/weekday, 4+4 hrs/weekend).

### Constraint Checklist
- [x] **Foundations First:** Derivatives → NNs → Transformers → Distributed Systems.
- [x] **Theory & Practice:** Every theoretical concept is paired with a "build from scratch" task.
- [x] **Systems Focus:** Heavy emphasis on efficient and distributed training (MIT 6.824/6.5940).

---

## 📅 The Daily Routine Protocol
*Apply this template to the specific content listed in the Weekly Syllabus below.*

* **Monday (Theory - 1.5h):** Watch the primary lecture (2x speed if needed). Take notes on the math, not just the high-level ideas.
* **Tuesday (Math/Reading - 1.5h):** Read the associated paper or textbook chapter. Derive the key equations (e.g., Backprop gradients, Self-Attention) by hand on paper.
* **Wednesday (Coding Setup - 1.5h):** Specific coding sub-task (e.g., implement the class structure, data loader, or forward pass).
* **Thursday (Coding Core - 1.5h):** Implement the core algorithm (e.g., backward pass, attention mechanism, Raft log replication).
* **Friday (Debug/Refine - 1.5h):** Debug using small unit tests. Compare your outputs against a reference implementation (e.g., PyTorch `nn.Linear`).
* **Saturday (Deep Work - 4h):** The "Project" day. Assemble the pieces into a working system. Train on real data.
* **Sunday (DSA & Review - 4h):** 2 hours of LeetCode/Deep-ML + 2 hours of planning next week.

---

## Phase I: The Neural Substrate (Weeks 1–12)
**Goal:** Master the "Software 2.0" stack—from manual derivatives to ConvNets.  
**Key Resources:** Karpathy (Zero to Hero), MIT 6.S191, Deep Learning (Goodfellow).



| Week | Phase | Topic | Theory Resource (Mon/Tue) | Coding Task (Wed-Sat) | DSA/ML Practice (Sun) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | Foundations | Autograd Engines | Karpathy: Micrograd Lecture. Goodfellow Ch 6.5. | **Project:** Build Micrograd from scratch. Implement `Value` node and DAG visualization. | Arrays & Hashing (Two Sum, Contains Duplicate) |
| **2** | Foundations | Backpropagation | Karpathy: Micrograd (cont). Calculus Review. | **Project:** Implement `backward()` for Add, Mul, Pow, Tanh. Train a demo classifier. | Sliding Window (Best Time to Buy Stock) |
| **3** | Foundations | Language Modeling I | Karpathy: Makemore (Bigram). Intro to Logits/CrossEntropy. | **Project:** Build Makemore Bigram model. Implement counting vs. gradient-based training. | Two Pointers (Valid Palindrome) |
| **4** | Foundations | MLPs & Embeddings | Karpathy: Makemore (MLP). Bengio 2003 Paper. | **Project:** Implement MLP with context window. Visualize embedding lookup tables. | Stack (Valid Parentheses) |
| **5** | Foundations | Training Dynamics | Karpathy: Makemore (BatchNorm). Goodfellow Ch 8. | **Project:** Implement BatchNorm1d manually. Diagnose "dead neurons" using histograms. | Binary Search (Search in Rotated Array) |
| **6** | Foundations | Manual Backprop | Karpathy: Building Makemore Part 4. | **Project:** *The Crucible:* Write the backward pass for Linear/BatchNorm/Tanh layers without autograd. | Linked List (Reverse Linked List) |
| **7** | Vision | ConvNets (CNNs) | MIT 6.S191: CNNs. Karpathy: WaveNet. | **Project:** Implement `Conv2d` using im2col (matrix multiplication). Train on MNIST. | Trees (Invert Binary Tree) |
| **8** | Vision | Modern CNNs | Reading: ResNet Paper (He et al.). | **Project:** Build ResNet-18 from scratch. Implement Skip Connections. Train on CIFAR-10. | Trees (Max Depth, Diameter) |
| **9** | Sequence | RNNs & LSTMs | MIT 6.S191: RNNs. Goodfellow Ch 10. | **Project:** Implement a raw RNN cell. Train character-level text generation. | Heap (Kth Largest Element) |
| **10** | Optimization | Optimizers | Reading: Adam Paper (Kingma & Ba). | **Project:** Implement SGD, RMSProp, and Adam from scratch. Compare convergence. | Backtracking (Combination Sum) |
| **11** | Practice | Initialization | Reading: Kaiming Init & Xavier Init papers. | **Lab:** Experiments on weight initialization. Visualize how bad init kills gradient flow. | Graphs (Number of Islands) |
| **12** | **Capstone I** | **Nano-PyTorch** | Review Week. | **Capstone:** Refactor your Micrograd + Layers into a clean library `NanoTorch`. | Graphs (Clone Graph) |

---

## Phase II: The LLM Architect (Weeks 13–28)
**Goal:** Build, train, and align a GPT-class model. Understand data pipelines.  
**Key Resources:** Stanford CS336, Stanford CME 295, Karpathy (GPT).



| Week | Phase | Topic | Theory Resource (Mon/Tue) | Coding Task (Wed-Sat) | DSA/ML Practice (Sun) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **13** | Architecture | Self-Attention | Karpathy: Let's Build GPT. *Attention Is All You Need*. | **Project:** Implement Scaled Dot-Product Attention & Multi-Head Attention classes. | Deep-ML: Matrix Multiplication |
| **14** | Architecture | The Transformer | CS336: Architectures. Pre-Norm vs Post-Norm. | **Project:** Build the full GPT class. Verify parameter counts against GPT-2 paper. | Deep-ML: Softmax implementation |
| **15** | Architecture | Positional Encodings | CME 295: RoPE. Reading: RoFormer paper. | **Project:** Implement Rotary Positional Embeddings (RoPE) using complex numbers. | 1D DP (Climbing Stairs) |
| **16** | Training | Pre-training Loop | CS336: Training. Gradient Clipping, Scheduler. | **Project:** Train your GPT on "TinyShakespeare". Implement text generation sampling. | Intervals (Merge Intervals) |
| **17** | Data | Tokenization | Karpathy: Tokenizer. Reading: BPE algorithm. | **Project:** Build a BPE tokenizer from scratch. Handle UTF-8 byte streams. | Tries (Implement Trie) |
| **18** | Optimization | KV Cache & GQA | CME 295: GQA. Reading: Llama 2 paper. | **Project:** Add Grouped Query Attention (GQA) and KV Caching to your model. Benchmark speedup. | Greedy (Max Subarray) |
| **19** | Scale | Scaling Laws | CS336: Scaling Laws. DeepMind Chinchilla paper. | **Lab:** Train 3 mini-models (1M, 5M, 10M). Fit a power law curve to predict loss. | Math (Rotate Image) |
| **20** | Data Eng | The Pipeline | CS336: Data. Common Crawl / WARC format. | **Project:** Write a parser for WARC files. Filter text by perplexity score. | Bit Manipulation |
| **21** | Data Eng | Deduplication | Reading: MinHash LSH for deduplication. | **Project:** Implement MinHash LSH to find near-duplicate documents in a dataset. | Hashing (Design Twitter) |
| **22** | Systems | Mixed Precision | CME 295: Hardware. FP16 vs BF16. | **Lab:** Implement Automatic Mixed Precision (AMP) training step with gradient scaling. | Review: Arrays |
| **23** | Alignment | SFT (Instruction) | CS336: Instruction Tuning. Chat Templates. | **Project:** Finetune your GPT (or a small Llama) on Alpaca dataset. Implement chat format. | Review: Linked Lists |
| **24** | Alignment | LoRA | Reading: LoRA paper. | **Project:** Implement Low-Rank Adaptation layers from scratch. Inject into Linear layers. | Deep-ML: PCA Implementation |
| **25** | Alignment | RLHF Theory | CS336: RLHF. Reward Modeling. | **Study:** Derive the PPO objective function. Understand KL-divergence penalty. | Review: Trees |
| **26** | Alignment | DPO | Reading: Direct Preference Optimization paper. | **Project:** Implement DPO Loss. Fine-tune on a preference dataset (Helpful vs Harmless). | Review: Graphs |
| **27** | Evaluation | LLM-as-a-Judge | CME 295: Evaluation. MMLU, GSM8K. | **Project:** Build an eval pipeline. Use GPT-4 to grade your model's outputs. | System Design: Web Crawler |
| **28** | **Capstone II** | **Vertical LLM** | Idea: Legal/Medical summarizer. | **Capstone:** Curate a domain dataset → Tokenize → Pretrain (small) → SFT → Eval. | System Design: Rate Limiter |

---

## Phase III: The Systems Engineer (Weeks 29–48)
**Goal:** Master distributed systems. This is the differentiator for Top-Tier Labs.  
**Key Resources:** MIT 6.824 (Distributed Systems), Designing Data-Intensive Applications (DDIA).



| Week | Phase | Topic | Theory Resource (Mon/Tue) | Coding Task (Wed-Sat) | Readings (DDIA) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **29** | Dist. Sys | MapReduce | MIT 6.824: Lecture 1. Google MR Paper. | **Lab:** MIT 6.824 Lab 1 (MapReduce). Master/Worker architecture. | Ch 1: Reliability/Scalability |
| **30** | Dist. Sys | Fault Tolerance | MIT 6.824: Lecture 2. | **Lab:** Handle worker crashes/timeouts in MapReduce. | Ch 5: Replication |
| **31** | Dist. Sys | Raft: Election | MIT 6.824: Raft. Visualization. | **Lab:** MIT 6.824 Lab 2A (Raft Leader Election). State machines. | Ch 9: Consistency |
| **32** | Dist. Sys | Raft: Logs | MIT 6.824: Log Replication. | **Lab:** MIT 6.824 Lab 2B (Log Replication). Handle consistency check. | Ch 9: Consensus |
| **33** | Dist. Sys | Raft: Persistence | MIT 6.824: Persistence. | **Lab:** MIT 6.824 Lab 2C (Persist state to disk). | Ch 7: Transactions |
| **34** | Storage | LSM Trees | DDIA: Storage Engines. | **Project:** Implement a simple LSM-tree (MemTable + SSTable) in Python. | Ch 3: Storage Engines |
| **35** | Dist. ML | DDP | PyTorch DDP Paper. | **Project:** Write a DDP training loop using `torch.distributed`. Sync gradients manually. | Ch 6: Partitioning |
| **36** | Dist. ML | Ring All-Reduce | Theory: Ring All-Reduce algorithm. | **Lab:** Implement Ring All-Reduce using send/recv primitives. | -- |
| **37** | Dist. ML | FSDP (ZeRO) | Reading: ZeRO Paper (Microsoft). | **Project:** Fine-tune a 7B model using FSDP on cloud GPUs (Lambda/RunPod). | -- |
| **38** | Dist. ML | Pipeline Parallel | Reading: GPipe / PipeDream. | **Study:** Diagram pipeline bubbles. Calculate efficiency of 1F1B schedule. | -- |
| **39** | Dist. ML | Tensor Parallel | Reading: Megatron-LM. | **Study:** Deep-ML "Distributed MatMul". Understand column/row splitting. | -- |
| **40** | DBs | Vector Search | CME 295: RAG. HNSW Algorithm. | **Project:** Build a Vector DB from scratch (Flat index + Quantization). | -- |
| **41** | Systems | Kafka/Streaming | DDIA: Stream Processing. | **Project:** Build a data ingestion pipeline using Kafka (or Redpanda). | Ch 11: Streaming |
| **42** | Systems | System Design I | System Design Primer. | **Design:** "Design a Distributed Job Scheduler" (like Celery/Kubernetes). | Ch 10: Batch Processing |
| **43** | Systems | System Design II | Designing ML Systems (Chip Huyen). | **Design:** "Design a Feature Store". | Huyen Ch 1-2 |
| **44** | **Capstone III** | **Mini-Param Server** | Goal: Async training. | **Capstone:** Build a Parameter Server where workers push gradients & pull weights. | -- |
| **45** | Review | Systems Review | Re-read Raft/Paxos papers. | **Task:** Explain Raft consensus out loud. Draw failure modes. | LeetCode: Advanced Graphs |
| **46** | Review | Concurrency | Go Concurrency / Python Asyncio. | **Task:** Solve "Dining Philosophers" or concurrent LRU Cache. | LeetCode: Concurrency |
| **47** | Prep | Mock Interview | Pramp / Peer. | **Mock:** System Design (e.g., "Design Twitter Timeline"). | -- |
| **48** | Prep | Mock Interview | Pramp / Peer. | **Mock:** ML System Design (e.g., "Design a YouTube Recommendation System"). | -- |

---

## Phase IV: Efficiency & Production (Weeks 49–64)
**Goal:** Optimization (CUDA) and MLOps.  
**Key Resources:** MIT 6.5940 (Efficient ML), Designing ML Systems, Triton Tutorials.



| Week | Phase | Topic | Theory Resource (Mon/Tue) | Coding Task (Wed-Sat) | Readings |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **49** | Hardware | GPU Architecture | MIT 6.5940: GPU Arch. HBM vs SRAM. | **Study:** Analyze NVIDIA A100/H100 specs. Memory Bandwidth calculations. | Huyen Ch 3 |
| **50** | Efficiency | Quantization | MIT 6.5940: Quantization. INT8/FP4. | **Project:** Implement a quantization function (absmax) for a Linear layer. | Huyen Ch 4 |
| **51** | Efficiency | Pruning | MIT 6.5940: Pruning. | **Project:** Implement Magnitude Pruning. Fine-tune to recover accuracy. | Huyen Ch 5 |
| **52** | Kernels | Triton Intro | OpenAI Triton Documentation. | **Project:** Solve Triton Puzzles 1-3 (Vector Add, MatMul). | -- |
| **53** | Kernels | Fused Kernels | Theory: Kernel Fusion benefits. | **Project:** Implement Fused Softmax in Triton. Benchmark vs PyTorch. | -- |
| **54** | Kernels | FlashAttention | Reading: FlashAttention (Dao). | **Project:** Implement simplified FlashAttention (tiling) in Triton. | -- |
| **55** | Inference | PagedAttention | Reading: vLLM Paper. | **Project:** Implement a Logical KV Cache Block manager (OS-style paging). | -- |
| **56** | Inference | Speculative Decoding | Reading: Speculative Decoding. | **Project:** Implement draft/verify loop with a small and large model. | -- |
| **57** | MLOps | Serving Architecture | Huyen: Deployment Patterns. | **Project:** Build a serving container (Docker) with FastAPI and Batching. | Huyen Ch 7 |
| **58** | MLOps | Monitoring | Huyen: Monitoring. Drift. | **Project:** Implement a drift detection system (KS-test) on input data. | Huyen Ch 8 |
| **59** | MLOps | CI/CD for ML | GitHub Actions / CML. | **Project:** Build a CI pipeline that trains a model and pushes to HuggingFace. | Huyen Ch 9 |
| **60** | RAG | Advanced RAG | CME 295: Agents. | **Project:** Build a RAG system with Hybrid Search (Keyword + Vector). | -- |
| **61** | Agents | Tool Use | Reading: ReAct / Toolformer. | **Project:** Build an agent that can call a Python Calculator and Weather API. | -- |
| **62** | **Capstone IV** | **Inference Engine** | Goal: Speed. | **Capstone:** Build a high-throughput LLM server with Continuous Batching. | -- |
| **63** | Prep | Coding Prep | Deep-ML Hard Problems. | **Task:** Implement K-Means, DBSCAN, Decision Tree from scratch. | LeetCode: Hard |
| **64** | Prep | System Design | Design: "Design ChatGPT". | **Task:** Capacity planning for serving 100M daily users. | -- |

---

## Phase V: The Final Sprint (Weeks 65–72)
**Goal:** Interview Readiness and Portfolio Polish.

| Week | Focus | Daily Task (Mon-Fri) | Weekend Task (Sat-Sun) |
| :--- | :--- | :--- | :--- |
| **65** | Resume & Portfolio | Polish GitHub readme's for Micrograd, GPT, Raft, Inference Engine. | **Mock:** Behavioral Interview (STAR method). |
| **66** | Review: Theory | Review: Transformers (MHA/GQA/RoPE), BN/LN, Optimizers. | **Mock:** ML Theory (Explain nuances of Adam vs SGD). |
| **67** | Review: Systems | Review: Raft, MapReduce, DDP, HBM/SRAM. | **Mock:** Distributed Systems Design. |
| **68** | Coding Grind I | Deep-ML: Tensor manipulation, Broadcast semantics. | LeetCode: Graphs/DP speed runs. |
| **69** | Coding Grind II | Deep-ML: Implement Backprop for `Conv2d`. | LeetCode: Trees/Heaps speed runs. |
| **70** | Mock Gauntlet | Full mock loops (Coding + Sys Design + Behavioral). | Refine "Tell me about a project" stories. |
| **71** | Applications | Apply to Google, OpenAI, Anthropic, Meta, Startups. | Research company-specific blogs/papers. |
| **72** | **The End** | Relaxation & Confidence. Light review. | **GO LIVE.** |
