# 💾 DataSwap – Decentralized AI/Data Marketplace
 *Buy, sell, and compute on datasets — fully decentralized.*

---

## 1. Concept
DataSwap is a **peer-to-peer marketplace** for datasets, aimed at AI researchers, data scientists, and ML teams.  
Users can upload datasets to **Filecoin Warm Storage**, monetize them, or purchase datasets from others, using **Filecoin Pay** for secure payments.  

Key points:  
- On-chain dataset metadata ensures trust and transparency.  
- Fast retrieval through **FilCDN**.  
- Optional “compute-over-data” feature allows buyers to test datasets before purchase.  

---

## 2. Core Features
### ⚡ a) Dataset Upload & Storage
- Users upload datasets (CSV, JSON, images, audio).  
- Stored via **FilecoinWarmStorageService** with **PDP verification**.  
- Metadata stored on-chain: name, description, size, type, sample preview, license.  

### ⚡ b) Marketplace & Discovery
- Browsable dataset catalog by category (NLP, vision, audio, tabular).  
- Search, filter, and preview datasets without full download.  
- Optional tagging system for better discoverability.  

### ⚡ c) Payment & Access
- Buyers pay via **Filecoin Pay**: one-time or subscription access.  
- Streaming payments supported for datasets that update frequently.  
- Revenue automatically settles to dataset owner wallet.  

### ⚡ d) Secure Retrieval & CDN
- Access datasets via **FilCDN** for blazing-fast download.  
- Optional time-limited access: dataset automatically becomes inaccessible after subscription ends.  

### ⚡ e) Compute-over-Data (Optional)
- Buyers can run light preprocessing scripts on datasets **without full download**.  
- Example: run a small model evaluation on images or perform summary stats.  
- Payments handled per compute job or included in subscription.  

### ⚡ f) Synapse SDK Integration
- JavaScript/TypeScript SDK for direct integration with ML workflows.  
- Example: `loadDataset('datasetID')` fetches dataset from Filecoin into Colab or local environment.  

---

## 3. Flow
1. **Dataset Upload**
   - User uploads a small example dataset (~100MB).  
   - Stored in warm storage → PDP verification passes.  
   - Metadata saved on-chain.  

2. **Dataset Discovery**
   - Another user browses marketplace, previews dataset.  
   - Searches by category/tag.  

3. **Purchase / Access**
   - Buyer pays via **Filecoin Pay** (one-time or subscription).  
   - Dataset delivered via **FilCDN**.  

4. **Optional Compute**
   - Buyer runs a test script on dataset before fully committing.  
   - Usage measured and billing handled via Filecoin Pay.  

5. **Revenue Flow**
   - Dataset owner wallet receives FIL instantly.  

---

## 4. Architecture 
- **Frontend DApp**: React + Tailwind (shadcn/ui) for upload, marketplace, and dashboards.  
- **Filecoin Warm Storage**: stores datasets with PDP verification.  
- **FilCDN**: serves datasets fast to buyers.  
- **Filecoin Pay**: handles one-time and streaming payments, escrow, and settlement.  
- **Synapse SDK**: integrates datasets directly into ML workflows.  

**Data Flow:**  
1. Provider uploads dataset → Warm Storage → PDP verification → on-chain metadata.  
2. Buyer discovers dataset → previews metadata.  
3. Buyer pays via Filecoin Pay → access granted via FilCDN.  
4. Optional compute jobs run via Synapse SDK → paid per job.  
5. Provider receives revenue instantly.  

---


## 5. Why
- DataSwap unlocks **trusted, decentralized datasets** for AI & ML teams.  
- Eliminates central data brokers → creators monetize directly.  
- Combines **storage, payment, and CDN** into a **single composable dApp**.  
- Judges see immediate utility: “AI teams can pay and use datasets securely and instantly.”  

---

## 6. Extensions / Future Roadmap
- Ratings & reviews for datasets.  
- Dataset versioning & auto-updates with streaming payments.  
- Integration with AI model marketplaces.  
- Governance DAO for curation and dataset verification.  

---
