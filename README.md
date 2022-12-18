# Solution for Bottle Class

```python
class Bottle:
    def __init__(self, size: int):
        if size <= 0:
            raise ValueError("Bottle size can be > 0")
        if not isinstance(size, int):
            raise TypeError("Bottle size should be integer")

        self.size = size
        self._water = 0

    @property
    def water(self):
        return self._water

    @water.setter
    def water(self, value):
        if not isinstance(value, int):
            raise TypeError("Water is measured in ml (integer)")

        if not (0 <= value <= self.size):
            raise ValueError(
                "Water can't be lower than 0 and "
                f"higher than bottle size ({self.size})"
                )

        self._water = value

```
