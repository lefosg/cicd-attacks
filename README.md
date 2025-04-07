# CI/CD Attack Playground

This repository is a **minimalistic demonstration environment** designed to explore and test **CI/CD pipeline attack vectors** using both **GitHub Actions** and **GitLab CI**.

## 🐍 app.py

The `app.py` file is a super simple Python script that prints "Hello, World!" to the console:

```python
print("Hello, World!")
```

What we want to do is containerize in the pipeline and explore potential attacks.
While the application itself is trivial, it serves as a placeholder for testing and demonstrating CI/CD workflows and potential risks associated with misconfigured pipelines.


## 🎯 Purpose
This repo is intended for educational and research purposes around CI/CD security. It helps demonstrate:

How attackers might exploit CI/CD pipelines (e.g., injecting malicious code, exfiltrating secrets, privilege escalation).
The differences in behavior between GitHub Actions and GitLab CI.
Best practices for securing CI/CD workflows.
⚠️ Warning: This project is for educational use only. Do not use any attack techniques demonstrated here in production environments or on systems you do not own or have permission to test.

For each platform, we have a vulnerable file and its hardened version. You can distinguish the differences in the files as the vulnerable lines are commented out.

## Vulnerabilities analysed:
1. Enable Debug Logging ([GH](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/troubleshooting-workflows/enabling-debug-logging)) -> Do not enable this option since it may output sensitive logs that you do not want to be visible (e.g., env vars with their values)

2. 