---
published: true
layout: post
categories:
  - Python
---
Unit test pada python digunakan pada unit-unit kode python untuk dengan lebih mudah menemukan adanya kesalahan. Menggunakan library bawaan python unittest, unit test pada python bisa dilakukan.

### Help
```
python3 -m unittest -h
```

- awali unit dengan nama test_

### Example test_json_search.py
```
# Fill the Python code in this file
import unittest
from recrusive_json_search import *
from test_data import *

class json_search_test(unittest.TestCase):
    '''test module to test search function in `recursive_json_search.py`'''
    def test_search_found(self):
        '''key should be found, return list should not be empty'''
        self.assertTrue([]!=json_search(key1,data))
    def test_search_not_found(self):
        '''key should not be found, should return an empty list'''
        self.assertTrue([]==json_search(key2,data))
    def test_is_a_list(self):
        '''Should return a list'''
        self.assertIsInstance(json_search(key1,data),list)

if __name__ == '__main__':
	unittest.main()
```

### Run
```
python3 -m unittest -v test_json_search.py 

```
Output:
```
[]
test_is_a_list (test_json_search.json_search_test)
Should return a list ... ok
test_search_found (test_json_search.json_search_test)
key should be found, return list should not be empty ... FAIL
test_search_not_found (test_json_search.json_search_test)
key should not be found, should return an empty list ... ok

======================================================================
FAIL: test_search_found (test_json_search.json_search_test)
key should be found, return list should not be empty
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/home/devasc/labs/devnet-src/unittest/test_json_search.py", line 10, in test_search_found
    self.assertTrue([]!=json_search(key1,data))
AssertionError: False is not true

----------------------------------------------------------------------
Ran 3 tests in 0.002s

FAILED (failures=1)

```
