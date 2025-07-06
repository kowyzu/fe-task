<template>
  <div class="contact-form container text-start d-flex flex-column justify-content-center mb-5 mb-md-0 py-5">
    <form novalidate @submit.prevent="handleFormSubmit()">
      <div class="row justify-content-center">
        <div class="row justify-content-center">
          <div class="col-11">
            <div class="row row-cols-xl-2 row-cols-1">
              <div class="col-xl-7 col pt-3 pt-xl-0 px-0">
                <span class="label label-form text-uppercase">Your name</span>
                <NameInput ref="nameInput" id="firstName" placeholder="First name" v-model.trim="name" />
              </div>
              <div class="col-xl-4  px-0">
                <span class="label label-form text-uppercase">Budget</span>
                <select class="form-select mt-2 mb-4" aria-label="select budget">
                  <option selected>$500</option>
                  <option value="1">$600</option>
                  <option value="2">$700</option>
                  <option value="3">$800</option>
                </select>
              </div>
            </div>
          </div>
        </div>
        <div class="row justify-content-center">
          <div class="col-11 px-0">
            <span class="label label-form text-uppercase">Input field</span>
            <EmailInput ref="emailInput" id="email" placeholder="name@mail.com" v-model.trim="email" />
          </div>
        </div>
        <div class="row justify-content-center">
          <div class="col-11 px-0">
            <span class="label label-form text-uppercase">Your message</span>
            <MessageTextArea ref="messageTextArea" id="message" placeholder="Message" v-model.trim="message" />
          </div>
        </div>
        <div class="row justify-content-evenly">
          <div class="col-11">
            <div class="row gx-5">
              <div class="col-md-7 col align-content-center">
                <div class="form-check">
                  <input class="form-check-input" type="checkbox" value="yes" id="checkChecked" checked>
                  <label class="form-check-label" for="checkChecked">
                    <p class="form-check-text">Send me a copy</p>
                  </label>
                </div>
              </div>
              <div class="col-md-4 col pb-3 pb-md-0">
                <button type="submit" class="btn-action btn-middle m-0">Send</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import NameInput from './NameInput.vue';
import EmailInput from './EmailInput.vue';
import MessageTextArea from './MessageTextArea.vue';

export default {
  components: {
    NameInput,
    EmailInput,
    MessageTextArea,
  },
  data() {
    return {
      name: '',
      email: '',
      message: '',
      error: null,
      success: null,
      statusMessage: '',
    }
  },
  methods: {
    // Validate form inputs via specific validation methods from form conponents
    isFormValid() {

      let isNameValid = this.$refs.nameInput.validate();
      let isEmailValid = this.$refs.emailInput.validate();
      let isMessageValid = this.$refs.messageTextArea.validate();

      if (!isNameValid || !isMessageValid || !isEmailValid) {
        this.error = true;
        return false;
      }

      this.error = null;
      return true;
    },


    // After form submitting validate data, prepare object with filled data and post to index.php
    handleFormSubmit() {
      if (!this.isFormValid()) {
        return;
      }
      else { this.cleanForm() }
    },

    // Clean input values in form
    cleanForm() {
      this.name = '';
      this.email = '';
      this.message = '';
      this.error = null;
    }
  }
}
</script>