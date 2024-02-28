# Why computed properties are useful
Generally speaking we want to reduce the amount of logic in a [[template]]. The reason for this is that templates offer limited possibilities for logic. It is a better practice to pass computed properties to the template and do all of the computation and logic in [[javascript]].

The nifty thing about [[computed properties]], as opposed to just some datatype that's being passed, is that:
- computed properties are automatically unwrapped (no `#.value` required )
- computed properties will be computed without the necessity of a function call.
	- Other data would only be updated if a function is being called that determines the required output.
	- computed data will update is its dependencies are changed, without explicitly needing to call the logic that determines the computed value.
	- In practice this means that computed properties do not require an in-template event trigger.

# Example
Let's say we have an array of lists as below.

``` 
const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})
```
If we want to list the publised works of this author we could use something like:
```
<p>Has published books:</p>
<span>{{ author.books.length > 0 ? 'Yes' : 'No' }}</span>
```
This includes the logic in-template. This can make the function of the template more obvious to the reader, but limits the functionality of it. For example this means the list will only update is the page is being refreshed. Instead we could use a computed property, which will dynamically update the template if the dependencies are changed:
```
<script setup>
import { reactive, computed } from 'vue'

const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})

// a computed ref
const publishedBooksMessage = computed(() => {
  return author.books.length > 0 ? 'Yes' : 'No'
})
</script>

<template>
  <p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>
</template>
```
