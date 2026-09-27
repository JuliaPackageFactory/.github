# Julia Package Factory

I have been involved in the development of several Julia packages through [my own research](https://ohno.github.io/) and my work with [JuliaFewBody](https://github.com/orgs/JuliaFewBody/repositories). Working on these packages meant repeating many of the same setup steps, so I had been thinking about automating them. Then, in June 2025, a colleague asked me:

> Hey. I had AI create a Julia package, but the documentation isn't deploying properly. How can I fix it?

That question motivated me to develop [PkgFactory.jl](https://github.com/JuliaPackageFactory/PkgFactory.jl). PkgFactory.jl automates the process from creating a repository to deploying package infrastructure.

## Usage

PkgFactory.jl can be used through **CLI**, **Web UI** (local, hosted), and **MCP** (stdio, Streamable HTTP). The easiest way is to access and use this website: https://pkgfactory-web.ohnolab.workers.dev/

## Templates

PkgFactory.jl currently provides [three templates](https://github.com/JuliaPackageFactory/PkgFactory.jl/tree/main/templates) with different levels of functionality. You can see examples automatically generated from these templates in the following repositories:

| Template                                                                          | Purpose                                                                    |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [TemplateMinimum.jl](https://github.com/JuliaPackageFactory/TemplateMinimum.jl)   | Minimal Julia package setup                                                |
| [TemplateSimple.jl](https://github.com/JuliaPackageFactory/TemplateSimple.jl)     | Standard package setup with documentation and CI                           |
| [TemplateAllInOne.jl](https://github.com/JuliaPackageFactory/TemplateAllInOne.jl) | Full-featured package setup with development and quality-assurance tooling |

## Feedback

Please share your feedback in [GitHub Discussions](https://github.com/JuliaPackageFactory/PkgFactory.jl/discussions). If you've used PkgFactory.jl to create a package, I'd love to see it—please share a link there as well.
