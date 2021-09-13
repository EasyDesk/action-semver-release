# action-semver-release

This action automates the processes of updating major version and minor version tags when a release is triggered.  
Then, it automates the process of creating GitHub releases.

## Usage
The expected version format is a [Semantic Version](https://semver.org/) possibly prefixed by a `v`.
If the version isn't conform to Semantic Versioning the action will **fail**.
In order to avoid this, you **must handle conditional execution of this action depending on the version format**.

### Usage example
```yaml
    steps:
      - uses: EasyDesk/action-semver-release@v1
        with:
          prefix: Semantic Version Release Action
          version: v1.0.0
          prerelease: false
          files: |
            LICENSE
```

## Credits
This action couldn't work without [marvinpinto/action-automatic-releases](https://github.com/marvinpinto/action-automatic-releases).
