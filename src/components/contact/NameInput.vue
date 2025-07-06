<template>
  <div class="mt-2 mb-4">
    <input name="firstName" :id="id" type="text"
      :class="['form-control', 'form-first-name', 'animate__animated', { 'form-error-input': error }, { 'animate__headShake': error }]"
      aria-label="First name" :placeholder="placeholder" :value="modelValue" @input="updateValue" @change="validate">
    <div v-if="error" class="form-error-msg ps-2 animate__animated animate__fadeIn">
      {{ error }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    placeholder: String,
    modelValue: String,
  },
  data() {
    return {
      error: null,
    };
  },
  methods: {
    updateValue(event) {
      this.$emit('update:modelValue', event.target.value);
    },
    validate() {
      if (!this.modelValue.trim()) {
        this.error = 'Please enter your name.';
        this.$emit('error', this.error);
        return false;
      }
      this.error = null;
      this.$emit('error', null);
      return true;
    },
  },
};
</script>