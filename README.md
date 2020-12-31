# Toshling - a Python client library for the Toshl API

Toshling is an(other) implementation of a client for the [Toshl API](https://developer.toshl.com/docs/).

## Installation

Toshling can be installed from the PyPI using `pip`:
```
pip install toshling
```

## Usage

All interaction with Toshl is done via the `Client` class, which is constructed with your API key:
```python
import toshling

client = toshling.Client('xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx')
```

## Issues

Toshling has numerous flaws, mostly due to the incomplete [JSON Hyper-Schema](https://json-schema.org/draft/2019-09/json-schema-hypermedia.html) documents provided by Toshl, which are inconsistent, based on an old draft spec and do not match their actual API documentation.

Ideally the full client would be automatically generated from the schemas, but that is not currently possible. Instead, as much functionality as possible was implemented in a semi-automated manner, with the expectation that edge cases will present themself in day-to-day usage.

Please feel free to submit issues for consideration on GitHub.

## Related libraries

- [toshl](https://pypi.org/project/toshl/) - a seemingly unmaintained API client missing some key features such as getting entries.
- [toshl-api](https://pypi.org/project/toshl-api/) - an autogenerated client without much documentation.