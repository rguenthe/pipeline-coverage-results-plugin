# Pipeline: Coverage Results Plugin

The plugin adds a pipeline step to access code coverage results.

Currently supported coverage providers:
- [code-coverage-api-plugin](https://jenkins.io/projects/gsoc/2018/code-coverage-api-plugin/)

# Usage

The method `getCoverageResult` can be used to access code coverage results.

- _Parameter_ `element`: the coverage element: e.g. `'Line'`, `'Conditional'` (depends on used coverage adapter)
- _Return_: Integer value representing the coverage in percent (`-1` if no coverage results were found)

If no parameter `element` is given it defaults to `'Line'`.

## Examples

These are examples for use with the `code-coverage-api-plugin` which provides `'Line'` and `'Conditional'` coverage elements for all adapters.

### Line coverage
```groovy
def lineCoverage = getCoverageResult('Line');
```

### Branch coverage
```groovy
def conditionCoverage = getCoverageResult('Conditional');
```
