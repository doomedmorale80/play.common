# Play.Common
Common libraries used by Play Economy services.

## Create and publish package
```powershell
$version="1.0.6"
$owner="doomedmorale80"
$gh_pat="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"

dotnet pack src\Play.Common\ --configuration Release -p:PackageVersion=$version -p:RepositoryUrl=https://github.com/$owner/play.common -o ..\packages

dotnet nuget push ..\packages\Play.Common.$version.nupkg --api-key $gh_pat --source "github"
```