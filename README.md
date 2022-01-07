# Github Action: pypi-build-publish

Github action to build and publish to PyPI [PEP 518](https://www.python.org/dev/peps/pep-0518/) compliant projects (flit, poetry,...).

Usage:

```yaml
- use: conchylicultor/pypi-build-publish@v1
  with:
    pypi-token: ${{ secrets.PYPI_API_TOKEN }}
```

The action assume:

* The project has a `pyproject.toml` (or `setup.py`) in the top-level directory.
* Python and pip are installed (e.g. by `actions/setup-python@v2`).

## Inputs

* `pypi-token`: The PyPI API token to use. (required)

## Outputs

None.
