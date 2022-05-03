# React Full Stack Starter-Kit

A complete boilerplate with React + NextJS SSR, GraphQL API and Relay.

## Project Structure

The top-level directly layout looks as follows:

```bash
.
├── packages/                   # Shared components (modules) managed by Lerna
├── api/                        # GraphQL API gateway
├── web/                        # NextJS website
├── lerna.json                  # Lerna configuration
└── package.json                # List of project dependencies
```

## Tech Stack

- [React][react] for building component-based UIs ([docs][reactdocs])
- [NextJS][nextjs] for building SSR websites ([docs][nextjsdocs])

## Prerequisites

- [Node.js][node] v9 or higher + [Yarn][yarn] package manager
- [Lerna][lerna] a tool for managing JavaScript projects with multiple packages
- [Docker][docker] Community Edition v17 or higher (only for the API project)
- [VS Code][code] editor (preferred) + [Project Snippets][vcsnippets],
  [EditorConfig][vceditconfig], [ESLint][vceslint], [Flow][vcflow], and [Prettier][vcprettier]
  plug-ins.

## Getting Started

**Start API**

```bash
$ cd api
$ yarn                          # Install Node.js dependencies)
$ yarn start                    # Build and launch API service
```

**Start WEB**

```bash
$ cd web
$ yarn                          # Install Node.js dependencies)
$ yarn dev                      # Build and launch WEB service
```

# Task

## Setup

## Database

- Create a new migration file using the yarn script

```bash
$ yarn db-change your-migration-name:
```

- Edit the newly created migration file to add the following 3 new columns to the properties table:

```
- land_surface (float)
- number_of_rooms (float)
- number_of_parkings (int)
```

- Run migration

```bash
$ yarn db-migrate
```

## API

- Add new fields to PropertyType and PropertyInputType
- Update the validator and the migration to make the new fields work

## WEB

- Create a form to upsert a property on this page (we recommend using Formik)
- Create a new page to display all created properties

## Bonus

- Deploy the project somewhere on the web (AWS Labmda, Google Cloud Functions, Zeit, Heroku...)

