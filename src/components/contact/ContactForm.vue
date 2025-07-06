<template>
  <div class="contact-form container text-start d-flex flex-column justify-content-center mb-5 mb-md-0">
    <div class="row justify-content-center">
      <div class="row justify-content-between">
        <div class="col-11">
          <div class="row row-cols-md-2 row-cols-1">
            <div class="col-md-7 col pt-3 pt-md-0">
              <span class="label label-form text-uppercase">Your name</span>
              <input name="firstName" id="firstName" type="text" class="form-control form-first-name mt-2 mb-4"
                placeholder="First name" aria-label="First name">
            </div>
            <div class="col-md-4 col">
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
          <input name="email" id="email" type="text" class="form-control form-email mt-2 mb-4"
            placeholder="name@mail.com" aria-label="e-mail">
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-11 px-0">
          <span class="label label-form text-uppercase">Your message</span>
          <textarea name="message" id="message" class="form-control form-message p-3 mt-2 mb-4" placeholder="Message"
            aria-label="message" rows="3"></textarea>
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
              <button class="btn-action btn-middle m-0">Send</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>