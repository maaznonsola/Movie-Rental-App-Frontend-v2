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

To run this app in a local development environment:

- Check that a recent version of Node is installed.
- Clone the GitHub repo.
- Run `npm install` at the level of the `package.json` file to install dependencies.
- Run `npm start`.
- The `.env.development` file should include: `REACT_APP_API_URL=http://localhost:3900/api` to point to the [Node/Express backend deployed on local](https://github.com/maaznonsola/Movie-Rental-App-Backend).

## Local development with local, development backend Node application

### For the frontend:

- Check that a recent version of Node is installed.
- Clone the GitHub repo.
- Run `npm install` at the level of the `package.json` file to install dependencies.
- Run `npm start`.
- The `.env.development` file should include: `REACT_APP_API_URL=http://localhost:3900/api`.

### For the backend:

- Refer the [Backend Documentation](https://github.com/maaznonsola/Movie-Rental-App-Backend/blob/master/README.md).