<template>
  <div class="register">
    <register />
  </div>
</template>

<script>
// @ is an alias to /src
import register from "@/components/register.vue";

export default {
  name: "registerVue",
  components: {
    register
  }
};
</script>
