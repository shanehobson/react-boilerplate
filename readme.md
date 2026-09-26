# React Boilerplate

A starter template for React and Redux apps with Google sign-in through Firebase Authentication, public and private routes, Sass styling, and a Jest test setup. It is adapted from the boilerplate in Andrew Mead's React course.

> Built in 2018. This project is not actively maintained, and its dependencies (React 15, Webpack 3, Babel 6) are outdated.

## Features

- Google login and logout through Firebase Authentication
- `PublicRoute` and `PrivateRoute` components that redirect based on auth state
- Login page, dashboard, 404 page, header with logout, and a loading screen shown while auth state resolves
- Redux store with thunk middleware and Redux DevTools support
- Sass styles organized into base and component partials
- Jest and Enzyme tests with snapshot testing for components, actions, and reducers
- Express server for production that serves the built app with client-side routing fallback

## Tech Stack

- React 15, Redux, React Redux, Redux Thunk
- React Router 4
- Firebase (Auth and Realtime Database)
- Sass
- Webpack 3, Babel 6
- Jest, Enzyme
- Express

## Getting Started

```bash
yarn install
yarn run dev-server
```

### Environment Variables

Webpack loads Firebase config from `.env.development` (or `.env.test` when `NODE_ENV=test`). Both files are git-ignored. Create them with these keys:

```
FIREBASE_API_KEY=
FIREBASE_AUTH_DOMAIN=
FIREBASE_DATABASE_URL=
FIREBASE_PROJECT_ID=
FIREBASE_STORAGE_BUCKET=
FIREBASE_MESSAGING_SENDER_ID=
```

### Scripts

| Script | Description |
| --- | --- |
| `dev-server` | Run webpack-dev-server |
| `build:dev` | Development build to `public/dist` |
| `build:prod` | Production build to `public/dist` |
| `test` | Run Jest |
| `start` | Serve `public/` with Express on `PORT` (default 3000) |
| `heroku-postbuild` | Production build on Heroku deploy |

## Project Structure

```
src/
  actions/      # Auth actions (login, logout, startLogin, startLogout)
  components/   # Pages, header, loader
  firebase/     # Firebase initialization
  reducers/     # Auth reducer
  routers/      # AppRouter, PublicRoute, PrivateRoute
  store/        # Redux store setup
  styles/       # Sass partials
  tests/        # Jest tests, snapshots, and mocks
server/         # Express production server
public/         # index.html, images, and the webpack output
```
