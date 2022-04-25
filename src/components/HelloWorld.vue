<script setup>
import BaseModal from "./BaseModal.vue"
defineProps({
  msg: {
    type: String,
    required: true
  }
});

</script>

<template>
    <button @click="showMessage = !showMessage">Toggle Message</button>
    <button @click="showModal = true">Show Modal</button>
    <Teleport to="body">
      <BaseModal v-if="showModal" :disabled="true">
        <h1>Hi Vue</h1>
        <button @click = "showModal = false">Close Modal</button>
      </BaseModal>
    </Teleport>
    
    <Teleport to="#purple-box">
      <p v-if="showMessage">Hello from HelloWorld</p>
    </Teleport>
    

</template>

<script>
  export default {
  components:{BaseModal},
  data() {
    return {
      showMessage: true,
      showModal: false
    }
  },
}
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
