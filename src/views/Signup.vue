<template>
  <div class="SignupImage">
    <b-container>
      <div class="pt-5">
        <b-card class="m-auto" style="max-width: 25rem">
          <h1>Sign Up</h1>
          <b-form class="mx-auto" style="max-width: 30rem">
            <b-input-group class="mt-4">
              <b-form-input
                name="name"
                placeholder="Name"
                type="text"
              ></b-form-input>
            </b-input-group>

            <b-input-group class="mt-3">
              <b-form-input
                placeholder="Email address"
                type="email"
              ></b-form-input>
            </b-input-group>

            <b-input-group class="mt-3">
              <b-form-input
                id="password-input"
                autocomplete="on"
                placeholder="Password"
                type="password"
              ></b-form-input>
            </b-input-group>

            <b-input-group class="mt-3">
              <b-form-input
                placeholder="Home Address"
                type="text"
              ></b-form-input>
            </b-input-group>

            <b-input-group class="mt-3">
              <b-form-input
                placeholder="Telephone Number"
                type="number"
              ></b-form-input>
            </b-input-group>

            <b-dropdown text="Areas Interested" block class="mt-3">
              <b-form-group>
                <b-form-checkbox-group
                  id="checkbox-group-1"
                  :options="options"
                  name="flavour-1"
                  stacked
                ></b-form-checkbox-group>
              </b-form-group>
            </b-dropdown>

            <b-button variant="primary" class="mt-3">Sign up</b-button>
          </b-form>
        </b-card>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Signup",

  data() {
    return {
      dismissSecs: 10,
      dismissCountDown: 0,
      showDismissibleAlert: false,
      form: {
        name: "",
        email: "",
        password: "",
        homeAddress: "",
        telephoneNumber: "",
        status: "",
        selected: [],
      },
      options: [
        { text: "Basketball", value: "BasletBall" },
        { text: "Badminton", value: "Badminton" },
        { text: "Football", value: "Football" },
        { text: "Cricket", value: "Cricket" },
        { text: "Handball", value: "Handball" },
        { text: "Volleyball", value: "Vollyball" },
        { text: "Table Tennis", value: "Table tennis" },
        { text: "Skateboarding", value: "Skateboarding" },
      ],
    };
  },
  methods: {},
};
</script>

<style>
.SignupImage {
  background-image: url("https://i.pinimg.com/originals/08/ed/3a/08ed3a37713c50fe0eeeb4b78dd00096.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
  background-position: center;
}
</style>