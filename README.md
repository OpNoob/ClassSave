# ClassSave
A base class for saving and loading classes from disk.

## Install
```cmd
pip install ClassSave
```

## Usage
```python
from ClassSave import ClassSL


class TEST(ClassSL):
    def __init__(self, test_str=123, **kwargs):
        super().__init__(**kwargs)

        if not self._loaded:
            self.test_str = test_str
            print(self.test_str)


t = TEST(test_str=234, load=False, save_json=True, json_private=False)
t.save_class()
```
