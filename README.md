# Age Estimation Face Dataset: Minors & Young Adults (10-30 Years)

Age estimation face dataset: 10,000+ consented selfies of minors & young adults (10-30 years) with verified per-year age labels. Multi-ethnic, phone-captured. Built for under-18 age gating, age verification, and face recognition.

## Dataset Overview

| | |
|---|---|
| **Total images** | 10,000+ |
| **Age range** | 10-30 (per-year folders) |
| **Ethnicities** | Black, Caucasian, Hispanic |
| **Gender** | Male, Female |
| **Capture device** | Smartphone front camera |
| **Labels** | age, gender, ethnicity |
| **Format** | JPEG images + CSV metadata |
| **Consent** | Full legal consent |

![](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F20109613%2Fa45b6901e1407d1dbed91dfac92e838f%2Fdataset_preview_age.png?generation=1775577020990409&alt=media)

## Metadata Format

| Column | Description | Example |
|---|---|---|
| `file_name` | Image filename | age_14_0023.jpeg |
| `age_folder` | Age folder | age_14 |
| `age` | Verified age at capture | 14 |
| `gender` | Gender | female |
| `ethnicity` | Ethnicity | black |

## Use Cases

### Age Gating & Legal Compliance

```
Input: User selfie at app sign-up
Model: Age estimation (trained on this dataset)
Output: under_18 / over_18
Action: Block or allow access
```

Train binary classifiers or regression models that accurately detect whether a user is under 18. Dense per-year sampling around the 18-year boundary reduces false positives and false negatives where it matters most.

### Age Estimation

Fine-tune pretrained models (DEX, MiVOLO, AgeNet) on the 10-30 segment to reduce MAE in the range where public datasets underperform. Verified birth-year labels provide clean ground truth.

### Age Verification Without ID

Build selfie-only age checks for platforms that need frictionless onboarding. No document upload required — the model estimates age directly from a phone-captured photo.

### Bias Evaluation

Test your existing age estimation model across ethnicities and genders using the structured metadata. Identify and fix demographic accuracy gaps before production deployment.

## Comparison With Public Datasets

| Feature | This Dataset | UTKFace | IMDB-WIKI | MORPH | FG-NET |
|---|---|---|---|---|---|
| Age range | **10-30** | 0-116 | 0-100 | 16-77 | 0-69 |
| Focus on teens | **Dense** | Sparse | Sparse | None | Sparse |
| Label quality | **Birth-year verified** | Filename-parsed | Noisy/scraped | Verified | Verified |
| Ethnic diversity | **3 groups, balanced** | 5 groups | Skewed | 80% one group | Limited |
| Consent | **Full + guardian** | None | None | Research only | Research only |
| Commercial license | **Yes** | No | No | No | No |
| Selfie-specific | **Yes** | Mixed | Web photos | Mugshot-style | Mixed |

## Getting the Full Dataset

This repository contains a descriprion only. For the samplee and full 10,000+ image dataset with commercial license:

1. **Browse samples** on [Kaggle](https://kaggle.com/datasets/axondata/age-estimation-minors-dataset) or [HuggingFace](https://huggingface.co/datasets/AxonData/age-estimation-minors-face-dataset-10-30)
2. **Request access** at [axonlab.ai](https://axonlab.ai/dataset/age-estimation-face-dataset/)
3. **Contact us** at sales@axonlabs.pro


