---
title: Introduction to GitHub Actions for Beginners
author: John Ng
date: "2024-05-01"
theme: default
---

# Introduction to GitHub Actions for Beginners

**Automate Your Workflow with GitHub Actions**

---

# Agenda

1. What are GitHub Actions?
2. Why Use GitHub Actions?
3. Key Concepts
4. YAML Basics
5. Creating Your First Workflow
6. Live Demo

---

# What are GitHub Actions?

- **Definition:** GitHub Actions is a CI/CD platform that allows you to automate your build, test, and deployment pipeline.
- **Key Features:**
  - Automate workflows directly in your GitHub repository.
  - Extensive marketplace of actions.
  - Supports multiple languages and platforms.

---

# Why Use GitHub Actions?

- **Benefits:**
  - Seamless integration with GitHub repositories.
  - Customizable workflows.
  - Free for public repositories.
- **Use Cases:**
  - Continuous Integration and Continuous Deployment (CI/CD).
  - Automated testing.
  - Scheduled tasks and notifications.

---

# Key Concepts

- **Workflows:** Automated processes that you set up in your repository.
- **Jobs:** A set of steps that execute on the same runner.
- **Actions:** Individual tasks that can be combined to create jobs and workflows.
- **Runners:** Servers that run your workflows when they're triggered.

---

# YAML Basics

```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Step Name
        run: echo "Hello, World!"
```
---

# Github Action Basics
````md magic-move

```yaml
name: Workflow Name
```
```yaml
name: Workflow Name
on: [push, pull_request]
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
```
```yaml
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Step Name
        run: echo "Hello, World!"       
```

````

---
# Github Action Key Parts

```yaml {1|2|4-10|5-10|7-10}
name: Workflow Name
on: [push, pull_request]

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Step Name
        run: echo "Hello, World!"
```
---
# Components

<Counter :count="4"/>



---