# radon-defuse-action
A GitHub Action for integrating radon-defuse in GitHub workflows.

## Inputs

## `model`

**Required** The id of the model to use for the prediction. The id can be found in th

## `language`

**Required** The language of the files to run the prediction on. Can be `ansible` or `tosca`.


## `url`

**Required** The API URL of the backend server.



## Example usage

```yaml
on: [push]

jobs:
  defect_prediction_job:
    runs-on: ubuntu-latest
    name: Run DEFUSE's model CONDITIONAL for Ansible
    steps:
      - name: Defect Prediction
        id: defect_prediction
        uses: radon-h2020/radon-defuse-action@v1.1
        with:
          model: 'NEWEKjxoBvRdTopqjjKW'
          language: 'ansible'
          url: 'https://28d1495a475d.ngrok.io/'
```
