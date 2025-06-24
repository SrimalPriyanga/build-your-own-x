# Test Configurations for Build Your Own X

## Table of Contents
- [Unit Tests](#unit-tests)
- [Integration Tests](#integration-tests)
- [End-to-End Tests](#end-to-end-tests)
- [Test Tools & Frameworks](#test-tools--frameworks)

---

## Unit Tests

```yaml
unit:
    framework: pytest
    test_dir: tests/unit
    coverage:
        enabled: true
        threshold: 85
    run_on_commit: true
```

## Integration Tests

```yaml
integration:
    framework: pytest
    test_dir: tests/integration
    services:
        - database
        - cache
    run_on_pr: true
```

## End-to-End Tests

```yaml
e2e:
    framework: playwright
    test_dir: tests/e2e
    headless: true
    base_url: http://localhost:8000
    run_on_ci: true
```

## Test Tools & Frameworks

- **pytest**: Python unit/integration testing
- **playwright**: End-to-end browser testing
- **coverage.py**: Code coverage reporting

---

> Adjust paths and frameworks as needed for your project structure.