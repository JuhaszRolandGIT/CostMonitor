<script setup>
import { ref } from 'vue';

      const name = ref('John')
      const status = ref('Active')
      const tasks = ref(['One', 'Two', 'Three'])

      const toggleStatus = () => {
        if(status.value === 'active'){
        status.value = 'pending';

      } else if(this.status.value === 'pending'){
        status.value = 'inactive'

      } else{
        status.value = 'active'
        }
}
</script>

<template>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else="status === 'pending'">User is inactive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <button @click="toggleStatus">Change Status</button>
</template>