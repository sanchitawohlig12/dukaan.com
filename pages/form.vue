<!--template>
  <div class="container">
    <h1>About You</h1>
    <br />
    <form ref="form" style="font-size: 25px" @submit.prevent="submit">
      <v-row>
        <v-col>
          <label for="first">First Name</label>
          <input
            v-model="first"
            type="text"
            placeholder="First Name"
            required
            @keypress="isLetter($event)"
          />
        </v-col>
        <v-col>
          <label for="last">Last Name</label>
          <br />
          <input
            v-model="last"
            type="text"
            placeholder="Last Name"
            required
            @keypress="isLetter($event)"
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <label for="email">Email</label><br />
          <input v-model="email" type="email" placeholder="Email" required />
        </v-col>
        <v-col>
          <label for="phone">Phone</label>
          <br />
          <input
            v-model="phone"
            type="number"
            placeholder="Phone"
            maxlength="10"
            required
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <label for="position">Select Position</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 70%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
          >
            <option value="" selected disabled hidden>
              --Choose an option--
            </option>
            <option>Local Retailer</option>
            <option>National Retailer</option>
            <option>Global Retailer</option>
            <option>Manufacture</option>
          </select></v-col
        >
        <v-col>
          <label for="position">Annual Turnover</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 70%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
          >
            <option value="" selected>Under 12 Lakhs</option>
            <option>12-50 Lakhs</option>
            <option>N50-99 Lakhs</option>
            <option>Above 1 Crore</option>
            <option>Not for profit/NGO</option>
          </select>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <label for="first">Link to your any online page </label>
          <input type="text" placeholder="About You" />
        </v-col>
        <v-col>
          <label for="last">Available start date</label>
          <br />
          <input type="date" placeholder="Available start date" />
        </v-col>
      </v-row>
      <br />
      <br />
      <v-row>
        <v-col>
          <v-btn
            type="submit"
            value="Submit"
            depressed
            color="pink"
            rounded
            class="white--text"
            large
          >
            Send Message
          </v-btn>
        </v-col>
      </v-row>
    </form>
  </div>
</!--template>

// <script>
// export default {
//   name: 'form',

//   data() {
//     return {
//       error: [],
//       first: null,
//       last: null,
//       email: null,

//       phone: null,
//     }
//   },

//   methods: {
//     isLetter(e) {
//       const char = String.fromCharCode(e.keyCode) // Get the character
//       if (/^[A-Za-z]+$/.test(char)) return true
//       // Match with regex
//       else e.preventDefault() // If not match, don't add to input text
//     },
//     onlyNumber($event) {
//       const keyCode = $event.keyCode ? $event.keyCode : $event.which
//       if ((keyCode < 48 || keyCode > 57) && keyCode !== 46) {
//         // 46 is dot
//         $event.preventDefault()
//       }
//     },
//     Login(e) {
//       if (this.first && this.last && this.email && this.phone) {
//         console.log('successfully done')
//         alert('Thanks for contacting us...!')
//       }
//       this.error = []
//       if (!this.first) {
//         this.error.push('Please Enter First Name..!')
//       }
//       if (!this.email) {
//         this.error.push('Please Enter Email')
//       }
//       if (!this.phone) {
//         this.error.push('Please Enter Phone Number ')
//       }
//       if (!this.last) {
//         this.error.push('Please Enter Last Name')
//       }

//       console.warn('Error:' + this.error)
//       e.preventDefault()
//       this.first = ''
//       this.last = ''
//       this.email = ''

