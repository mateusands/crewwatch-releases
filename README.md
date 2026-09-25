# crewwatch-releases

CrewWatch's desktop app: the packages for Linux (`.deb`, AppImage) and macOS (`.dmg`, Apple Silicon
and Intel), and the `latest.json` the installed app's updater reads. Download from
[Releases](https://github.com/mateusands/crewwatch-releases/releases); the installed app updates
itself from here.

The source is not in this repository. A release is built from a tag of the source by
[the Release workflow](.github/workflows/release.yml):

```bash
gh workflow run release.yml -R mateusands/crewwatch-releases -f tag=v2.7.0
```

The macOS packages are not signed by Apple: the first time, open the app from the Finder's context
menu (Open), or run `xattr -d com.apple.quarantine /Applications/CrewWatch.app`.
