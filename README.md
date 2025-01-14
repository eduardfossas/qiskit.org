<p align="center">
  <a href="https://qiskit.org/">
    <img alt="Qiskit" src="https://qiskit.org/images/qiskit-logo.png" width="70" />
  </a>
</p>

<h1 align="center">
  Welcome to <a href="https://qiskit.org">Qiskit.org</a>
</h1>
<p align="center">
Qiskit is an open-source quantum computing software development framework for leveraging today's quantum processors in research, education, and business.
</p>
<p align="center">
  <a href="https://github.com/Qiskit/qiskit.org/blob/main/LICENSE.txt">
    <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="Qiskit.org is released under the Apache 2.0 License." />
  </a>
  <a href="https://github.com/Qiskit/qiskit.org/actions">
    <img src="https://github.com/Qiskit/qiskit.org/workflows/build%20and%20deploy/badge.svg?branch=main" alt="Current GitHub Action build status." />
  </a>
  <a href="https://github.com/Qiskit/qiskit.org/blob/main/CONTRIBUTING.rst">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome!" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=qiskit">
    <img src="https://img.shields.io/twitter/follow/qiskit.svg?label=Follow%20@qiskit" alt="Follow @qiskit" />
  </a>
</p>

<h3 align="center">
  <a href="https://qiskit.org/">Home page</a>
  <span> · </span>
  <a href="https://qiskit.org/events/">Events</a>  
  <span> · </span>
  <a href="https://qiskit.org/advocates/">Advocates</a>
  <span> · </span>
  <a href="https://qiskit.org/documentation/">Documentation</a>
</h3>

<br/>

## Table of Contents

- [Table of Contents](#table-of-contents)
- [🚀 Get Up and Running](#-get-up-and-running)
- [💻 Technology Used](#-technology-used)
- [🏭 Content Generation](#-content-generation)
  - [🥸 Mocking content](#-mocking-content)
- [🏷️ Naming Conventions](#️-naming-conventions)
  - [Nuxt Components](#nuxt-components)
- [✏️ How to Contribute](#️-how-to-contribute)
- [🗓 Open backlog](#-open-backlog)
- [👩‍💻 Maintainers](#-maintainers)
- [🔗 Connect with Qiskit](#-connect-with-qiskit)

<br/>

## 🚀 Get Up and Running

1. **Download this repository and go to its folder**

   ```shell
   git clone git@github.com:Qiskit/qiskit.org.git && cd qiskit.org
   ```

2. **Install dependencies**

   ```shell
    npm install
   ```

3. **Create an .env file**

```shell
cp .env.example .env
```

4. **Run a local server with hot reload at [localhost:3000](localhost:3000)**

   ```shell
   npm run dev
   ```

<br/>

## 💻 Technology Used

Qiskit.org is a static website generated using [Nuxt](https://nuxt.com/).

We create and run tests using [Vitest](https://vitest.dev/), avoid syntax errors using [ESLint](https://eslint.org/) and [Stylelint](https://stylelint.io/), and automate code integration and deployment using [GitHub Actions](https://github.com/features/actions).

<br/>

## 🏭 Content Generation

Qiskit.org integrates with the tools used by the IBM Quantum Community Team to generate content based on 3rd party APIs such as Airtable. Part of this content is prefetched during building time.

During local development, mock data is generated by default but fetching real data from Airtable is possible. If you need to do this, please ask a core maintainer for the `AIRTABLE_ACCESS_TOKEN`, or [generate your own](https://airtable.com/developers/web/guides/personal-access-tokens) if you have an Airtable account with access to the required bases. Once you have the Airtable access token, change these environment variables in your `.env` file:

- `AIRTABLE_ACCESS_TOKEN=<Airtable access token>`
- `GENERATE_CONTENT=true`
- `MOCK_CONTENT=false`

Then you can run the local server as usual and the content will be fetched at the beginning:

```shell
npm run dev
```

#### 🥸 Mocking content

If you don't have access to the Airtable data or you don't need to fetch it, mock data can be generated by setting the environment variable `MOCK_CONTENT` to `true` in your `.env` file. This is set by default after you generate your `.env` file from `.env.example`.

The project has a default mocked content under the `hooks/mock/content` folder. If you want your own custom mocked content, you can create a new folder and set it as your mocked content folder using the environment variable `MOCK_BASE_PATH` which should be an absolute path of your system.

<br/>

## 🏷️ Naming Conventions

### Nuxt Components

When working with files in the `components/` directory, please adhere to the following naming conventions:

- Component files and directories should be named using PascalCase.
- Always use multi-word names.
- Simplify component names where possible, for example, `EventsItemCard` can be named `EventsCard`.
- Group related components in folders when more than one component refers to the same concept.
- When naming the component `.vue` files, include the whole path to make it easier to locate the components.
- Generic components that can be reused across multiple pages should be placed in the `components/Ui/` directory.
- Components specific to a page should be placed in their respective directory, such as `components/Events/` for events-specific components.
- Avoid appending "Section" to component names, as it is usually implied that the component represents a section of the page.

<br/>

## ✏️ How to Contribute

Contributions are always welcomed, no matter how large or small. Before contributing, please read the [contributing guide](CONTRIBUTING.md) and [code of conduct](CODE_OF_CONDUCT.md).

<br/>

## 🗓 Open backlog

We actively maintain our backlog using [GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects). You can view our backlog [here](https://github.com/orgs/Qiskit/projects/10).

<br/>

## 👩‍💻 Maintainers

<table>
<tr>
<td align="center"><a href="https://github.com/eddybrando"><img src="https://avatars2.githubusercontent.com/u/22047320?s=460&u=58f460132271f2ea45d270841f3821eb46c4bb5e&v=4" width="120px;" alt="Eddybrando Vásquez"/><br /><sub><b>Eddybrando Vásquez</b></sub></a><br /><a href="https://github.com/qiskit/qiskit.org/issues?q=author%3Aeddybrando" title="Bug reports">🐛</a><a href="https://github.com/qiskit/qiskit.org/commits?author=eddybrando" title="Code">💻</a><a href="https://join.slack.com/t/qiskit/shared_invite/enQtODQ2NTIyOTgwMTQ3LTI0NzM2NzkzZjJhNDgzZjY5MTQzNDY3MGNiZGQzNTNkZTE4Nzg1MjMwMmFjY2UwZTgyNDlmYWQwYmZjMjE1ZTM" title="Answering Questions on Slack">💬</a></td>
<td align="center"><a href="https://github.com/techtolentino"><img src="https://avatars2.githubusercontent.com/u/6276074?s=460&v=4" width="120px;" alt="Randy Tolentino"/><br /><sub><b>Randy Tolentino</b></sub></a><br /><a href="https://github.com/qiskit/qiskit.org/issues?q=author%3Atechtolentino" title="Bug reports">🐛</a><a href="https://github.com/qiskit/qiskit.org/commits?author=techtolentino" title="Code">💻</a><a href="https://join.slack.com/t/qiskit/shared_invite/enQtODQ2NTIyOTgwMTQ3LTI0NzM2NzkzZjJhNDgzZjY5MTQzNDY3MGNiZGQzNTNkZTE4Nzg1MjMwMmFjY2UwZTgyNDlmYWQwYmZjMjE1ZTM" title="Answering Questions on Slack">💬</a></td>
</tr>
</table>

<br/>

## 🔗 Connect with Qiskit

- [Twitter](https://twitter.com/qiskit)
- [Medium](https://medium.com/Qiskit)
- [YouTube](https://www.youtube.com/Qiskit)
- [Slack](https://qisk.it/join-slack)
