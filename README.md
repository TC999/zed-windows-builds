# Unofficial builds of Zed for Windows

**NOTE: This is not a support channel for Zed on Windows.**

These builds are for those who want to live on the bleeding edge or just want to test Zed out on Windows. 

Any issues with the Windows build should go through official channels, as this repository does not concern itself with the source code of Zed or issues found therein. 

If you have suggestions for improvements to the build process, please start a discussion or make a PR. 

All installation instructions below require that [Scoop](https://scoop.sh/) is installed on your system.

## Stable builds

```pwsh
scoop bucket add extras
scoop install extras/zed
```

## Nightly builds

```pwsh
scoop bucket add versions
scoop install versions/zed-nightly
```

## Vulkan doesn't work for you?

Install the OpenGL version

### Stable OpenGL version

```pwsh
scoop bucket add extras
scoop install extras/zed-opengl
```

### Nightly OpenGL version

```pwsh
scoop bucket add versions
scoop install versions/zed-opengl-nightly
```

### For Windows 10 users

Zed may not start unless you install the [Microsoft Visual C++ Redistributable 2022](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#visual-studio-2015-2017-2019-and-2022) package. If you are using Scoop, you can install it using the following command:

```pwsh
scoop bucket add extras
scoop install vcredist2022
```

## Updates

```pwsh
# Stable version
scoop update zed
# Stable OpenGL version
scoop update zed-opengl
# Nightly version
scoop update zed-nightly
# Nightly OpenGL version
scoop update zed-opengl-nightly
```

## Is it safe?

This repository is just a [simple GitHub workflow](./.github/workflows/build.yml) that builds Zed from `main` and publishes a release every night at UTC+0000. (Additionally on push for testing).

See the [Zed homepage](https://zed.dev/) or [official repository](https://github.com/zed-industries/zed) for more details.
