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
    </tbody>

    </table>
</div>  
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {}
})
export default class TodoList extends Vue {}
</script>
