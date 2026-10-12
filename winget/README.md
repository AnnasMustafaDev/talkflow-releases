# winget manifests

Manifests for the [Windows Package Manager](https://learn.microsoft.com/windows/package-manager/) package `Zehnix.Talkflow`, ready to submit to [microsoft/winget-pkgs](https://github.com/microsoft/winget-pkgs).

Validate and submit them with [wingetcreate](https://github.com/microsoft/winget-create):

```powershell
winget validate --manifest winget\manifests\z\Zehnix\Talkflow\1.1.1
wingetcreate submit winget\manifests\z\Zehnix\Talkflow\1.1.1
```

Submit only the newest version; older folders stay for reference.

For a new version: `wingetcreate update Zehnix.Talkflow --version x.y.z --urls <setup URL> --submit`.
