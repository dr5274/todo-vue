<template>
<div>
    <h3>Todo Items</h3>

    <div class="row">

        <div class="col-sm-3">

            <span class="pull-left">

                <div class="input-group input-group-sm">
                    <input type="text" class="form-control" placeholder="New todo..." >
                    <span class="input-group-btn">
                        <button class="btn btn-default" type="button" >
                            <span class="fa fa-plus"></span>
                        </button>
                    </span>
                </div>

            </span>

        </div>

        <div class="col-sm-1">
            <!-- <app-loading-spinner [image]="4" [loading]="isBusy()"></app-loading-spinner> -->
        </div>

        <div class="col-sm-2">

            <span class="pull-right">
                Show completed items
                <input class="clickable" type="checkbox" />
            </span>

        </div>

    </div>

    <div class="row">

        <div class="col-sm-6">
            <TodoList />
            <!-- <app-todo-list [showCompleted]="showCompleted"></app-todo-list> -->
        </div>

    </div>
</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TodoList from "@/components/TodoList.vue";

@Component({
  components: {
    TodoList
  }
})
export default class TodoItems extends Vue {}
</script>
