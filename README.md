# Esquio v3.0 Github Action rolloff feature

With this Esquio Github action you can disable a feature in an Github Actions workflow.[Esquio](https://esquio.readthedocs.io/en/latest/).

Please read [Esquio readthedocs](https://esquio.readthedocs.io/en/latest/) first to fully understand Esquio Feature Toggle package configuration and possibilities.

## Parameters needed

- **esquio-url**: Url to the Esquio Api. i.e.: https://myesquioui.deployment.com
- **esquio-api-key**: API key to authenticate to esquio. Recommended to store as [Github secret](https://help.github.com/en/github/automating-your-workflow-with-github-actions/virtual-environments-for-github-actions#creating-and-using-secrets-encrypted-variables)
- **product-name**: Name of the product to which the feature belongs.
- **feature-name**: Name of the feature to disable.

## Example

```YAML
      - name: Esquio rolloff
        uses: actions/esquio-rolloff-v3
        id: esquio-rolloff-v3
        with:
          esquio-url: 'https://esquiodemoui.azurewebsites.net/'
          esquio-api-key: ${{ secrets.apikey }}
          product-name: 'Default'
          feature-name: 'MatchScore'
```
