# mlem-demo
Demo for testing MLEM API, for the Medium Article [MLEM: A One Stop Shop for Productionizing your ML Models](https://medium.com/@ee.shetty/mlem-a-one-stop-shop-for-productionizing-your-ml-models-90855c331405)
<br><br>Run `model.ipynb` for the entire demo

## Prerequisites
```
pip install -r requirements.txt
```

## Getting IMDb data
You can access IMDb datasets [here](https://datasets.imdbws.com/)
For this example, download the following datasets
- title.basics.tsv
- title.ratings.tsv

## Serving on FastAPI

```
> mlem serve fastapi --model ratings_model
```
```
⏳️ Loading model from ratings_model.mlem
Starting fastapi server...
🖇️  Adding route for /predict
Checkout openapi docs at <http://0.0.0.0:8080/docs>
INFO:     Started server process [54845]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:8080 (Press CTRL+C to quit)
INFO:     127.0.0.1:63807 - "GET /docs HTTP/1.1" 200 OK
INFO:     127.0.0.1:63807 - "GET /openapi.json HTTP/1.1" 200 OK
INFO:     127.0.0.1:49181 - "POST /predict HTTP/1.1" 200 OK
```
