# The Arc of Conflict

**Analysis of Media Discourse on the Main Actors of the Syrian Conflict (2010–2026)**

Seminararbeit — Methods and Applications in Digital Humanities  
Universität Leipzig, Fakultät für Mathematik und Informatik  
Author: Orwa Romeeah  
Supervisor: Dr. Ing. Andreas Niekler  
Date: April 5, 2026

---

## Research Question

How does media framing of key Syrian conflict actors evolve across distinct conflict phases, and how do these framings differ between Western and Middle Eastern English-language media?

## Actors Studied

- Syrian Regime (Assad)
- Syrian Opposition
- HTS (Hay'at Tahrir al-Sham / formerly Jabhat al-Nusra)
- ISIS
- Russia
- Iran
- Turkey

## Sources

- **The Guardian** (~8,500 articles) — collected via the Guardian Open Platform API
- **Al Jazeera English** (~4,200 articles) — collected via sitemap scraping

## Diachronic Phases

| Phase | Period | Description |
|-------|--------|-------------|
| P1 | 2010–2011 | Pre-war baseline |
| P2 | 2012–2015 | Uprising and escalation |
| P3 | 2016–2019 | International intervention |
| P4 | 2022–2025 | Regime collapse and transition |

## Methods

- **Co-occurrence analysis** using log-likelihood ratio (G²) at the sentence level
- **Dictionary-based sentiment analysis** using the Hu & Liu Opinion Lexicon with a targeted ±5 word window around actor mentions
- **Cross-source comparison** between The Guardian and Al Jazeera English

## Repository Structure

```
├── README.md
├── arc_of_conflict_Process.ipynb    # Guardian: data collection, preprocessing,
│                                          # co-occurrence, sentiment, and cross-source comparison
├── Arcofconfliket-aljazera.ipynb          # Al Jazeera: data collection, article extraction,
│                                          # date parsing, and CSV export
├── data/                                  # Corpus CSV files (Guardian and Al Jazeera)
├── outputs/                               # Generated plots and co-occurrence networks
```

## How to Run

1. Open the notebooks in [Google Colab](https://colab.research.google.com/)
2. Upload the CSV data files from the `data/` folder or mount Google Drive
3. Run cells sequentially — each notebook is self-contained with all preprocessing, analysis, and visualisation steps

## Dependencies

- Python 3
- pandas, numpy
- scikit-learn (CountVectorizer)
- matplotlib, networkx
- BeautifulSoup (for Al Jazeera scraping)
- NLTK / custom stopword lists

