# Angular Project Structure Styleguide

## Purpose

This style guide serves as the defacto standard for structuring your new angularjs frontend application at WCA. The project structure is inspired by another fantastic guide that the rest of our angularjs codebase is based upon: [John Papa - Angular 1 Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md).

The purpose of this style guide is to provide guidance on building Angular pplications by showing the conventions we as a team at WCA use and more importantly why we chose them.

## Table of Contents

1. [Directory Structure](#directory-structure)
1. [Naming Conventions](#naming-conventions)
1. [References](#references)

## Directory Structure

### TODO

- [ ] discuss location of sass files
- [ ] change this to a component based structure instead similar to the treefort application

```
.
├── app
│   ├── app.js
│   ├── common
│   │   ├── controllers
│   │   ├── directives
│   │   ├── filters
│   │   └── services
│   ├── home
│   │   ├── home.module.js
│   │   ├── home.routes.js
│   │   ├── controllers
│   │   │   ├── first.controller.js
│   │   │   └── second.controler.js
│   │   ├── directives
│   │   │   └── functionality-1
│   │   │   	├── functionality-1.directive.js
│   │   │   	└── functionality-1.tpl.js
│   │   ├── filters
│   │   │   ├── bar.filter.js
│   │   │   └── foo.filter.js
│   │   └── services
│   │       ├── model.service.js
│   │       └── helper.service.js
│   └── about
│       ├── about.module.js
│       ├── about.routes.js
│       ├── controllers
│       │   └── third.controller.js
│       ├── directives
│       │   ├── functionalty-2.directive.js
│       │   └── functionality-3.directive..js
│       ├── filters
│       │   └── localize.filter.js
│       └── services
│           └── helper.service.js
├── lib
└── test
```

### Why

## Naming Conventions

### Directories 

Name directories using `kebab-case` syntax.

#### Why

### Files

Name files using `kebab-case` syntax. Add a file type descriptor at the end of the file name that describes what type of Angular construct it is.

```
// bad

// good
```

#### Why

Because it makes it easier to write patterns for build tools such as gulp.

## References

1. https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md
1. https://github.com/gianarb/awesome-angularjs
1. https://github.com/mgechev/angularjs-style-guide#directory-structure
