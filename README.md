# Meta-path-aware Homophily Inference and Heterophily Extraction for Heterogeneous Graph Contrastive Learning

This repository provides the implementation of **HILT** (**H**omophily **I**nference and heterophi**L**y ex**T**raction).

## Dataset

Extract `dataset.zip` in the project root. The directory structure should be:

```text
dataset/
├── ACM/
├── DBLP/
├── IMDB/
└── Yelp/
```

## Run

Set `model_name` in `main.py`:

```python
args = get_args(model_name="HILT", dataset="ACM", custom_key="Node")
```

Train HILT on each dataset:

```bash
python main.py --dataset ACM
python main.py --dataset DBLP
python main.py --dataset IMDB
python main.py --dataset Yelp
```

Evaluate the pretrained parameters in `best/<DATASET>/best.pkl`:

```bash
python main.py --dataset ACM --load_parameter
python main.py --dataset DBLP --load_parameter
python main.py --dataset IMDB --load_parameter
python main.py --dataset Yelp --load_parameter
```

## Requirements

- Python 3.12
- PyTorch 2.11.0
- NumPy 2.4.3
- SciPy 1.17.1
- scikit-learn 1.8.0
- tqdm 4.67.3
- ruamel.yaml >= 0.18
- CUDA 12.8
