# MurphySec code scan

Integrating the MurphySec code security detection tool into the CI/CD process can detect security vulnerabilities in real time for each code update and quickly repair these security vulnerabilities.



## Usage

### Inputs
- `MURPHYSEC_TOKEN`: MurphySec official website token

## Example usage
```yaml
name: "MurphySec code scan"
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: MurphySec code scan
        uses: murphysecurity/actions@v1.1.3
        with:
          MURPHYSEC_TOKEN: ${{ secrets.MURPHYSEC_TOKEN }}
```

