# Julia Package Factory

I have been involved in the development of several Julia packages through [my own research](https://ohno.github.io/) and my work with [JuliaFewBody](https://github.com/orgs/JuliaFewBody/repositories). Working on these packages meant repeating many of the same setup steps, so I had been thinking about automating them. Then, in June 2025, a colleague asked me:

> Hey. I had AI create a Julia package, but the documentation isn't deploying properly. How can I fix it?

## Usage

Simply provide basic information such as the package name and GitHub username, and ~PkgFactory.jl~ [PkgFactory.ts](https://github.com/JuliaPackageFactory/PkgFactory.ts) automatically creates the repository and sets up the package infrastructure. ~PkgFactory.jl~ PkgFactory.ts can be used through several interfaces, including **CLI**, **Web UI** (local or hosted), and **MCP** (stdio or Streamable HTTP). The easiest way to get started is with the hosted Web UI:

https://pkgfactory-staging.ohnolab.workers.dev/

## Templates

~PkgFactory.jl~ PkgFactory.ts currently provides [three templates](https://github.com/JuliaPackageFactory/PkgFactory.ts/tree/main/packages/pkgfactory/templates) with different levels of functionality. You can see examples automatically generated from these templates in the following repositories:

| Template                                                                  | Purpose                                                                    |
| ------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [TestMinimum.jl](https://github.com/JuliaPackageFactory/TestMinimum.jl)   | Minimal Julia package setup                                                |
| [TestSimple.jl](https://github.com/JuliaPackageFactory/TestSimple.jl)     | Standard package setup with documentation and CI                           |
| [TestAllInOne.jl](https://github.com/JuliaPackageFactory/TestAllInOne.jl) | Full-featured package setup with development and quality-assurance tooling |

## Feedback

Please share your feedback in [GitHub Discussions](https://github.com/JuliaPackageFactory/PkgFactory.ts/discussions). If you've used PkgFactory.jl to create a package, I'd love to see it—please share a link there as well.
