# DmitryLegostaev.GitHubActions.PushNupkgToGitHub

### Usage example

```yml
- name: Push nuget package to GitHub
  uses: DmitryLegostaev/DmitryLegostaev.GitHubActions.PushNupkgToGitHub@main
  with:
    PROJECT_NAME: ${{ matrix.project }}
    NUGET_API_KEY: ${{ secrets.GITHUB_TOKEN }}
    GITHUB_GPR_NAMESPACE: ${GITHUB_REPOSITORY}
```

### Inputs

| Input name | Description | Required | Default value |
| - | - | - | - |
| PROJECT_NAME | Project name | true | |
| DOTNET_CONFIGURATION | Configuration name for .NET project | false | "Release" |
| NUGET_API_KEY | Key to use with nuget push | true | |
| GITHUB_GPR_URL | Github GPR url. | false | "https://nuget.pkg.github.com" |
| GITHUB_GPR_NAMESPACE | Github GRP project namespace | true | |
| DOTNET_VERSION | .NET version to use | false | "6.0.x" |
