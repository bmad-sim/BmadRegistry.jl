# BmadRegistry.jl
Local Julia registry for Julia packages that have not yet been submitted to the official Registrator.

The need for this is discussed at https://discourse.julialang.org/t/developing-interdependent-local-unregistered-packages/103936/10

Also see https://discourse.julialang.org/t/github-ci-add-custom-registry/63590

## Maintaining the Registry

Instructions at https://github.com/GunnarFarneback/LocalRegistry.jl

## Create Registry

To create the local version of BmadRegistry.jl do (only needs to be done once per Julia installation):
```
using LocalRegistry
create_registry("BmadRegistry", "https://github.com/bmad-sim/BmadRegistry.jl", push = true)
using Pkg
pkg"registry add https://github.com/bmad-sim/BmadRegistry.jl"
```

## Register a Package or a New Version of a Package

The recommended way to register a package or a new version of a
package is simply:

```
using LocalRegistry
register()
```

For this to work you need to either have the package in your current
directory or have the package activated.
