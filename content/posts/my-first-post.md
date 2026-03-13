+++
date = '2026-03-14T02:27:53+05:30'
draft = false
title = 'My First Post'
+++


First blog post test
Python Test code
```python
def greet(name: str) -> str:
    """Returns a greeting string."""
    return f"Hello, {name}!"

print(greet("Hugo"))
```


```yara
rule DetectMalware {
    meta:
        author = "researcher"
        description = "Detects suspicious PE files"
    strings:
        $magic = { 4D 5A }
        $str1 = "CreateRemoteThread" nocase
    condition:
        $magic at 0 and $str1
}
```