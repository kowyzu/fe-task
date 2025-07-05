<template>
  <li :id="id" :class="class">
    <span v-if="isChecked" class="check-icon"></span>
    <p :class="isChecked ? '' : 'ps-4'">{{ text }}</p>
  </li>
</template>

<script>
export default {
  props: {
    id: String,
    class: String,
    isChecked: Boolean,
    text: String,
  }
}
</script>