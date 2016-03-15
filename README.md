# angular-project-structure-styleguide

## Purpose

This style guide serves as the defacto standard for structuring your new angularjs frontend application at WCA. The project structure is inspired by another fantastic guide that the rest of our angularjs codebase is based upon: [John Papa - Angular 1 Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md).

The purpose of this style guide is to provide guidance on building Angular pplications by showing the conventions we as a team at WCA use and more importantly why we chose them.

## Table of Contents

1. [Directory Structure](##directory-structure)


## Directory Structure

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
│   │   ├── controllers
│   │   │   ├── FirstCtrl.js
│   │   │   └── SecondCtrl.js
│   │   ├── directives
│   │   │   └── directive1.js
│   │   ├── filters
│   │   │   ├── filter1.js
│   │   │   └── filter2.js
│   │   └── services
│   │       ├── service1.js
│   │       └── service2.js
│   └── about
│       ├── controllers
│       │   └── ThirdCtrl.js
│       ├── directives
│       │   ├── directive2.js
│       │   └── directive3.js
│       ├── filters
│       │   └── filter3.js
│       └── services
│           └── service3.js
├── partials
├── lib
└── test
```
