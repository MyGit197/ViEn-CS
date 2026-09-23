# ViEn-CS

**ViEn-CS** is a multi-domain Vietnamese-English code-switching speech dataset
for automatic speech recognition (ASR). It contains naturally occurring
Vietnamese speech with English insertions collected from public media across 17
topics.

The complete dataset contains **99,334 utterances** and **402.11 hours** of
speech. Its 142.36-hour code-switching portion includes 9,489 distinct English
words. The data is organized into code-switching (`cs`) and Vietnamese-only
(`vi`) training, validation, and test splits.

## Dataset access

The dataset is hosted on Kaggle in four packages:

| Package | Included split(s) | Kaggle link |
|---|---|---|
| Code-switching training data | `cs_train` | [myspace04/my-cs-data](https://www.kaggle.com/datasets/myspace04/my-cs-data) |
| Vietnamese-only training data | `vi_train` | [myspace04/my-vi-data](https://www.kaggle.com/datasets/myspace04/my-vi-data) |
| Validation data | `cs_valid`, `vi_valid` | [myspace04/all-valid](https://www.kaggle.com/datasets/myspace04/all-valid) |
| Test data | `cs_test_e`, `cs_test_h`, `vi_test` | [myspace04/all-test](https://www.kaggle.com/datasets/myspace04/all-test) |

Each package can also be downloaded with the
[Kaggle CLI](https://github.com/Kaggle/kaggle-api):

```bash
kaggle datasets download -d myspace04/my-cs-data
kaggle datasets download -d myspace04/my-vi-data
kaggle datasets download -d myspace04/all-valid
kaggle datasets download -d myspace04/all-test
```

## Dataset statistics

| Split | Type | Duration (hours) | Utterances |
|---|---|---:|---:|
| `cs_train` | Code-switching train | 122.67 | 28,873 |
| `cs_valid` | Code-switching validation | 6.49 | 1,524 |
| `cs_test_e` | Standard code-switching test | 6.58 | 1,558 |
| `cs_test_h` | Rare-term code-switching test | 6.62 | 1,328 |
| `vi_train` | Vietnamese-only train | 246.81 | 62,770 |
| `vi_valid` | Vietnamese-only validation | 6.42 | 1,618 |
| `vi_test` | Vietnamese-only test | 6.53 | 1,663 |

Durations are rounded to two decimal places. The dataset-wide duration is
computed from the original, unrounded segment durations.

## Split design and annotations

- `cs_test_e` follows the distribution of the code-switching training data.
- `cs_test_h` is a harder rare-term set: approximately 90% of its utterances
  contain an English term occurring fewer than two times in `cs_train`.
- Training and validation labels were generated automatically and filtered by
  the dataset construction pipeline.
- The transcripts, code-switching terms, boundaries, and audio-text consistency
  of both code-switching test sets were manually verified by Vietnamese
  annotators with English proficiency.

## Intended use

ViEn-CS is released to support research on Vietnamese-English code-switching
ASR, low-resource speech recognition, dataset construction, and evaluation of
rare English terms embedded in Vietnamese speech.

## Citation

If you use ViEn-CS, please cite the accompanying paper:

> *ViEn-CS: A Multi-Domain Vietnamese-English Code-Switching Dataset*.

Full bibliographic information will be added after publication.

## License

This repository is released under the [Apache License 2.0](LICENSE). Please also
review the terms shown on each Kaggle dataset page before downloading or using
the data.
