Learn Vue, one of the most popular and approachable JavaScript frameworks! Get hands-on experience building with flexible components using directives, props, lifecycle hooks, and slots. You’ll use Vue Router for routing and Pinia for state management. By the end of the course, you will have the skills and knowledge to create a Vue project from start to finish, deploy it to production, and explore the Vue ecosystem on your own.
_Published: January 4, 2023_

Course Repo - https://github.com/bencodezen/complete-intro-to-vue-3-workshop

## Table of Contents

## 1. Introduction

### Introduction

_00:00:00 - 00:04:37_
Ben Hong introduces the course by providing some personal background, discussing who this workshop is for, and the course prerequisites. Course resources and an overview of the workshop format are also covered in this segment.

## 2. Overview

### Vue Overview

_00:04:38 - 00:14:15_
Ben discusses an overview of what Vue is and why to consider using Vue, including Vue being approachable, performant, versatile, community-first, and enterprise proven. A brief demonstration of some applications that use Vue is also included in this segment.

### Creating a Vue App

_00:14:16 - 00:20:51_
Ben briefly discusses prerequisite knowledge for creating a Vue app and walks through how to create a base Vue application without using any build tools. Vue is being used directly from a CDN by placing a script tag into the HTML and can be configured via a defined configuration object.

### Directives

_00:20:52 - 00:32:32_
Ben demonstrates using unique attributes with the v- prefix called directives, including `v-if`, `v-else`, and `v-for`, to reactively apply updates to the DOM when the value of its expression changes. Student questions regarding differences between Vue 2 and Vue 3, why the `v-for` directive is on the `li` element instead of the `ul` element, and if the data attribute is required are also covered in this segment.

### Getting Started with Vue Exercise

_00:32:33 - 00:40:19_
Students are instructed to choose a TV show and use their newly gained knowledge of directives to create an HTML page, reactive data for characters on the show, and render an empty state if no characters exist. Ben then walks through a possible solution to the exercise, including a new syntax for returning data.

### Getting Started Q&A

_00:40:20 - 00:48:38_
Ben answers student questions regarding if the if...else statement can be extended, if there are any gotchas with namespacing the characterList, and if characterList is globally available. How to render the characterList as a string instead of a list is also covered in this segment.

### Event Handling & View Model

_00:48:39 - 01:01:58_
Ben demonstrates handling events in Vue, defining methods, and using the `v-on` and `v-bind` directives to call those methods to add interactivity to the page. The `v-model` directive can be used in place of `v-on` and `v-bind` to create a two-way binding.

### Event Handling Q&A

_01:01:59 - 01:09:47_
Ben answers student questions regarding tracking the increment amount, passing arguments to methods, and the difference between `@click` and `v-on click`

### Event Handling Exercise

_01:09:48 - 01:17:41_
Students are instructed to add a favorite button to each character and render the favorited characters in a separate list. Ben then walks through a possible solution to the event handling exercise, including the bonus challenge.

## 3. Watchers & Computer Properties

### Watchers & Computed Properties

_01:17:42 - 01:26:16_
Ben demonstrates using the watch option to trigger a function whenever a reactive property changes. Computed properties allow the ability to declaratively compute derived values.

### Computed Properties Exercise

_01:26:17 - 01:38:39_
Students are instructed to create a statistics column for character attributes that leverages computed properties. Ben then walks through a possible solution to the computed properties exercise.

### Computed Properties vs Watchers

_01:38:40 - 01:41:31_
Ben answers a student's question regarding real-life examples of when it is better to use computed properties over watchers.

## 4. Vue Tools

### Progressive Enhancement

_01:41:32 - 01:45:29_
Ben discusses the ability to progressively enhance websites with Vue using the CDN to avoid complete code rewrites. A brief walkthrough of the process GitLab took migrating their app to Vue is also provided in this segment.

### create-vue, Dev Tools, & Volar

_01:45:30 - 02:01:57_
Ben walks through creating a new Vue application using the Vite-based scaffolding tool `create-vue`, the contents of the generated application, and briefly demonstrates the available functionality of the Vue dev tools. A student's question regarding migrating an existing project to Vite is also covered in this segment.

### Build Tools Exercise

_02:01:58 - 02:13:46_
Students are instructed to create a new project using `create-vue` named `atla-forum` and migrate `index.html` into `App.vue`. Ben then walks through a possible solution to the build tools exercise. A student's question regarding using `.vue` without using Vite is also covered in this segment.