//       this.phone = ''
//     },
//   },
// }
// </script>
<style!-- scoped>
input[type='text'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='number'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='email'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='date'] {
  border: black 2px solid;
  outline-style: none;
  width: 70%;
}
label {
  font-weight: normal;
}
input[type='submit'] {
  border: black 2px solid;
  outline-style: none;
  width: 20%;
  height: 60px;
  background-color: rgb(138, 163, 238);
}
.btn {
  background-color: rgb(224, 51, 51);
  color: black;
}
</style!-->
<template>
  <div class="container">
    <h1>About You</h1>
    <v-divider
      v-if="!$vuetify.breakpoint.smAndDown"
      dark
      color="black"
      width="20%"
    ></v-divider>
    <v-divider
      v-if="$vuetify.breakpoint.smAndDown"
      dark
      color="black"
      width="50%"
    ></v-divider>
    <br />
    <br />
    <br />
    <br />
    <v-snackbar
      v-model="snackbar"
      class="snackbar"
      absolute
      light
      top
      center
      style="top: 10%"
    >
      <span style="color: green">Registration successful!</span>
      <v-icon style="color: green"> mdi-checkbox-marked-circle </v-icon>
    </v-snackbar>
    <form ref="form" style="font-size: 25px" @submit.prevent="submit">
      <v-row>
        <v-col>
          <label for="first">First Name</label>
          <input
            v-model="form.first"
            :rules="rules.name"
            type="text"
            placeholder="First Name"
            required
            @keypress="isLetter($event)"
          />
        </v-col>
        <v-col>
          <label for="last">Last Name</label>
          <br />
          <input
            v-model="form.last"
            :rules="rules.name"
            type="text"
            placeholder="Last Name"
            required
            @keypress="isLetter($event)"
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <label for="email">Email</label><br />
          <input
            v-model="form.email"
            :rules="rules.emailRules"
            type="email"
            placeholder="Email"
            required
          />
        </v-col>
        <v-col>
          <label for="phone">Phone</label>
          <br />
          <input
            v-model="form.phone"
            :rules="rules.phone"
            type="text"
            placeholder="Phone"
            maxlength="10"
            required
            @keypress="onlyNumber"
          />
        </v-col>
      </v-row>
      <v-row v-if="!$vuetify.breakpoint.smAndDown">
        <v-col cols="12" sm="6">
          <label for="position">Select Position</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 70%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
            required
          >
            <option value="" selected disabled hidden>
              --Choose an option--
            </option>
            <option>Local Retailer</option>
            <option>National Retailer</option>
            <option>Global Retailer</option>
            <option>Manufacture</option>
          </select></v-col
        >
        <v-col cols="12" sm="6">
          <label for="position">Annual Turnover</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 70%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
            required
          >
            <option value="" selected>Under 12 Lakhs</option>
            <option>12-50 Lakhs</option>
            <option>N50-99 Lakhs</option>
            <option>Above 1 Crore</option>
            <option>Not for profit/NGO</option>
          </select>
        </v-col>
      </v-row>
      <v-row v-if="$vuetify.breakpoint.smAndDown">
        <v-col cols="12" sm="6">
          <label for="position">Select Position</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 80%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
            required
          >
            <option value="" selected disabled hidden>
              --Choose an option--
            </option>
            <option>Local Retailer</option>
            <option>National Retailer</option>
            <option>Global Retailer</option>
            <option>Manufacture</option>
          </select></v-col
        >
        <v-col cols="12" sm="6">
          <label for="position">Annual Turnover</label>
          <select
            class="form-control"
            style="
              font-size: 25px;
              height: 50%;
              width: 80%;
              border: black 2px solid;
              outline-style: none;
            "
            placeholder="select"
            required
          >
            <option value="" selected>Under 12 Lakhs</option>
            <option>12-50 Lakhs</option>
            <option>N50-99 Lakhs</option>
            <option>Above 1 Crore</option>
            <option>Not for profit/NGO</option>
          </select>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <label for="first">Link to your any online page </label>
          <input type="text" placeholder="About You" required />
        </v-col>
        <v-col>
          <label for="last">Available start date</label>
          <br />
          <input type="date" placeholder="Available start date" required />
        </v-col>
      </v-row>
      <br />
      <br />
      <v-row>
        <v-col>
          <input type="submit" value="Submit" />
        </v-col>
      </v-row>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    const defaultForm = Object.freeze({
      first: '',
      last: '',
      email: '',

      phone: '',

      terms: false,
    })

    return {
      form: Object.assign({}, defaultForm),
      rules: {
        name: [(val) => (val || '').length > 0 || 'This field is required'],
        emailRules: [
          (v) => !!v || 'E-mail is required',
          (v) => /.+@.+/.test(v) || 'E-mail must be valid',
        ],
        phone: [
          (v1) => !!v1 || 'Phone number is required',
          (v1) => /\d{10}/.test(v1) || 'Please enter correct mobile number',
          (v1) =>
            (v1 && v1.length === 10) || 'Please enter correct mobile number',
        ],
      },
      snackbar: false,

      defaultForm,
    }
  },

  computed: {
    formIsValid() {
      return (
        this.form.first && this.form.last && this.form.email && this.form.phone
      )
    },
  },

  methods: {
    isLetter(e) {
      const char = String.fromCharCode(e.keyCode) // Get the character
      if (/^[A-Za-z]+$/.test(char)) return true
      // Match with regex
      else e.preventDefault() // If not match, don't add to input text
    },
    onlyNumber($event) {
      const keyCode = $event.keyCode ? $event.keyCode : $event.which
      if ((keyCode < 48 || keyCode > 57) && keyCode !== 46) {
        // 46 is dot
        $event.preventDefault()
      }
    },

    resetForm() {
      this.form = Object.assign({}, this.defaultForm)
      this.$refs.form.reset()
    },

    submit() {
      this.snackbar = true
      this.resetForm()
    },
  },
}
</script>

<style>
input[type='text'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='number'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='email'] {
  border: black 2px solid;
  outline-style: none;
}
input[type='date'] {
  border: black 2px solid;
  outline-style: none;
  width: 70%;
}
label {
  font-weight: normal;
}
input[type='submit'] {
  border: black 2px solid;
  outline-style: none;
  width: 20%;
  height: 60px;
  color: white;
  background-color: black;
}
h1 {
  font-weight: bold;
}

@media only screen and (max-width: 991px) {
  input[type='submit'] {
    border: black 2px solid;
    outline-style: none;
    width: 30%;
    height: 60px;
    color: white;
    background-color: black;
  }
  input[type='date'] {
    border: black 2px solid;
    outline-style: none;
    width: 80%;
  }
}
</style>


