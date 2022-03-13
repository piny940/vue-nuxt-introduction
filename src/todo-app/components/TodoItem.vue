<template>
  <li>{{ title }}</li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
      validator: function(value) {
        return Array.from(value).length < 10;
      },
    },
  },
};
</script>