### Custom Components

_02:13:47 - 02:22:32_
Ben demonstrates creating a custom component in Vue and scoping all of the associated JavaScript and HTML to that specific file. Components are pulled into the application by registering them in the exports under the components option.

### Custom Components Exercise

_02:22:33 - 02:31:07_
Students are instructed to practice scoping, creating, and importing custom components to `App.vue`. Ben then walks through a possible solution to the custom component exercise and briefly discusses the data flow between the application and components.

### Props

_02:31:08 - 02:38:26_
Ben walks through passing data to components by declaring props. A student's question regarding passing functions as props is also covered in this segment.

### Props Exercise and Q&A

_02:38:27 - 02:49:49_
Ben instructs students to practice implementing props for their Vue application. Student questions regarding how to approach user details when creating a user card component, if computed properties could be used to pass data, if properties are passed by reference, and will the component rerender if the data changes outside of it are also covered in this segment.

### Emitting Custom Events

_02:49:50 - 03:00:43_
Ben discusses defining and emitting custom events, defining global methods, and demonstrates the Vue dev tools timeline registering DOM events. Student questions regarding if events traveling multiple levels have to be caught and reemitted and if there is an emit equivalent in Vue 2.

### Emitting Custom Events Exercise

_03:00:44 - 03:14:40_
Students are instructed to build out components as they see fit, whether receiving data from the parent or keeping it at the top level. Ben then walks through a possible solution to the exercise and answers some student questions. Student questions covered in this segment include having the `favoriteCharacter` function in a separate module, how the data gets into the `favoritesList` variable.

### Slots for Layout

_03:14:41 - 03:30:06_
Ben demonstrates using slots to pass a template fragment to a child component and let the child component render the fragment within its template. Props and if-else conditions can be attached to slots to allow for more flexibility and reusability.

### Slots Exercise

_03:30:07 - 03:33:38_
Students are instructed to create a base layout for their application and practice implementing slots. Ben then walks through an example solution for the slots exercise

## 5. Fetching Data

### Fetching Data in Lifecycle Hooks

_03:33:39 - 03:47:43_
Ben demonstrates fetching async data in Vue and walks through a diagram of how a lifecycle hook works. A student's question regarding if the lifecycle hooks can be paused if a promise is not returned is also covered in this segment.

### Generic Component

_03:47:44 - 03:52:36_
Ben walks through the contents of the `cest-la-vue` project and introduces a "meta component" for rendering dynamic components or elements. The component to render is determined by the `is`-prop which can be an HTML tag name, a component's registered name, or bound to the definition of a component.

### Fetching Data in Lifecycle Exercise

_03:52:37 - 04:06:37_
Students are instructed to create a `UsersPage` component, leverage the created lifecycle hook to fetch a list of users from the `JSONPlaceholder` API, and render the returned list of users to the page. Ben then walks through the solution to the fetching data in lifecycle exercise.

### Generating Unique Keys on the Client

_04:06:38 - 04:09:07_
Ben answers a student's question regarding generating unique keys on the frontend by providing npm package called `uuid`. A brief pseudocode demonstration of how this package would be used is also provided in this segment.

## 6. Composition API

### Composition API

_04:09:08 - 04:22:45_
Ben discusses that composition API, when used with Vue, is vanilla JavaScript and allows custom code organization at the cost of having no default option. A brief overview of the experimental feature `Suspense` and a demonstration of rendering data from an API is also covered in this segment.

### Reactive References

_04:22:46 - 04:33:35_
Ben demonstrates how to create reactive references using the Vue helper methods, including `ref`, `computed`, and `reactive`. The differences between Composition API and Options API are also briefly discussed in this segment.

### Composition API Exercise

_04:33:36 - 04:39:51_
Students are instructed to refactor the `UsersPage` to use setup to fetch data. Ben then walks through a possible solution to the Composition API exercise.

### script setup

_04:39:52 - 04:50:29_
Ben discusses a Vue compiler option to fully buy into using composition API while saving code space. Student questions regarding if this route would result in more concise components and how stable the script setup is are also covered in this segment.

### script setup Exercise

_04:50:30 - 04:56:02_
Students are instructed to refactor the `UserPage` to use script setup, practice using `defineProps`, and practice using `defineEmits`. Ben then walks through a possible solution to the script setup exercise.

