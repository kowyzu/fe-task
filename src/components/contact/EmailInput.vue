<template>
  <div class="mt-2 mb-4">
    <input name="email" :id="id" type="email"
      :class="['form-control', 'form-email', 'animate__animated', { 'form-error-input': error }, { 'animate__headShake': error }]"
      :placeholder="placeholder" :value="modelValue" aria-label="e-mail" @input="updateValue" @change="validate">
    <div v-if="error" class="form-error-msg animate__animated animate__fadeIn">
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

    validateEmail() {
      let email = this.modelValue;
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return emailRegex.test(email);
    },

    validate() {
      if (!this.modelValue.trim()) {
        this.error = 'Please enter your email.';
        this.$emit('error', this.error);
        return false;
      }
      if (!this.validateEmail()) {
        this.error = 'Invalid email address. Please enter an email in the format: example@domain.cz';
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