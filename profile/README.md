# Julia Package Factory

In June 2025, a colleague asked me:

> Hey. I had AI create a Julia package, but the documentation isn't deploying properly. How can I fix it?

That question motivated me to develop [PkgFactory.jl](https://github.com/JuliaPackageFactory/PkgFactory.jl).

## Overview

PkgFactory.jl automates the process from creating a repository to deploying package infrastructure. There's no need to set up deployment keys or manually configure repository settings. See the [PkgFactory.jl documentation](https://juliapackagefactory.github.io/PkgFactory.jl/) to get started.

## Templates

[PkgFactory.jl](https://github.com/JuliaPackageFactory/PkgFactory.jl) currently provides [three templates](https://github.com/JuliaPackageFactory/PkgFactory.jl/tree/main/templates) with different levels of functionality. You can see examples generated from these templates in the following repositories:

| Template                                                                          | Purpose                                                                    |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [TemplateMinimum.jl](https://github.com/JuliaPackageFactory/TemplateMinimum.jl)   | Minimal Julia package setup                                                |
| [TemplateSimple.jl](https://github.com/JuliaPackageFactory/TemplateSimple.jl)     | Standard package setup with documentation and CI                           |
| [TemplateAllInOne.jl](https://github.com/JuliaPackageFactory/TemplateAllInOne.jl) | Full-featured package setup with development and quality-assurance tooling |

[PkgTemplates.jl](https://github.com/JuliaCI/PkgTemplates.jl) was incredibly helpful to me when I was learning how to configure CI. However, its approach of generating package templates on disk does not align well with the current design of PkgFactory.jl, although support for PkgTemplates.jl may be added in the future. In addition, its large number of configuration options can be overwhelming for beginners due to the [Paradox of Choice](https://en.wikipedia.org/wiki/The_Paradox_of_Choice).

## Interfaces

[PkgFactory.jl](https://github.com/JuliaPackageFactory/PkgFactory.jl) can be used through:

* **CLI** — create packages from the terminal
* **Web UI** — create and configure packages from a browser
* **MCP** — create packages from AI applications

## Feedback

Coming soon.

## About me

I have been involved in the development of several Julia packages through [my own research](https://ohno.github.io/) and my work with [JuliaFewBody](https://github.com/orgs/JuliaFewBody/repositories).

Guides to Julia package development include [How to develop a Julia package](https://julialang.org/contribute/developing_package/), [Modern Julia Workflows — Sharing your code](https://modernjuliaworkflows.org/sharing/), [Pkg.jl — Creating Packages](https://pkgdocs.julialang.org/v1/creating-packages/), and [Julia — Workflow Tips](https://docs.julialang.org/en/v1/manual/workflow-tips/). In Japanese, additional information can be found on [Qiita](https://qiita.com/search?q=Julia+%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8) and [Zenn](https://zenn.dev/search?q=Julia%2520%25E3%2583%2591%25E3%2583%2583%25E3%2582%25B1%25E3%2583%25BC%25E3%2582%25B8&mode=semantic).

These resources have been extremely useful for developing Julia packages, but the process still involves many manual steps.

Shouldn't we automate them?