### Composables

_04:56:03 - 05:04:10_
Ben demonstrates a type of reusable JavaScript utility to share props between components called **composables** that similarly utilizes the use prefix from React. A walk-through of implementing composables in the base counter is also covered in this lesson.

### Composables Q&A

_05:04:11 - 05:15:26_
Ben answers student questions regarding how `beforeDestroy` works in Composition API, how permanent the composables are, and how an unmounted component's state is handled.

### Composables Exercise

_05:15:27 - 05:21:56_
Students are instructed to create a composables folder in the `src` directory, analyze the app to locate a shareable piece of state or functionality, and create a file called `useState.js` / `useFunction.js`. Ben then walks through a possible solution to the composables exercise.

## 7. Styling Components

### Global vs. Scoped Styles

_05:21:57 - 05:26:27_
Ben demonstrates how to define global and scoped styling in a Vue application. Scoped styles take relevant component elements and append a unique data attribute.

### CSS Modules

_05:26:28 - 05:31:38_
Ben demonstrates applying the module mode to CSS styles to allow scoping styles to components. The selected class gets recompiled with a generated hash attached to define the scope.

### v-bind in CSS

_05:31:39 - 05:36:36_
Ben discusses combining the interactivity of JavaScript and CSS styling using Vue's `v-bind`.

### Styling Components Exercise

_05:36:37 - 05:40:48_
Students are instructed to refactor styles using an external global file, practice styling with scoped CSS, and practice styling with CSS modules. Ben then walks through a possible solution to the styling components exercise.

## 8. Routing & Deployment

### Vue Router

_05:40:49 - 05:49:59_
Ben walks through setting up Vue Router, defining a set of routes, and applying those routes to the application. Each route is defined by a path and a component variable.

### History Management

_05:50:00 - 05:56:14_
Ben discusses defining how URLs should be displayed using various Vue history modes, including hash, HTML5, and memory mode. A demonstration of what happens when including Vue Router while creating a new project with `create-vue` is also provided in this segment.

### Vue Router Exercise

_05:56:15 - 06:06:23_
Students are instructed to open the Vue Router docs for reference, install and configure Vue Router, move page components into a new `src/views` directory, create a `src/router.js` file with the correct routes, and update `App.vue` to utilize the `router-link` and `router-view` components. Ben then walks through a possible solution to the Vue Router exercise.

### Programmatic Navigation

_06:06:24 - 06:11:36_
Ben demonstrates implementing programmatic navigation using `useRouter` from Vue Router to responsively navigate the user. The `router.push` and `router.replace` methods are demonstrated in this segment.

### Dynamic Route Params

_06:11:37 - 06:18:46_
Ben walks through dynamically rendering data based on the provided navigation route using the `useRoute` helper method. Student questions regarding params parent routes and nested navigation are also covered in this segment.

### Dynamic Routing Exercise

_06:18:47 - 06:28:31_
Students are instructed to use programmatic navigation on the `LoginPage` to navigate the user to a `DashboardPage` and create a dynamic route that displays each user's profile on its own page. Ben then walks through a possible solution to the dynamic routing exercise.

### State Management with Pinia

_06:28:32 - 06:38:43_
Ben discusses defining and managing a global store using the Vue store **Pinia**. Pinia provides the structure for managing an application's state through getters and actions and includes dev tools.

### State Management with Pinia Exercise

_06:38:44 - 06:50:07_
Students are instructed to install Pinia, configure Vue to use it, create a stores folder in the src directory, create an `itemTypeStore.js` in it, create a store, add some state, getters, and actions, and call things in the component. Ben then walks through a possible solution to the state management with Pinia exercise.

### VueUse Hooks & Vue Transitions

_06:50:08 - 06:53:46_
Ben discusses helpful hooks from VueUse for accessing local storage using the `useStorage` and setting color preferences with `useColorMode`. Transitions and transition components in Vue are also briefly discussed in this segment.

### Deploying Your Vue App

_06:53:47 - 07:00:18_
Ben demonstrates connecting a GitHub account and deploying a Vue application with Netlify. Netlify will keep track of the application's GitHub repository and rebuild the deployment on a repo change.

## 9. Wrapping Up

### Wrapping Up

_07:00:19 - 07:01:21_
Ben wraps up the course by providing suggestions for where to go next, including Nuxt and TypeScript. Links to Ben's social media accounts are also provided in this segment.
