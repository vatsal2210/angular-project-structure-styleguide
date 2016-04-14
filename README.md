# Angular Project Structure Styleguide

## Purpose

This style guide serves as the defacto standard for structuring your new angularjs frontend application at WCA. The project structure is inspired by another fantastic guide that the rest of our angularjs codebase is based upon: [John Papa - Angular 1 Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md).

The purpose of this style guide is to provide guidance on building Angular pplications by showing the conventions we as a team at WCA use and more importantly why we chose them.

## Table of Contents

1. [Directory Structure](#directory-structure)
1. [Naming Conventions](#naming-conventions)
1. [References](#references)

## Directory Structure

We use a recurisve component based folder structure. This helps to keep the folders relatively flat and easy to navigate.  If you find yourself seeing 7+ files it may be time to start thinking about splitting out some of the functionality into a new module.  This helps to make modules small and single purpose. 

```
.
└── app
    ├── example.app.js
    ├── index.html
    ├── less
    │   └── app.less
    ├── common
    │   ├── controllers
    │   ├── directives
    │   ├── filters
    │   └── services
    ├── home
    │   ├── home.module.js
    │   ├── home.routes.js
    │   ├── first.controller.js
    │   ├── second.controler.js
    │   ├── functionality-1.directive.js
    │   ├── functionality-1.tpl.js
    │   ├── bar.filter.js
    │   ├── model.service.js
    │   ├── model.spec.js
    │   └── home.less
    └── about
        ├── about.module.js
        ├── about.routes.js
        ├── third.controller.js
        ├── functionalty-2.directive.js
        ├── functionality-3.directive.js
        ├── localize.filter.js
        ├── helper.service.js
        └── about.less

```

### Why

It helps to keep folders more flat. Files are also typically grouped closely to other files that have similar functionality.

## Naming Conventions

### Directories 

Name directories using `kebab-case` syntax.

#### Why

Because it's easy, it's case insensitive, and we name our files in a similar pattern.

### Files

Name files using a modified `kebab-case` syntax. Add a file type descriptor at the end of the file name that describes what type of Angular construct it is.

```
// bad
functionality-service.js

// good
functionality.service.js
```

#### Why

Using `kebab-case` with `.componenttype.js` makes it easier to use globstar patterns for build tools and test configurations. It also makes it easier to distinguish which file you're searching for.

## References

1. https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md
1. https://github.com/gianarb/awesome-angularjs
1. https://github.com/mgechev/angularjs-style-guide#directory-structure
