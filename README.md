# get-opensearch-version
Gets the OpenSearch Version from gradle properties

Thanks to @scrawfor99 for inspiring this action

```yaml
inputs:
  working-directory:
    description: 'The working directory to run the gradle command'
    default: .

outputs:
  version:
    description: 'The OpenSearch version from gradle properties'
```

## Usage:

```yaml
steps:
- id: get-version 
  uses: peternied/get-opensearch-version@v1
  with:
    working-directory: project-subdirectory
- run: echo "We are using OpenSearch version ${{ steps.get-version.outputs.version }} in this project"
```