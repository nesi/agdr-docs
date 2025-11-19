# agdr-docs
Mkdocs based AGDR support pages.

[AGDR support files example](https://nesi.github.io/agdr-docs/docs/index.md)

## Update info

Nov 19 2025 (MP): New builds for release notes 2025_11_18.md
fail with a proselint function definition
problem in checks/run_proselint.py.
Something has changed under the covers. Looks like Cal
has already dealt with this and has adjusted run_proselint.py
in the nesi support-docs repo. I stole that and removed the specification
of
```proseline==0.14.0```
in the requirements.txt file. Then while building, another error
related to lxml. On a hunch that XML is not involved, I just commented
out lxml in the requirements.txt file and it built and deployed fine.
