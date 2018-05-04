<template>
  <div class="columns is-centered">
    <div class="column is-one-third is-mobile">
      <sign-in/>
    </div>
  </div>
</template>

<script>
import SignIn from '~/components/SignIn.vue'

export default {
  components: {
    SignIn
  }
}
</script>
