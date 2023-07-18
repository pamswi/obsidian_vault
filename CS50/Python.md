object oriented programming - values / variables have properties as well as built-in functions 
e.g
```python
s = input("do you agree?")
s= s.lower()
```

```python
for i in range(3):
print("meow")
```

def to define a function

```python
def main():
	for i in range(3):
		meow()

def meow():
	print("meow")

main()
```

do something forever

```python

from cs50 import get_int

while True:
	n = get_int("Height: ")
	if n > 0:
		break

for i in range(n):
	print("#")
```

csv
csv.reader(file)
csv.DictReader(file)


[ ] to access dict with "row name"

dict() is the same as = {}

