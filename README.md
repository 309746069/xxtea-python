# XXTEA for Python

[![Build Status](https://travis-ci.org/xxtea/xxtea-python.svg?branch=master)](https://travis-ci.org/xxtea/xxtea-python)
[![PyPI](https://img.shields.io/pypi/v/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/l/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/pyversions/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/implementation/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/status/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/dm/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/dw/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)
[![PyPI](https://img.shields.io/pypi/dd/xxtea-py.svg)](https://pypi.python.org/pypi/xxtea-py)

## Introduction

XXTEA is a fast and secure encryption algorithm. This is a XXTEA library for Python.

It is based on CFFI, so it is fast and support both cpython and pypy.

It is different from the original XXTEA encryption algorithm. It encrypts and decrypts raw binary data instead of 32bit integer array, and the key is also the raw binary data.

## Installation

```sh
pip install xxtea-py
```

## Usage

Python2:
```python
import xxtea
text = "Hello World! 你好，中国！"
key = "1234567890"
encrypt_data = xxtea.encrypt(text, key)
decrypt_data = xxtea.decrypt(encrypt_data, key)
print(text == decrypt_data);
```

Python3:
```python
import xxtea
text = "Hello World! 你好，中国！"
key = "1234567890"
encrypt_data = xxtea.encrypt(text, key)
decrypt_data = xxtea.decrypt_utf8(encrypt_data, key)
print(text == decrypt_data);
```
