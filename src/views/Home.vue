<template>
    <TodoItems/>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TodoItems from "@/components/TodoItems.vue";

@Component({
  components: {
    TodoItems
  }
})
export default class Home extends Vue {}
</script>
