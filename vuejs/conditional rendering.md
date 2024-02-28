
# Conditional rendering
[[vuejs]] has a built in functionality that can introduce conditionality in web pages using a v-if [[directive]]. This directive can be added to html tags, such that boolean values can be read from the vue.js [[javascript]] scope. If this is used in combination with a [[function]] call, this can introduce conditional rendering.

## Example
```
<script type="module">
import { createApp, ref } from 'vue'

createApp({
  setup() {
    const awesome = ref(true)

    function toggle() {
      // ...
      awesome.value = !awesome.value
    }

    return {
      awesome,
      toggle
    }
  }
}).mount('#app')
</script>

<div id="app">
  <button @click="toggle">toggle</button>
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>
</div>
```
 The example above will spawn a button that will toggle the rendering of the [[h1]] elements. The rendering is determined by the [[boolean]] `awesome` the `@click` directive triggers a `toggle()` functioncall when the event it triggered.

  because the `awesome` [[boolean]] is declared in the `setup()` scope it is callable within all of `createApp()`. That means tha tit does not have to be passed to functions to be able to edit the values.

Because the functions need to be triggerable from within [[HTML]] elements the funciton has to return itself too.

# List Redering
[[vuejs]] can also render lists. This needs to be facilitated in the [[template]] by for example have an [[unordered list]], in which we can place a `<li>` element to which w connect the v-for [[directive]]. This wil cause the `<li>` element to be created multiple times, as long as the loop iterates. This is shown in the example below. The example also shows how we can use a [[dictionary]] to dynamically add and remove `<li>` elements by interacting with the [[HTML]] elements only.

## Example
```
<script type="module">
import { createApp, ref } from 'vue'

createApp({
  setup() {
    // give each todo a unique id
    let id = 0

    const newTodo = ref('')
    const todos = ref([
      { id: id++, text: 'Learn HTML' },
      { id: id++, text: 'Learn JavaScript' },
      { id: id++, text: 'Learn Vue' }
    ])

    function addTodo() {
      todos.value.push({ id: id++, text: newTodo.value })
      newTodo.value = ''
    }

    function removeTodo(todo) {
      todos.value = todos.value.filter((t) => t !== todo)
    }

    return {
      newTodo,
      todos,
      addTodo,
      removeTodo
    }
  }
}).mount('#app')
</script>

<div id="app">
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" required placeholder="new todo">
    <button>Add Todo</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</div>
```

