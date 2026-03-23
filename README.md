# langchain_test 2

## Getting started

To make it easy for you to get started with GitLab, here's a list of recommended next steps.

Already a pro? Just edit this README.md and make it your own. Want to make it easy? [Use the template at the bottom](#editing-this-readme)!

## Add your files and dependencies

- [ ] First create a venv python virtual environment
- [ ] Use below command to install dependency
```
pip install --require-hashes -r requirements.txt
```

- [ ] To add dependency in the development **Follow below steps instead of directly using pip install**
1. Add dependency in pyproject.toml, add version constrain if it is known in advance, **if it is not known, reference requirement.txt later and manually add inside the pyproject.toml**
2. Run the command
```
pip-compile -o requirements.txt --generate-hashes pyproject.toml
```
to check conflict and pin the related dependency in requirement.txt
3. Install dependency inside requirements.txt using command
```
pip install --require-hashes -r requirements.txt
```
4. If dependency is only used in test environment like pytest, add dependency in test and run
```
pip-compile -o requirements.txt --generate-hashes pyproject.toml --extra test
```
5. **Follow above steps instead of directly using pip install**

## Dependencies conflict or missing
1. Add specific version of the dependency in pyproject.toml (example, "numpy==1.24.3")
2. Follow instructions in "Add your files and dependencies"