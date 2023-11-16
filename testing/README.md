# Testing

## Kaggle

### Importing datasets

1. Use `opendatasets` to import datasets from the Kaggle API.
2. Create an API key in the "Account" page in your Kaggle account.
3. Download and add the `kaggle.json` file to the testing directory.
4. *Adding the `kaggle.json` file to the same directory as the jupyter notebook allows the `opendatasets.download()` to automatically read the contents of `kaggle.json`. If not, import it to the notebook.*

### Embedding

Use open-source embedding models from HuggingFace using the `sentence-transformers` package.
- Ensure that you have (rustup)['https://rustup.rs/'] installed to run `pip install -U sentence-transformers` successfully.
- Ensure that you have run `pip install tqdm` before installing `sentence-transformers`.
- You may have to use `--user` in the installation.