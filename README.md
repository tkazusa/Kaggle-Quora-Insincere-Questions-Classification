# Quora-Insincere-Questions-Classification
## Getting started
### Setup kaggle api credential
Download kaggle.json and place in the location: ~/.kaggle/kaggle.json.
See details: https://github.com/Kaggle/kaggle-api

### Download and unzip datasets from competition page
```
docker-compose run cpu kaggle competitions download quora-insincere-questions-classification -p input
unzip "input/*.zip" -d input
```
