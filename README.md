# Movie Rental App Frontend v2

This frontend app is based on [Vidly (Movie Rental App) v1](https://github.com/maaznonsola/vidly), though this version has many distinctions.

Some key changes to this version include:

- Updates to current versions of all libraries and dependencies.
- Use of function components rather than class components for stateful components.
- Use of React context API to manage user info for authenticated and authorized UI state logic.
- Substantial refactor of table pagination logic (filter data, sort data, page of data).
- Customer page with view all, search, create, update, and delete operations.
- Rentals page with view all, search, create, and return operations.

The focus in this application was to:

- Use modern JavaScript features and libraries
- Use contemporary React features and best practices to build the UI
- Establish a maintainable, clean code base
- Create a useful layer of abstraction for common UI components
- Keep learning practices as close to real-world development work as possible

This version of the application does not focus on or include:

- Mobile first design, responsive design for mobile

The [backend Node/Express application](https://github.com/maaznonsola/Movie-Rental-App-Backend) can also be viewed on GitHub.

# Project Dependencies

## Frontend Libraries

### 1. [react](https://reactjs.org/) & [react-dom](https://reactjs.org/docs/react-dom.html)

The fundamental libraries for building user interfaces with a component-based architecture. **React** focuses on rendering UI, while **React-DOM** handles DOM-specific rendering.

---

### 2. [react-router-dom](https://reactrouter.com/)

A library for managing routing in React applications. It enables smooth navigation between pages, dynamic routes, and browser history handling.

---

### 3. [bootstrap-css-only](https://getbootstrap.com/)

Provides the core CSS for Bootstrap without JavaScript components. Ideal for lightweight projects where only styling is required.

---

### 4. [react-toastify](https://fkhadra.github.io/react-toastify/)

A library for displaying customizable toast notifications in React applications.

---

## Form Validation

### 5. [joi-browser](https://github.com/jeffbski/joi-browser) & [joi-password-complexity](https://www.npmjs.com/package/joi-password-complexity)

**Joi-browser** enables schema-based validation in the browser, while **joi-password-complexity** extends validation for secure password policies.

---

## Utilities

### 6. [axios](https://axios-http.com/)

A promise-based HTTP client for the browser and Node.js. It simplifies making API requests and handling responses.

---

### 7. [lodash](https://lodash.com/)

A utility library for simplifying common tasks such as working with arrays, objects, and strings.

---

### 8. [prop-types](https://www.npmjs.com/package/prop-types)

A runtime type-checking library for React props, ensuring components receive the correct data types.

---

## Authentication and Security

### 9. [jwt-decode](https://github.com/auth0/jwt-decode)

A small library that helps decode JSON Web Tokens (JWT) without verifying the signature. Useful for extracting token information on the client side.

---

## Monitoring and Error Tracking

### 10. [@sentry/react](https://www.npmjs.com/package/@sentry/react) & [@sentry/tracing](https://www.npmjs.com/package/@sentry/tracing)

**@sentry/react** is used for error monitoring in React applications, while **@sentry/tracing** adds performance monitoring capabilities.

---

## Application Context Overview

The mock context for this application was a movie rental shop.

Two distinct user groups would be using the website.

1. Employees wanting to assist customers in renting and returning movies.

2. Managers wanting to manage inventory and customer profiles.

## Context to Concept Mapping Auth And Admin

The app meets an early set of necessary functionality. Based on the assumption that future features would likely be added, the following conceptual points would be useful for developers:

1. Regular employees can register as users and sign in to gain authenticated status.

2. Managers must have both registered / logged in auth status and further authorization status. This change gets made when someone with database access adds `isAdmin: true` to the employee's user document.

## Key Features By Auth & Admin Status

This frontend application reflects the following levels of access, which are enforced by the Node/Express backend application.

### 1. No Auth & No Admin status

A site visitor who has not registered / logged in can:

- See genres
- See movies
- Register as a user
- Login as a user

### 2. Auth & No Admin status

A logged in user who is not admin can also:

- Logout and return to not logged in UI state
- See all customers
- See all rentals
- Search rentals
- Create new rentals
- Check in rentals

### 3. Auth & Admin status

A logged in user who is an admin can:

- Add / update genres
- Add / update / delete movies
- Add / update / delete customers

## Local development

### For the frontend:

To run this app in a local development environment:

- Check that a recent version of Node is installed.
- Clone the [GitHub repo](https://github.com/maaznonsola/Movie-Rental-App-Frontend-v2).
- Run `npm install` at the level of the `package.json` file to install dependencies.
- Run `npm start`.
- The `.env.development` file should include: `REACT_APP_API_URL=http://localhost:3900/api` to point to the [Node/Express backend deployed on local](https://github.com/maaznonsola/Movie-Rental-App-Backend).

### For the backend:

- Refer the [Backend Documentation](https://github.com/maaznonsola/Movie-Rental-App-Backend/blob/master/README.md).
