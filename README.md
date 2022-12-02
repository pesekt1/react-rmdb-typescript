# Movies web site in React.js (Typescript version)

Data are fetched from a public API service: https://www.themoviedb.org/

Application setup:

Make a free account at https://www.themoviedb.org/

Go to https://www.themoviedb.org/settings/api
and apply for API key.

Once you have it, use it in the .env file:

```
REACT_APP_API_KEY= ...
```

Run:.

```
npm install
npm start
```

The API provides different endpoints - we are setting the variables in config.ts:
```typescript
// Read more about the API here: https://developers.themoviedb.org/

const API_URL: string = 'https://api.themoviedb.org/3/';
const API_KEY: string | undefined = process.env.REACT_APP_API_KEY;

const SEARCH_BASE_URL: string = `${API_URL}search/movie?api_key=${API_KEY}&language=en-US&query=`;
const POPULAR_BASE_URL: string = `${API_URL}movie/popular?api_key=${API_KEY}&language=en-US`;
// For login and voting
const REQUEST_TOKEN_URL: string = `${API_URL}authentication/token/new?api_key=${API_KEY}`;
const LOGIN_URL: string = `${API_URL}authentication/token/validate_with_login?api_key=${API_KEY}`;
const SESSION_ID_URL: string = `${API_URL}authentication/session/new?api_key=${API_KEY}`;

const IMAGE_BASE_URL: string = 'http://image.tmdb.org/t/p/';
```

API Documentation: https://developers.themoviedb.org/3/getting-started/introduction


--