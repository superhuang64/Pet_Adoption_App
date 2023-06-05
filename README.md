# Adopt Animals APP

### Controlled form

REACT form elements and state
form/select/input/option
attributes
interact with states
set submit

useEffects
provide a way to handle performing side effects in what are otherwise pure React components

1. component

- pure function- props as input,same input return same output- predictable, reliable, and easy to test

2. side effects

- reach outside of React components
- separated from the rendering process
- common side effects:(unpredictable)
  - Making a request to an API for data from a backend server(make a request to an async data source)
  - To interact with browser APIs (to use document or window directly)
  - Use unpredictable timing functions like setTimeout or setInterval

3. value in the outer scope

- include that within the dependencies array

4. dependency array

custom hook
use localStorage to persist a user’s form input in the browser storage using React Hooks.
localStorage gives us access to a browser’s Storage object.
decide when should extract a component

- reusable, testable, too big, more organized, easy to read
- balance of component decomposition
  decide the location of requestdata function
- scope: whether reusable
  use status(good for testing)

What we want to achieve:

- when page load(useEffect)
  - get an initial set of pets
- when input animal(custom hook)(combination of hooks)
  - get the breed list
- when submit(event handler)
  - get the queried pets, list in the website
  - user interactions in JavaScript using event handlers
  - virtual DOM

props

- pass props to child component(as attribute key)
- read props in child component(as argument)
- related javascript syntax: spread, deconstruct

# localstorage?????????????????????????

[query cache](https://www.youtube.com/watch?v=2TX8ojaSwF0)

## React Router

[React router doc](https://reactrouter.com/en/main/start/tutorial)

- package: "react-router-dom"
  - { BrowserRouter, Routes, Route }
  - { Link }
  - { useParams }
    make second page, switch page

Link- page link
change `<a href>` to `<Link to={}`
more quick, not reload whole page

```
<Link to={`/details/${id}`} className="pet">
...
</Link>
```

make each result as a link to a details page

useParams
get params from React Router

header: return back to the home page

## React query

[Tanstack reacy-query](https://tanstack.com/query/latest/docs/react/overview)

- library:@tanstack/react-query
  QueryClientProvider- queryClient
  cache most of what you fetch from a database
  fetching data from the server.
  an be cached and we can avoid calling the server again if we have same parameters.
  wrap the app with the provider
  wrap app in a query client
  make request to api(split out- testable and reusable)

mutation

minimise effects, make it smallest and testable

context

keep that in cache
no refetch
