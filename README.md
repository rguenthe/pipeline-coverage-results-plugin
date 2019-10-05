# Pipeline: Coverage Results Plugin

The plugin provides DSL methods to access code coverage results in jenkins pipelines.

Supported coverage sources:
* [code-coverage-api-plugin](https://jenkins.io/projects/gsoc/2018/code-coverage-api-plugin/)

## Examples

### Get coverage elements

```groovy
def lineCoverage = getCoverageResult('Line');
def conditionCoverage = getCoverageResult('Conditional');
```
