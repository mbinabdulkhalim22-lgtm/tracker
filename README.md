 AI Tutor

← All projects
Task Tracker
Build a CLI app to track your tasks and manage your to-do list.

beginner
Programming Language
CLI
Filesystem
Details
Solutions

Started working 45 seconds ago. Follow these tips to get most out of it.
Started Working

Submit Solution
5 upvotes
10 upvotes
Task tracker is a project used to track and manage your tasks. In this task, you will build a simple command line interface (CLI) to track what you need to do, what you have done, and what you are currently working on. This project will help you practice your programming skills, including working with the filesystem, handling user inputs, and building a simple CLI application.

Requirements
The application should run from the command line, accept user actions and inputs as arguments, and store the tasks in a JSON file. The user should be able to:

Add, Update, and Delete tasks

Mark a task as in progress or done

List all tasks

List all tasks that are done

List all tasks that are not done

List all tasks that are in progress

Here are some constraints to guide the implementation:

You can use any programming language to build this project.

Use positional arguments in command line to accept user inputs.

Use a JSON file to store the tasks in the current directory.

The JSON file should be created if it does not exist.

Use the native file system module of your programming language to interact with the JSON file.

Do not use any external libraries or frameworks to build this project.

Ensure to handle errors and edge cases gracefully.

Example
The list of commands and their usage is given below:

bash

# Adding a new task
task-cli add "Buy groceries"
# Output: Task added successfully (ID: 1)
# Updating and deleting tasks
task-cli update 1 "Buy groceries and cook dinner"
task-cli delete 1
# Marking a task as in progress or done
task-cli mark-in-progress 1
task-cli mark-done 1
# Listing all tasks
task-cli list
# Listing tasks by status
task-cli list done
task-cli list todo
task-cli list in-progress
Task Properties
Each task should have the following properties:

id: A unique identifier for the task

description: A short description of the task

status: The status of the task (todo, in-progress, done)

createdAt: The date and time when the task was created

updatedAt: The date and time when the task was last updated

Make sure to add these properties to the JSON file when adding a new task and update them when updating a task.

Getting Started
Here are a few steps to help you get started with the Task Tracker CLI project:

Set Up Your Development Environment
Choose a programming language you are comfortable with (e.g., Python, JavaScript, etc.).

Ensure you have a code editor or IDE installed (e.g., VSCode, PyCharm).

Project Initialization
Create a new project directory for your Task Tracker CLI.

Initialize a version control system (e.g., Git) to manage your project.

Implementing Features
Start by creating a basic CLI structure to handle user inputs.

Implement each feature one by one, ensuring to test thoroughly before moving to the next e.g. implement adding task functionality first, listing next, then updating, marking as in progress, etc.

Testing and Debugging
Test each feature individually to ensure they work as expected. Look at the JSON file to verify that the tasks are being stored correctly.

Debug any issues that arise during development.

Finalizing the Project
Ensure all features are implemented and tested.

Clean up your code and add comments where necessary.

Write a good readme file on how to use your Task Tracker CLI.

By the end of this project, you will have developed a practical tool that can help you or others manage tasks efficiently. This project lays a solid foundation for more advanced programming projects and real-world applications.

Happy coding!

Join the Community

roadmap.sh is among the top 10 most starred projects on GitHub and is visited by hundreds of thousands of developers every month.

Top 10
 out of 28M!

373K

GitHub Stars

Star us on GitHub
Help us reach #1
+90k
every month

+3.2M

Registered Users

Register yourself
Commit to your growth
+2k
every month

52K

Discord Members

Join on Discord
Join the community
Roadmaps
Guides
FAQs
YouTube

roadmap.sh
by
@nilbuild

Community created roadmaps, best practices, projects, articles, resources and journeys to help you choose your path and grow in your career.

© roadmap.sh·Terms·Privacy·

ThewNewStack
The top DevOps resource for Kubernetes, cloud-native computing, and large-scale development and deployment.

DevOps·Kubernetes·Cloud-Native

Cookie Settings
# setup-python

