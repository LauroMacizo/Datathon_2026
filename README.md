# Hey Banco · Datathon 2026
## Havi 2.0 — Motor de Inteligencia Proactiva

De reactivo a proactivo: clustering no supervisado + NLP + Claude IA sobre 4 datasets de usuarios reales.

# ¿Qué es Havi 2.0?
Havi es el asistente virtual de Hey Banco. Hoy responde cuando el usuario pregunta. Havi 2.0 actúa antes de que lo haga.

## Construimos un motor de inteligencia que:

* Segmenta a los 24,000 usuarios en 4 perfiles de comportamiento usando K-Means
* Analiza el historial de conversaciones con BERT en español (pysentimiento)
* Calcula un score de propensión por acción para cada usuario en tiempo real
* Conecta Claude (Anthropic) como cerebro conversacional con gestión emocional en vivo
  
## Estructura del repositorio
```
havi-2.0/
├── DATASETS/
│   ├── hey_clientes.csv
│   ├── hey_productos.csv
│   ├── hey_transacciones.csv
│   └── hey_conversaciones.parquet
│
├── Havi_2_Pipeline.ipynb        ← Notebook principal (VS Code / Jupyter)
├── havi_mockup_hey.html         ← Demo interactivo funcional
├── havi_output.json             ← Generado por el notebook (no subir con key)
│
├── hey_banco_logo.png           ← Logo del banco 
├── hey_banco_web_logo.png       ← Ícono 
│
└── README.md
```


---

## 🔄 Pipeline (resumen)

### Incluye:
- Feature engineering avanzado
- NLP con `pysentimiento`
- Clustering con `scikit-learn`
- PCA para visualización
- Sistema de decisiones por cluster

---

## ⚡ Instalación

```bash
git clone https://github.com/LauroMacizo/Datathon_2026.git
cd Datathon_2026

python -m venv .venv
.venv\Scripts\activate   # Windows

pip install pandas numpy scikit-learn pyarrow matplotlib pysentimiento
```

# EJECUTAR DEMO
```
python -m http.server 8000
```

# Stack
* Python (pandas, sklearn, pyarrow, matplotlib)
* Claude (Anthropic)
* HTML + CSS + JS 
* Chart.js