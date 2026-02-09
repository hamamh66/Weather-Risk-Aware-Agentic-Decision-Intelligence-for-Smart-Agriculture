
# Weather-Risk-Aware Agentic Decision Intelligence for Smart Agriculture

This repository provides an end-to-end reproducible framework for **context-aware agricultural decision intelligence** using dual-stream Vision Transformers, dynamic risk modeling, and agentic IoT policies.

The system integrates **pest recognition**, **crop identification**, **weather context**, and **decision-quality evaluation** to enable sustainable and intelligent agricultural intervention strategies.

---

## Core Contributions

- Dual-stream visual intelligence:
  - **BEiT** → Pest classification  
  - **MiT-B0** → Crop classification
- Dynamic risk scoring conditioned on:
  - Weather variables
  - Growth stages
  - Seasonal context
- Agentic decision policies:
  - Static baseline
  - Weather-adaptive policy
- Decision-level evaluation:
  - Accuracy, Precision, Recall, F1
  - Confusion matrices
  - Spray rate analysis
  - Unnecessary intervention reduction
- Fully reproducible pipeline with all outputs saved to **Google Drive**

---

## Pipeline Overview

Images → Dual Vision Transformers → Joint Scenario Builder  
→ Weather Context Simulation / API  
→ Dynamic Risk Scoring  
→ Policy Decision Layer  
→ Decision-Quality Metrics & Ablations

---

## Repository Structure

```
├── notebooks/
│   ├── Weather_Risk_Aware_Agentic_Decision.ipynb
│   └── Weather_Risk_Aware_Agentic_Decision_PAPERREADY.ipynb
│
├── figures/          # Auto-generated plots
├── tables/           # CSV metrics and summaries
├── logs/             # JSON exports and configs
├── models/           # BEiT and MiT checkpoints
├── datasets/         # User-provided datasets
└── README.md
```

---

## Requirements

- Python 3.10+
- PyTorch
- transformers
- timm
- scikit-learn
- pandas
- matplotlib
- lime

Install dependencies:

```bash
pip install transformers timm accelerate datasets evaluate scikit-learn lime pandas matplotlib
```

---

## Dataset Structure

Expected directory layout:

```
MyDrive/Datasets/
 ├── pest/
 │    ├── train/<class_name>/*.jpg
 │    └── test/<class_name>/*.jpg
 └── crop/
      ├── train/<class_name>/*.jpg
      └── test/<class_name>/*.jpg
```

---

## Running the Notebook

1. Open the notebook in **Google Colab**
2. Mount Google Drive
3. Set dataset paths
4. Run all cells sequentially

All outputs are automatically saved to:

```
/MyDrive/SmartAgri_Direction1/runs/<RUN_ID>/
```

---

## Generated Outputs

### Figures
- Policy comparison curves
- Risk distribution histograms
- Spray rate vs weather
- Unnecessary sprays vs weather
- Decision boundary visualization
- Confusion matrices

### Tables (CSV)
- Decision quality summary
- Confusion matrices
- Policy metrics
- Spray rate by weather bin
- Top predicted pests
- Top predicted crops

---

## Evaluation Metrics

- Decision Accuracy
- Precision / Recall / F1
- Spray Rate
- False Positive Reduction
- Weather-Penalty Ablations

---

## Reproducibility

- Fixed random seeds
- Deterministic sampling
- Logged configurations
- Automatic CSV/JSON exports
- Google Drive integration

---

## Use Cases

- Smart irrigation systems
- Precision agriculture
- Autonomous pest management
- Sustainable resource optimization
- Decision-support dashboards

---

## Future Extensions

- Real weather API integration
- Edge device deployment
- Multimodal sensor fusion
- Explainable AI dashboards
- Reinforcement learning policy optimization

---

## License

For academic and research use.  
Commercial use requires permission.

---

## Citation

If you use this work, please cite the associated publication once available.

---

## Authors

Research Team — Intelligent Agriculture & Agentic AI Systems
