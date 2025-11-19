<div align="center">

# **Azure Data Factory – ETL & Data Orchestration**
Efficient • Scalable • Automated Data Workflows  

---

### **Badges**
![Azure](https://img.shields.io/badge/Azure-Data%20Factory-0072C6?logo=microsoft-azure)
![ETL](https://img.shields.io/badge/ETL-Pipelines-blue)
![DevOps](https://img.shields.io/badge/CI%2FCD-Enabled-green)
![JSON](https://img.shields.io/badge/Config-JSON-orange)
![Status](https://img.shields.io/badge/Maintained-No-success)

</div>

---

## **📌 Overview**
This repository contains the complete infrastructure and configuration setup for orchestrating and managing data workflows using **Azure Data Factory (ADF)**.  
It includes pipelines, datasets, dataflows, linked services, triggers, and publishing configurations that together enable a reliable **ETL (Extract, Transform, Load)** process.

These workflows support:
- automated data ingestion  
- transformation & mapping  
- scheduled and event-based triggers  
- integration across multiple data sources and destinations

---

## **📁 Project Structure**

```
├── dataflow/
│   └── Transformation logic (mapping, filtering, aggregations)
│
├── dataset/
│   └── Definitions for source & sink data structures
│
├── factory/
│   └── Factory-level metadata, global parameters, integration settings
│
├── linkedService/
│   └── Connection configs (Azure SQL, Blob Storage, ADLS, REST APIs)
│
├── pipeline/
│   └── ETL workflows coordinating datasets, linked services & dataflows
│
├── trigger/
│   └── Schedule/event triggers for automating pipeline execution
│
└── publish_config.json
    └── Deployment settings for publishing to ADF environments
```

---

## **🧠 Architecture Overview**

### **High-Level ETL Flow**

```
        +-------------------------+
        | External Data Sources   |
        | (SQL, Blob, ADLS, API) |
        +------------+------------+
                     |
                     v
        +--------------------------+
        |   Linked Services        |
        | (Secure Connections)     |
        +--------------------------+
                     |
                     v
        +--------------------------+
        |        Datasets          |
        | (Source/Sink Definitions)|
        +------------+-------------+
                     |
                     v
        +--------------------------+
        |        Pipelines         |
        |   (ETL Orchestration)    |
        +------------+-------------+
                     |
                     v
        +--------------------------+
        |        Dataflows         |
        | (Mapping & Transform)    |
        +------------+-------------+
                     |
                     v
        +--------------------------+
        |  Destination Storage     |
        | (SQL, ADLS, Blob, etc.) |
        +--------------------------+
```

---

## **⚙️ Tech Stack**

| Component | Technology |
|----------|------------|
| Orchestration | Azure Data Factory |
| Storage | Azure SQL • ADLS • Blob Storage |
| Pipeline Activities | Copy, Mapping Dataflow, Lookup, ForEach, Web |
| Authentication | Managed Identity / Key Vault |
| Deployment | ADF Publish + CI/CD support |
| Format | JSON-based factory assets |

---

## **🚀 How to Deploy**

### **1️⃣ Prerequisites**
- Azure subscription  
- Azure Data Factory instance  
- Required resource access (SQL, ADLS, Blob, Key Vault)
- GitHub or Azure DevOps (optional for CI/CD)

---

### **2️⃣ Configure ADF Git Integration**
In Azure Portal:  
**ADF → Manage → Git Configuration → GitHub/Azure DevOps**

---

### **3️⃣ Clone the Repository**
```bash
git clone <your-adf-repo-url>
cd <your-repo>
```

---

### **4️⃣ Deploy Using ADF UI**
1. Open ADF Studio  
2. Go to **Manage → ARM Template → Import**  
3. Select assets:
   - factory/
   - linkedService/
   - pipeline/
   - dataset/
   - dataflow/
4. Click **Publish**

---

### **5️⃣ Deploy via CI/CD (Optional)**
Use GitHub Actions or Azure DevOps pipelines with `publish_config.json`.

---

## **▶️ How to Run the Pipelines**

1. Open Azure Data Factory Studio  
2. Navigate to **Author**  
3. Open a pipeline  
4. Click **Debug** (test run)  
5. Click **Trigger Now** (manual run)  
6. View logs under **Monitor → Pipeline Runs**

---

## **🧪 Monitoring & Logging**

Use built-in ADF monitoring for:
- pipeline runs  
- activity logs  
- error traces  
- performance metrics  

Optional integrations:
- Azure Monitor  
- Log Analytics  
- Alerts

---

## **✨ Future Enhancements**
- Power BI dashboards for ETL monitoring  
- Event-based triggers (Event Grid)  
- Automated pipeline testing  
- YAML templates for CI/CD deployments  

---

## **🤝 Contributing**
Contributions are welcome!  
Feel free to submit a PR or open an issue.

---

## **📬 Contact**
**Isha Jha**  
Product Manager • Data & Cloud Engineering Background  
📧 jhaisha995@gmail.com  
🔗 https://www.linkedin.com/in/isha-jha-85398892