[![Basic validation](https://github.com/actions/setup-python/actions/workflows/basic-validation.yml/badge.svg?branch=main)](https://github.com/actions/setup-python/actions/workflows/basic-validation.yml)
[![Validate Python e2e](https://github.com/actions/setup-python/actions/workflows/test-python.yml/badge.svg?branch=main)](https://github.com/actions/setup-python/actions/workflows/test-python.yml)
[![Validate PyPy e2e](https://github.com/actions/setup-python/actions/workflows/test-pypy.yml/badge.svg?branch=main)](https://github.com/actions/setup-python/actions/workflows/test-pypy.yml)
[![e2e-cache](https://github.com/actions/setup-python/actions/workflows/e2e-cache.yml/badge.svg?branch=main)](https://github.com/actions/setup-python/actions/workflows/e2e-cache.yml)

This action provides the following functionality for GitHub Actions users:

- Installing a version of Python or PyPy and (by default) adding it to the PATH
- Optionally caching dependencies for pip, pipenv and poetry
- Registering problem matchers for error output

## What's new in V7

- Migrated action internals to ESM for compatibility with latest `@actions/*` packages. No changes to action inputs, outputs, or behavior.

## Breaking changes in V6

- Upgraded action from node20 to node24
  > Make sure your runner is on version v2.327.1 or later to ensure compatibility with this release. See [Release Notes](https://github.com/actions/runner/releases/tag/v2.327.1)

For more details,  see the full release notes on the [releases page](https://github.com/actions/setup-python/releases/tag/v6.0.0)

## Basic usage

See [action.yml](action.yml)

**Python**
```yaml
steps:
- uses: actions/checkout@v7
- uses: actions/setup-python@v7
  with:
    python-version: '3.13' 
- run: python my_script.py
```

**PyPy**
```yaml
steps:
- uses: actions/checkout@v7
- uses: actions/setup-python@v7 
  with:
    python-version: 'pypy3.10' 
- run: python my_script.py
```

**GraalPy**
```yaml
steps:
- uses: actions/checkout@v7
- uses: actions/setup-python@v7 
  with:
    python-version: 'graalpy-24.0' 
- run: python my_script.py
```

**Free threaded Python**
```yaml
steps:
- uses: actions/checkout@v7
- uses: actions/setup-python@v7
  with:
    python-version: '3.13t'
- run: python my_script.py
```

The `python-version` input is optional. If not supplied, the action will try to resolve the version from the default `.python-version` file. If the `.python-version` file doesn't exist Python or PyPy version from the PATH will be used. The default version of Python or PyPy in PATH varies between runners and can be changed unexpectedly so we recommend always setting Python version explicitly using the `python-version` or `python-version-file` inputs.

The action will first check the local [tool cache](docs/advanced-usage.md#hosted-tool-cache) for a [semver](https://github.com/npm/node-semver#versions) match. If unable to find a specific version in the tool cache, the action will attempt to download a version of Python from [GitHub Releases](https://github.com/actions/python-versions/releases) and for PyPy from the official [PyPy's dist](https://downloads.python.org/pypy/).

For information regarding locally cached versions of Python or PyPy on GitHub hosted runners, check out [GitHub Actions Runner Images](https://github.com/actions/runner-images).

## Supported version syntax

The `python-version` input supports the [Semantic Versioning Specification](https://semver.org/) and some special version notations (e.g. `semver ranges`, `x.y-dev syntax`, etc.), for detailed examples please refer to the section: [Using python-version input](docs/advanced-usage.md#using-the-python-version-input) of the [Advanced usage](docs/advanced-usage.md) guide.

## Supported architectures

Using the `architecture` input, it is possible to specify the required Python or PyPy interpreter architecture: `x86`, `x64`, or `arm64`. If the input is not specified, the architecture defaults to the host OS architecture.

## Caching packages dependencies

The action has built-in functionality for caching and restoring dependencies. It uses [toolkit/cache](https://github.com/actions/toolkit/tree/main/packages/cache) under the hood for caching dependencies but requires less configuration settings. Supported package managers are `pip`, `pipenv` and `poetry`. The `cache` input is optional, and caching is turned off by default.

The action defaults to searching for a dependency file (`requirements.txt` or `pyproject.toml` for pip, `Pipfile.lock` for pipenv or `poetry.lock` for poetry) in the repository, and uses its hash as a part of the cache key. Input `cache-dependency-path` is used for cases when multiple dependency files are used, they are located in different subdirectories or different files for the hash that want to be used.

 - For `pip`, the action will cache the global cache directory
 - For `pipenv`, the action will cache virtualenv directory
 - For `poetry`, the action will cache virtualenv directories -- one for each poetry project found

**Caching pip dependencies:**

```yaml
steps:
- uses: actions/checkout@v7
- uses: actions/setup-python@v7
  with:
    python-version: '3.13'
    cache: 'pip' # caching pip dependencies
- run: pip install -r requirements.txt
```
>**Note:** Restored cache will not be used if the requirements.txt file is not updated for a long time and a newer version of the dependency is available which can lead to an increase in total build time.

>The requirements file format allows for specifying dependency versions using logical operators (for example chardet>=3.0.4) or specifying dependencies without any versions. In this case the pip install -r requirements.txt command will always try to install the latest available package version. To be sure that the cache will be used, please stick to a specific dependency version and update it manually if necessary.

>The `setup-python` action does not handle authentication for pip when installing packages from private repositories. For help, refer [pip’s VCS support documentation](https://pip.pypa.io/en/stable/topics/vcs-support/) or visit the [pip repository](https://github.com/pypa/pip).

See examples of using `cache` and `cache-dependency-path` for `pipenv` and `poetry` in the section: [Caching packages](docs/advanced-usage.md#caching-packages) of the [Advanced usage](docs/advanced-usage.md) guide.

## Advanced usage

- [Using the python-version input](docs/advanced-usage.md#using-the-python-version-input)
- [Using the python-version-file input](docs/advanced-usage.md#using-the-python-version-file-input)
- [Check latest version](docs/advanced-usage.md#check-latest-version)
- [Caching packages](docs/advanced-usage.md#caching-packages)
- [Outputs and environment variables](docs/advanced-usage.md#outputs-and-environment-variables)
- [Available versions of Python, PyPy and GraalPy](docs/advanced-usage.md#available-versions-of-python-pypy-and-graalpy)
- [Hosted tool cache](docs/advanced-usage.md#hosted-tool-cache) 
- [Using `setup-python` with a self-hosted runner](docs/advanced-usage.md#using-setup-python-with-a-self-hosted-runner)
- [Using `setup-python` on GHES](docs/advanced-usage.md#using-setup-python-on-ghes)
- [Allow pre-releases](docs/advanced-usage.md#allow-pre-releases)
- [Using the pip-version input](docs/advanced-usage.md#using-the-pip-version-input)

## Recommended permissions

When using the `setup-python` action in your GitHub Actions workflow, it is recommended to set the following permissions to ensure proper functionality:

```yaml
permissions:
  contents: read # access to check out code and install dependencies
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).

## Contributions

Contributions are welcome! See our [Contributor's Guide](docs/contributors.md).
