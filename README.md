# CoreVision: Autonomous Driving Perception Pipeline

**CoreVision** è un framework di percezione 3D sviluppato per l'elaborazione di dati sensoristici ad alta fedeltà provenienti da sistemi LiDAR. Il progetto si focalizza sulla trasformazione di Point Clouds grezze (Dataset KITTI) in informazioni semantiche strutturate, fondamentali per la navigazione sicura di veicoli autonomi.

## 🛠️ Architettura della Pipeline

Il sistema implementa un flusso di elaborazione sequenziale per estrarre oggetti rilevanti dal rumore ambientale:

1.  **Voxel Grid Filtering:** Riduzione della densità della nuvola di punti per ottimizzare le prestazioni computazionali senza compromettere la struttura geometrica della scena.
2.  **ROI (Region of Interest) Clipping:** Ritaglio dello spazio 3D per focalizzare l'analisi esclusivamente sulla carreggiata e sulle aree limitrofe, eliminando punti distanti o irrilevanti.
3.  **Ground Segmentation:** Separazione matematica del piano stradale dagli ostacoli (veicoli, pedoni, infrastrutture) utilizzando algoritmi di segmentazione planare.
4.  **DBSCAN Clustering:** Raggruppamento dei punti rimanenti in cluster indipendenti per l'identificazione e la classificazione degli oggetti dinamici.

## 💻 Tech Stack
* **Linguaggio:** Python 3.x
* **Librerie Core:** 
    * `Open3D`: Elaborazione e visualizzazione di nuvole di punti 3D.
    * `NumPy`: Calcolo vettoriale e matriciale per trasformazioni spaziali.
    * `Matplotlib`: Analisi statistica e visualizzazione dei dati.

## 🎓 Obiettivi Ingegneristici & Accademici
Sviluppato come parte di un percorso di approfondimento in **Ingegneria**, il progetto dimostra competenze in:
*   **Identificazione ed Ottimizzazione:** Calibrazione di iperparametri per il clustering spaziale.
*   **Sistemi Integrati:** Gestione di pipeline di dati complessi in ambienti simulati.
*   **Meccanica Applicata:** Gestione di sistemi di riferimento e trasformazioni di coordinate.

---
*Progetto sviluppato da [Il Tuo Nome/LolloRega]*
