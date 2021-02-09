<template>
  <div class="home pa-2">
    <list-tasks v-if="$store.state.tasks.length" />
    <no-tasks v-else />
    <button-done-sorting v-if="$store.state.sorting" />
  </div>
</template>

<script>
import ButtonDoneSorting from '../components/Todo/ButtonDoneSorting.vue';
import ListTasks from "../components/Todo/ListTasks.vue";
import NoTasks from '../components/Todo/NoTasks.vue';
export default {
  name: "Home",
  components: {
    "list-tasks": require("@/components/Todo/ListTasks.vue").default,
    "no-tasks": require("@/components/Todo/NoTasks.vue").default,
    "button-done-sorting": require("@/components/Todo/ButtonDoneSorting.vue").default

  },
};
</script>


