# Julia Package Factory

<img width="2172" height="724" alt="hero" src="https://github.com/user-attachments/assets/eec1bec9-b372-4a48-9b91-37b8fb113b48" />

I have been involved in the development of several (more than 10, by hand) Julia packages through [my own research](https://ohno.github.io/) and my work with [JuliaFewBody](https://github.com/orgs/JuliaFewBody/repositories). Working on these packages meant repeating many of the same setup steps, which motivated me to automate them. Then, in June 2025, a question from a colleague prompted me to start this project:

> Hey. I had AI create a Julia package, but the documentation isn't deploying properly. How can I fix it?

## Usage

Simply provide basic information such as the package name and GitHub username, and [PkgFactory.ts](https://github.com/JuliaPackageFactory/PkgFactory.ts) automatically creates the repository and sets up the package infrastructure. PkgFactory.ts can be used through several interfaces, including **CLI**, **Web UI** (local or hosted), and **MCP** (stdio or Streamable HTTP). The easiest way to get started is with the hosted Web UI:

https://pkgfactory.ohnolab.workers.dev/

## Templates

PkgFactory.ts currently provides [three templates](https://github.com/JuliaPackageFactory/PkgFactory.ts/tree/main/packages/pkgfactory/templates) with different levels of functionality. You can see examples automatically generated from these templates in the following repositories:

| Template     | Example                                                                         | Purpose                                                                    |
| ------------ | ------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `Minimum`    | [ExampleMinimum.jl](https://github.com/JuliaPackageFactory/ExampleMinimum.jl)   | Minimal Julia package setup                                                |
| `Simple`     | [ExampleSimple.jl](https://github.com/JuliaPackageFactory/ExampleSimple.jl)     | Standard package setup with documentation and CI                           |
| `All-in-One` | [ExampleAllInOne.jl](https://github.com/JuliaPackageFactory/ExampleAllInOne.jl) | Full-featured package setup with development and quality-assurance tooling |

## Development History

This project started as [@ohno](https://github.com/ohno)'s repository, but has undergone several major specification changes:

| Period | Development Approach and Architecture |
|---|---|
| 2025-10-30 – 2026-08-03 | Developed PkgStarter.jl primarily using Jupyter Notebook and Cursor. Established package templates and GitHub Actions workflows, and prototyped GitHub API integration and authentication using GitHub OAuth Apps. Renamed the project to PkgFactory.jl on 2026-02-28. |
| 2026-08-04 – 2026-09-24 | Expanded AI-assisted development with Codex. Implemented a web UI, introduced end-to-end (E2E) tests, and developed PkgFactoryMCP.jl as a standalone package on 2026-09-07. |
| 2026-09-25 – 2026-09-28 | Integrated PkgFactoryMCP.jl into the main repository. Adopted a shared core library with separate applications for the CLI, web UI (local and hosted), and MCP server (local and hosted). Introduced hosting on Cloudflare Containers. |
| 2026-09-29 – Present | Moved primary development to PkgFactory.ts. Adopted Cloudflare Workers for hosting, added Jev-powered recommendations, and launched the service in production. |

## Feedback

Please share your feedback in [GitHub Discussions](https://github.com/JuliaPackageFactory/PkgFactory.ts/discussions). If you've used PkgFactory.jl to create a package, I'd love to see it—please share a link there as well.
