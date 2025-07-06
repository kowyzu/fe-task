<template>
  <div class="mt-2 mb-4">
    <textarea name="message" :id="id"
      :class="['form-control', 'form-message', 'animate__animated', { 'form-error-input': error }, { 'animate__headShake': error }]"
      :placeholder="placeholder" :value="modelValue" @input="updateValue" @change="validate" aria-label="message"
      rows="3"></textarea>
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
    validate() {
      if (!this.modelValue.trim()) {
        this.error = 'Please enter a message.';
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