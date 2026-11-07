# tridennote/scoop-bucket

[Scoop](https://scoop.sh) manifests for [Tridennote](https://github.com/tridennote/cli).

```powershell
scoop bucket add tridennote https://github.com/tridennote/scoop-bucket
scoop install tridennote
```

`bucket/tridennote.json` is regenerated from the latest GitHub release's `checksums.txt` by
`scripts/update-manifest.sh`. The **Update manifest** workflow runs it every 6 hours, on
demand (`gh workflow run update-manifest.yml -R tridennote/scoop-bucket`), or when it
receives a `tridennote-release` repository dispatch. The manifest also carries `checkver`
and `autoupdate`, so Scoop's own tooling can bump it.
