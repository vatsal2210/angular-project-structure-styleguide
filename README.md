# Angular Project Structure Styleguide

## Purpose

This style guide serves as the defacto standard for structuring your new angularjs frontend application at WCA. The project structure is inspired by another fantastic guide that the rest of our angularjs codebase is based upon: [John Papa - Angular 1 Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md).

The purpose of this style guide is to provide guidance on building Angular applications by showing the conventions we as a team at WCA use and more importantly why we chose them.

## Table of Contents

1. [Directory Structure](#directory-structure)
1. [Naming Conventions](#naming-conventions)
1. [References](#references)

## Directory Structure

We use a recurisve component based folder structure. This helps to keep the folders relatively flat and easy to navigate.  If you find yourself seeing 7+ files it may be time to start thinking about splitting out some of the functionality into a new module.  This helps to make modules small and single purpose. 

```
.
└── example
    ├── example.app.js
    ├── index.html
    ├── less
    │   └── example.less
    └── app
        ├── common
        │   ├── components
        │   ├── filters
        │   └── services
        └── components
            ├── home
            │   ├── home.module.js
            │   ├── home.routes.js
            │   ├── first.controller.js
            │   ├── second.controller.js
            │   ├── functionality-1.directive.js
            │   ├── functionality-1.tpl.html
            │   ├── bar.filter.js
            │   ├── model.service.js
            │   ├── model.spec.js
            │   └── home.less
            └── about
                ├── about.module.js
                ├── about.routes.js
                ├── third.controller.js
                ├── functionality-2.directive.js
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

### Angular Constructs

Declare Modules, Controllers, Directives, Filters, and Factories with the following naming conventions. Notice Services aren't mentioned because we are using Factories (yes they are a service too) instead as per the John Papa style guide.

Element | Naming style | Example | usage
----|------|----|--------
Modules | 'wca.' + lowerCamelCase  | wca.angularApp |
Controllers | Functionality + 'Controller'  | AdminController|
Components | wcaLowerCamelCase  | wcaFooter | as elements
Directives | wcaLowerCamelCase  | wcaListModal | as attributes
Filters | lowerCamelCase | userFilter |
Factories | lowerCamelCase | dataFactory | others

#### Why

Sometimes it's better to pick one way than to do something in a team setting.

See [this post](https://gist.github.com/toddmotto/5b4de6c777d3e446e6410fdadb824522) for more information on the distinction between components and directives in Angular 1.5

## References

1. https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md
1. https://github.com/gianarb/awesome-angularjs
1. https://github.com/mgechev/angularjs-style-guide#directory-structure
1. https://gist.github.com/toddmotto/5b4de6c777d3e446e6410fdadb824522
