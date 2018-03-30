<template>
<div>
    <table class="table table-condensed table-striped table-hover">

    <colgroup>
        <col width="60px">
        <col>
        <col width="30px">
        <col width="30px">
    </colgroup>

    <thead>
        <tr>

        <th class="clickable" title="Click to sort">#</th>

        <th class="clickable" title="Click to sort">Description</th>

        <th class="clickable" title="Click to sort">Complete</th>

        <th>Remove</th>

        </tr>
    </thead>

    <tbody>
        <tr v-for="todoItem in todoItems" :key="todoItem.id">

            <td>
                <span class="badge">{{todoItem.id}}</span>
            </td>

            <td>
                {{todoItem.description}}
            </td>

            <td class="text-center">
                <span class="clickable fa" v-bind:class="{ 'fa-calendar-check-o': todoItem.isComplete,  'fa-calendar-o': !todoItem.isComplete }"
                    ></span>
            </td>

            <td class="text-center">
                <span class="clickable fa fa-trash" ></span>
            </td>
            
        </tr>
    </tbody>

    </table>
</div>  
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TodoItem from "@/components/TodoItem.vue";
let nextTodoId = 1;

@Component({
  components: {
    TodoItem
  },
  data() {
    return {
      todoItems: [
        {
          id: nextTodoId++,
          description: "Learn Vue",
          isComplete: false
        },
        {
          id: nextTodoId++,
          description: "Learn about single-file components",
          isComplete: false
        },
        {
          id: nextTodoId++,
          description: "Fall in love",
          isComplete: false
        }
      ]
    };
  }
})
export default class TodoList extends Vue {}
</script>
