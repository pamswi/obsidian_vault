framework for dynamic html- developing web apps using Python

previously run on 
```
http-server
```

whereas now we can use micro web framework written in Python (when using app.py)

```python
from flask import Flask, render_template, request

app = Flask(__name__)

@app.route("/")
def index():
	return render_template("index.html")
```
the above imports the necessary bits from flask and then utilises them 


-------------------------------------- 

1. install python 
2. install pip (it's like npm but for python)
3. install flask 
4. create a virtual environment
5. activate it 
6. run python app.py