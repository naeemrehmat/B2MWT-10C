# Iterative Definition Refinement for Zero-Shot Classification via LLM-Based Semantic Prototype Optimization

This repository contains the benchmark dataset introduced in the paper:

> **Iterative Definition Refinement for Zero-Shot Classification via LLM-Based Semantic Prototype Optimization**

The dataset is designed for **content-based URL classification** and supports research in:

- Zero-shot website classification
- Semantic prototype optimization
- LLM-based content understanding
- Web content categorization
- Domain classification benchmarks

---

# Dataset Overview

We introduce a new **human-labeled benchmark dataset** for website content classification.

The dataset contains:

- **10 categories**
- **1,000 samples per category**
- **10,000 total samples**
- Each sample assigned **exactly one category**
- Labels verified through **human annotation**

The dataset is split into:

- **Train:** 200 samples per class
- **Dev:** 200 samples per class
- **Test:** 600 samples per class

---

# Dataset Statistics

| Category | Train | Dev | Test |
|---|---:|---:|---:|
| Betting & Gambling | 200 | 200 | 600 |
| Business & Industry | 200 | 200 | 600 |
| Content Retrieval Issues | 200 | 200 | 600 |
| Cultural & Creative Arts | 200 | 200 | 600 |
| Leisure & Entertainment | 200 | 200 | 600 |
| Literature & Books | 200 | 200 | 600 |
| Pornographic Content | 200 | 200 | 600 |
| Retail eCommerce | 200 | 200 | 600 |
| Unused & Placeholder | 200 | 200 | 600 |
| Video & Online Games | 200 | 200 | 600 |

### Total Samples

- **Train:** 2,000
- **Dev:** 2,000
- **Test:** 6,000

---

# Repository Structure

```text
.
├── train.json
├── dev.json
├── test.json
└── README.md
```

---

# Data Format

Each dataset file is a JSON list where every entry corresponds to a single website sample.

## Example

```json
{
  
  "Unique_ID": "S100001",
  "Label": "Cultural_&_Creative_Arts",
  "TEXT": "Website title: Breadwig\nWebsite body text: ..."
}
```

---

# Fields Description

| Field | Description |
|---|---|
| `Unique_ID` | Unique identifier for the sample |
| `Label` | Human-annotated category label |
| `TEXT` | Extracted textual webpage content |

---

# Categories

The dataset includes the following 10 categories:

1. Betting & Gambling
2. Business & Industry
3. Content Retrieval Issues
4. Cultural & Creative Arts
5. Leisure & Entertainment
6. Literature & Books
7. Pornographic Content
8. Retail eCommerce
9. Unused & Placeholder
10. Video & Online Games


---

# Notes

- Each sample contains website textual content extracted from webpages.
- The benchmark focuses on **content-based classification**, rather than URL string classification alone.

---

# Test Set Note

Due to GitHub file size limitations, the original `test.json` file has been split into two parts:

- `test_part1.json`
- `test_part2.json`

Please combine both files to reconstruct the complete test set before evaluation.

Example (Python):

```python
import json

with open("test_part1.json") as f1:
    part1 = json.load(f1)

with open("test_part2.json") as f2:
    part2 = json.load(f2)

test_data = part1 + part2

with open("test.json", "w") as f:
    json.dump(test_data, f, indent=2)

print("Combined test set size:", len(test_data))
```

---


# Citation

If you use this dataset in your research, please cite:

```bibtex
@article{rehmat2026iterative,
  title={Iterative Definition Refinement for Zero-Shot Classification via LLM-Based Semantic Prototype Optimization},
  author={Rehmat, Naeem and Saeed, Muhammad Saad and Ul Haq, Ijaz and Malik, Khalid},
  journal={arXiv preprint arXiv:2604.27335},
  year={2026}
}
```

---

# License

Please specify the dataset license here.

Example:

```text
This dataset is released for research and academic use only.
```


