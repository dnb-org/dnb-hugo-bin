This is a highly experimental project at the moment and tries to combine and normalise the build system across all `@dnb-org/dnb-hugo-*` projects. Use with caution. Don't blame me if it breaks everything ;) Once I have a version that I trust it will reach v1.0.0.

## Principal mode of operation

The scripts are contained in a `bin` directory and have a structured setup with helpers and scripts and an overall uniform way of function. The `bin` folder should be added to the repository that is using the scripts, as a folder, not a submodule. Updating overrides the existing files and can commit updates to the repository.

## Initial setup

Note that this will override any file in `bin`. Either modify to fit your paths or commit all files in `bin` so you have something to `git diff` against at first install.

```bash
git clone https://github.com/dnb-org/dnb-hugo-bin tmp.bin && mkdir -p bin && cp -R tmp.bin/bin bin && rm -rf tmp.bin
```

## Update

Run `bin/self/update`. Then check with `git diff` what's changed (or subscribe to releases on GitHub).
