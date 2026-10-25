# How to Train Your LLM — notebooks

Runnable companions to **How to Train Your ~~Dragon~~ LLM**, one of the
[AI/Biz books](https://www.ai.biz/books/how-to-train-your-llm/).

Every notebook opens directly in Google Colab. Nothing to install.

| Ch | Notebook | Chapter | Open |
|---|---|---|---|
| 1 | `01-what-a-language-model-is.ipynb` | [What a Language Model Is](https://www.ai.biz/books/how-to-train-your-llm/what-a-language-model-is/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/01-what-a-language-model-is.ipynb) |
| 2 | `02-tokenisation.ipynb` | [Tokenisation](https://www.ai.biz/books/how-to-train-your-llm/tokenisation/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/02-tokenisation.ipynb) |
| 3 | `03-the-data.ipynb` | [The Data](https://www.ai.biz/books/how-to-train-your-llm/the-data/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/03-the-data.ipynb) |
| 4 | `04-attention.ipynb` | [Attention, From a Lookup Table Up](https://www.ai.biz/books/how-to-train-your-llm/attention-from-a-lookup-table-up/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/04-attention.ipynb) |
| 5 | `05-the-transformer-block.ipynb` | [The Transformer Block](https://www.ai.biz/books/how-to-train-your-llm/the-transformer-block/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/05-the-transformer-block.ipynb) |
| 6 | `06-the-training-loop.ipynb` | [The Training Loop](https://www.ai.biz/books/how-to-train-your-llm/the-training-loop/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/06-the-training-loop.ipynb) |
| 7 | `07-scaling-laws.ipynb` | [Scaling Laws and What Compute Buys](https://www.ai.biz/books/how-to-train-your-llm/scaling-laws-and-what-compute-buys/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/07-scaling-laws.ipynb) |
| 8 | `08-infrastructure.ipynb` | [Infrastructure, Parallelism and Checkpoints](https://www.ai.biz/books/how-to-train-your-llm/infrastructure-parallelism-and-checkpoints/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/08-infrastructure.ipynb) |
| 9 | `09-evaluating-a-base-model.ipynb` | [Evaluating a Base Model](https://www.ai.biz/books/how-to-train-your-llm/evaluating-a-base-model/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/09-evaluating-a-base-model.ipynb) |
| 10 | `10-alignment.ipynb` | [Alignment, and Where This Book Stops](https://www.ai.biz/books/how-to-train-your-llm/alignment-and-where-this-book-stops/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/10-alignment.ipynb) |
| 11 | `11-serving.ipynb` | [Serving and the Cost of Inference](https://www.ai.biz/books/how-to-train-your-llm/serving-and-the-cost-of-inference/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/11-serving.ipynb) |
| 12 | `12-the-bill.ipynb` | [What Training One Costs, and When You Should Not](https://www.ai.biz/books/how-to-train-your-llm/what-training-one-costs-and-when-you-should-not/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-train-your-llm-notebooks/blob/main/12-the-bill.ipynb) |

## Saving your work

Colab opens these notebooks straight from GitHub, so you can run and edit them
immediately. Your changes are **not** saved back on their own. There are two
ways to keep them.

**Save to your Google Drive.** In Colab, choose *File → Save a copy in Drive*.
You get your own copy in your own account, and the original stays as it was.
This is the quickest option if you are just working through a chapter.

**Fork this repository first.** Fork it to your GitHub account, open the
notebook from your fork, and *File → Save a copy in GitHub* will write your
changes back to it. Better if you want your work version controlled, or if you
are going through the whole book.

## Running locally instead

Colab is the fastest way to start, not the only way. Clone or fork this
repository and run everything on your own machine:

```bash
git clone https://github.com/aibizx/how-to-train-your-llm-notebooks.git
cd how-to-train-your-llm-notebooks

# with uv (fastest)
uv venv && source .venv/bin/activate
uv pip install -r requirements.txt

# or with the standard library
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

jupyter lab
```

On Windows, activate with `.venv\Scripts\activate` instead.

Everything here runs on CPU. The first three chapters need only NumPy and
Matplotlib; from chapter 4 the models are built in PyTorch and sized so a
laptop trains them in a few minutes. Chapter 1 runs in about ten seconds and
the longest, chapter 6's sweeps, in about five minutes.

## How this repo is maintained

Notebooks are authored alongside the chapters in the site repository and pushed
here through the GitHub Contents API. The Colab badge at the top of each
notebook is regenerated on every push, so the links never go stale. Every code
cell is executed before anything is pushed.

Each book gets its own notebook repository, so you can clone just the one you
are working through.

---

MIT licensed. © Sameer Gupta · [ai.biz](https://www.ai.biz/)
