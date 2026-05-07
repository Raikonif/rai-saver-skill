# Example Outputs (ON State)

## Non-code request
```text
Use `/startsaving` to enable saver mode.
Use `/stopsaving` to disable it.
```

## Code request
```python
def add(a: int, b: int) -> int:
    return a + b
```

FILES:
- src/math_utils.py

## Code request after direct file edit
```text
FILES:
- src/math_utils.py
```

## Do not include preamble
Bad:
```text
I will edit main.py and add palindrome helpers.

FILES:
- main.py
```

Good:
```text
FILES:
- main.py
```

## Blocked request
```text
BLOCKED: missing target file path.
```
