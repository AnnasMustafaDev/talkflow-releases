# winget manifests

Manifests for the [Windows Package Manager](https://learn.microsoft.com/windows/package-manager/) package `AnnasMustafaDev.Talkflow`, ready to submit to [microsoft/winget-pkgs](https://github.com/microsoft/winget-pkgs).

Validate and submit them with [wingetcreate](https://github.com/microsoft/winget-create):

```powershell
winget validate --manifest winget\manifests\a\AnnasMustafaDev\Talkflow\1.0.0
wingetcreate submit winget\manifests\a\AnnasMustafaDev\Talkflow\1.0.0
```

For a new version: `wingetcreate update AnnasMustafaDev.Talkflow --version x.y.z --urls <setup URL> --submit`.
