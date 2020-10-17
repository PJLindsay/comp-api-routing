# oapi-to-capi

Udemy Vue3 course Section 19 #297

example of how to refactor from Options API (Vue2) to Composition API (Vue3)
with respect to routing / params

## Problems

REQUIREMENTS:
Add new product - want to be redirected to all products
When you click - view details, want to see details

OLD WAY (Options API)
this.$router
this.$route

NEW WAY (Composition API)

a few approaches:
1) pass params as a prop (on the routes) and inject products into project details (using props param of setup())

2) use route without this.$route:
  - add hooks / composables

```
import { useRoute } from 'vue-router'
...
setup() {
  ...
  const route = useRoute()
  products.value.find(product => product.id === route.params.pid)
```

```
import { useRouter } from 'vue-router'; // add hooks / composables
...
setup() {
  ...
  const router = useRouter()
  router.push('/products');
}
```

  composables are special functions built for Composition API (to be used in setup())

## Installation

npm install


## Run

npm run serve (Development)

