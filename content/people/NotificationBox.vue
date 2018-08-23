<template>
  <div class="column box notification has-text-centered" v-html="text">
  </div>
</template>

<script>

export default {
  name: 'notification-box',
  data() {
    return {
    };
  },
  props: [
    'text',
  ],
  methods: {
  },
};

</script>
