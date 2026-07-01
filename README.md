# Purpose of this Repo

The purpose if this repo is to serve as a staging area for generating the dependencies for the [Renderer Engine](https://github.com/JeanPhilippeKernel/RendererEngine.git) Project. 

Previously, The CI builds for the Renderer Engine project would build up all the dependencies on each run.

This repo serves the purpose of creating a CI build that will compile and package the dependencies "once" or only oon version changes to the required repos.

The main project will get its vendored packages from this repos output.

As github has provides runners from the platforms required by the Renderer Engine project, This projects CI will build all the required packages avail them to the main project.
