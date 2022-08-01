#  Build Number Incrementer

Increment build number as a secret in github repository

## Usage

## Inputs

### buildNumberSecretName

**Required** `String` Build number secret name.

### currentBuildNumberValue

**Required** `String` Current build number, the increment will be executed based on this value.


### token

**Required** `String` Repository access token (Github token)

### repository

**Required** `String` Repository to store. Default `github.repository` [context](https://docs.github.com/en/actions/reference/context-and-expression-syntax-for-github-actions#github-context)

## Outputs

### status

Response status code 

### data

Response json payload

## Examples

```YAML
uses: Tiiik/build-number-incrementer@v1.0.0
with:
  buildNumberSecretName: 'MY_SECRET_NAME'
  currentBuildNumberValue: 'Lorem ipsun dolor simit'
  repository: Tiiik/build-number-incrementer
  token: ${{ secrets.GITHUB_TOKEN }}
```


## References

### References

- [Get a repository public key](https://developer.github.com/v3/actions/secrets/#get-a-repository-public-key)
- [Create or update repository secret](https://developer.github.com/v3/actions/secrets/#create-or-update-a-repository-secret)
