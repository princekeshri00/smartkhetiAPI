<h1>API Server Setup</h1>
<br>

1> Open your terminal inside <code>smartkheti</code> folder

2> <code>pip install -r requirements.txt</code>

3> <code>cd model</code>

4> <code>python3 train_model.py</code>   (<i>Make sure to train the model before starting the Django server</i>)

5> <code>cd ..</code>

6> <code>cd app</code>

7> <code>python3 manage.py runserver</code>

<b>Now the API server is ready for use at <i>localhost</i> port 8000</b>
<br>
<hr>
<br>
<h3>Request format -> <h3>
  
```
curl -X POST http://127.0.0.1:8000/api/predict/ \
     -H "Content-Type: application/json" \
     -d '{
           "N": <float>,
           "P": <float>,
           "K": <float>,
           "temperature": <float>,
           "humidity": <float>,
           "ph": <float>,
           "rainfall": <float>
         }'
```

<br>

<b>Sample Request for Rice -> <b>
```
curl -X POST http://127.0.0.1:8000/api/predict/ \
     -H "Content-Type: application/json" \
     -d '{
           "N": 15,
           "P": 20,
           "K": 45,
           "temperature": 25,
           "humidity": 90,
           "ph": 8,
           "rainfall": 80
         }'
```
<br>
<hr>
<br> 
If you face any issues, feel free to raise queries in the <b>issue</b> section.
