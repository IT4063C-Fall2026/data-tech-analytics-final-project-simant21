# Which Vulnerabilities Do Attackers Actually Exploit?


## Project Overview
### Topic
Security teams can't patch every vulnerability, so they need to know which ones attackers actually exploit. 

### Project Questions
1. Which CVE characteristics (CVSS severity, vendor, weakness type, age) are associated with being listed as actively exploited?
2. Does EPSS tell us more about exploitation than CVSS does?
3. How long does it take from a CVE's publication to its KEV listing, and does it vary by vendor or weakness type?

### What an Answer Looks Like
- Bar chart: share of CVEs in KEV by CVSS band
- Scatter plot: EPSS vs. CVSS, with KEV CVEs highlighted
- Box plot: days from publication to KEV listing, by vendor
- Table: top weakness types (CWE) among KEV CVEs

### Data Sources
| Source | Type | Key fields |
|---|---|---|
| NVD CVE API | API | CVE ID, publish date, CVSS, CWE, vendor |
| CISA KEV catalog | File (JSON) | CVE ID, date added, vendor/product |
| FIRST EPSS scores | File (CSV) | CVE ID, EPSS score, percentile |

**How they relate:** All three share the CVE ID. NVD is the base table, left-joined with KEV and EPSS. A CVE missing from KEV is treated as "not known exploited."

**Limitations:** EPSS is a current snapshot, and KEV lists CVEs when CISA adds them, not when exploitation began.
## Self Assessment and Reflection

<!-- Edit the following section with your self assessment and reflection -->

### Self Assessment
<!-- Replace the (...) with your score -->

| Category          | Score    |
| ----------------- | -------- |
| **Setup**         | ... / 10 |
| **Execution**     | ... / 20 |
| **Documentation** | ... / 10 |
| **Presentation**  | ... / 30 |
| **Total**         | ... / 70 |

### Reflection
<!-- Edit the following section with your reflection -->

#### What went well?
#### What did not go well?
#### What did you learn?
#### What would you do differently next time?

---

## Getting Started
### Installing Dependencies

To ensure that you have all the dependencies installed, and that we can have a reproducible environment, we will be using `pipenv` to manage our dependencies. `pipenv` is a tool that allows us to create a virtual environment for our project, and install all the dependencies we need for our project. This ensures that we can have a reproducible environment, and that we can all run the same code.

```bash
pipenv install
```

This sets up a virtual environment for our project, and installs the following dependencies:

- `ipykernel`
- `jupyter`
- `notebook`
- `black`
  Throughout your analysis and development, you will need to install additional packages. You can can install any package you need using `pipenv install <package-name>`. For example, if you need to install `numpy`, you can do so by running:

```bash
pipenv install numpy
```

This will update update the `Pipfile` and `Pipfile.lock` files, and install the package in your virtual environment.

## Helpful Resources:
* [Markdown Syntax Cheatsheet](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [Dataset options](https://it4063c.github.io/guides/datasets)
