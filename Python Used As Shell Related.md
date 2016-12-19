#Python Shell
##OS
```python
import os
cwd = os.getcwd()
os.path.dirname()
os.path.basename()
os.path.exists()
os.listdir()
os.chdir(cwd)
os.system()
```
## xml
```python
try:
    import xml.etree.cElementTree as ET
except ImportError:
    import xml.etree.ElementTree as ET

s = '''<?xml version="1.0" encoding="UTF-8" standalone="yes"?> <Output> <Message>Successfully downloaded S_D_xxxxx_20161129.txt.gz</Message> </Output>'''

tree = ET.fromstring(s)
message = ''.join(tree.find('Message').itertext())
```

> Successfully downloaded S_D_xxxxx_20161129.txt.gz

##gzip
dynamicly open gzip file or normal file
```python
open_method = gzip.open if file_name.endswith('gz') else open
f = open_method(file_path, 'rb')
```

