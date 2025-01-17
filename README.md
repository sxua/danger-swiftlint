# [![Docker Hub](https://dockeri.co/image/41772ki/danger-swiftlint)](https://hub.docker.com/r/41772ki/danger-swiftlint)

Docker image for [Danger-Swift](https://github.com/danger/swift) using [SwiftLint](https://github.com/realm/SwiftLint)

# Usage Sample

## Local Docker

```sh
$ docker run -v `pwd`:`pwd` -w `pwd` 41772ki/danger-swiftlint local
```

## GitHub Actions

```yml
name: Danger
on:
  pull_request:
    paths:
      - '.swiftlint.yml'
      - '**/*.swift'
jobs:
  Danger:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Danger
        uses: 417-72KI/danger-swiftlint@v5.6
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Note for version
- v5.6: Swift 5.6
- v5.5: Swift 5.5
- v4: Swift 5.4 (no longer updated)
- v3: Swift 5.3 (no longer updated)
- v2: Swift 5.2 (no longer updated)
- v1: Swift 5.1 (no longer updated)
