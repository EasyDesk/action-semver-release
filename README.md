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

In this example, the existence of a 'v1.0.0' tag is expected.
The action is responsible to update 'latest', 'v1' and 'v1.0' tags to point to the same commit as 'v1.0.0'.

## Credits
This action couldn't work without [softprops/action-gh-release](https://github.com/softprops/action-gh-release).
