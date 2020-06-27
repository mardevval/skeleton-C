# skeleton-C

Just an empty skeleton for a C project

This file should be written in Markdown

Generally speaking, it should only explain what the software does and show usage examples.


# Directory structure:


## bin
The final compiled user executable, library (.so), or module (.ko) is put here

## build
A special directory that should not be considered part of the source of the project. Used for storing ephemeral build results, must not be checked into source control (use ignore option). This folder contains all object files, and the content is removed on a clean.

## config
In case the application requires it, here you find spoecific configuration files for compile-time (not to be confused with the app's own config file, e.g., in /etc/appname).

## data
Directory containing non-source code aspects of the project. This might include graphics, data sets and markup files.

## doc
Documentation (e.g. html, latex etc.)

## external
The external/ directory is reserved for embedding of external projects. Each embedded project should occupy a single subdirectory of external/. external/ should not contain files other than those required by tooling. This directory may be automatically populated, either partially or completely, by tools (eg. git submodules) as part of a build process. In this case, projects must declare the auto-populated subdirectories as ignored by relevant source control systems. Subdirectories of external/ should not be modified as part of regular project development. Subdirectories should remain as close to their upstream source as possible.

## extra
The extras/ directory is designated for containing additional submodules for the project which build upon the main component(s). This may include submodules that are not part of the project’s "default" build, or otherwise impose special requirements to be used. For example, the following might be candidates for extra/ rather than regular components:
 - Language bindings" or extra libraries that provide integrations of the project with programming languages or runtimes different from its own.
 - Platform bindings" or extra libraries (plugins) that integrate the project with a particular platform. For example, a windowing library that needs to understand how to talk with Windows, Quartz, X11, and Wayland would include its platform integration implementations in this directory.
 - Contributed" submodules. Additional submodules that are contributed by the project’s users and included in upstream, but are not officially supported by the project.
 - Optional submodules that require additional dependencies, or may be prohibitive to include for all users. For example, Qt’s Webkit module is prohibitively time consuming to build, and it requires the presence of dependencies that are only required exactly for that one component.

## include
Directory for all the public .h header files. These are basically APIs, so they are only here in this directory if they are relevant for the end user. If they contain function prototypes used only internally by the application they should not go here but rather somewhere inside /src. May be present or not. Also, may be omitted for projects that do not distinguish between private/public headers.

## lib
Put submodules here. A submodule is basically a nested project, with its own /src and /include directories etc (but build and compile scripts, if present, will not be used). In theory could be linked to another git project.

## src
Main compilable source location. In the presence of include/, also contains private headers.

## test
Test suites that should be run during a `make test`.

## tool
The tools/ directory is designated for holding extra scripts and tools related to developing and contributing to the project. For example, turn-key build scripts, linting scripts, code-generation scripts, test scripts, or other tools that may be useful to a project develop. The contents of this directory should not be relevant to a project consumer.





