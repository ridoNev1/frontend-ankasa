<template>
  <div class="container-fluid forgot-pass">
    <div class="row">
      <div class="col-sm-6 d-none d-sm-block">
        <div class="img-left">
          <img src="../assets/img/illustrationWhite.png" />
        </div>
      </div>

      <div class="right-side col-sm-6">
        <div class="container">
          <h5 class="mt-3 mb-5">
            <img src="../assets/img/planeBlue.png" alt="logo" /> Ankasa
          </h5>
          <h3 class="mb-5">Reset Password</h3>
          <form class="text-center" @submit.prevent="resetPassword">
            <input type="password" id="password" class="form-control mb-4" placeholder="New Password" autofocus required v-model="password" />
            <input type="password" class="form-control mb-4" placeholder="Confirm New Password" autofocus required id="confirm-password" @keyup="validate" />
            <!-- <p class="text-danger" id="message"></p> -->
            <button type="submit" class="btn btn-block btn-login">Reset</button>
            <p class="small text-muted mt-3 mb-3">
              Please set a secure password that contains both uppercase and lowercase as well as number and symbols. This is for your own safety
            </p>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped src="../assets/css/style.css"></style>

<script>
import Swal from 'sweetalert2'
import { mapActions } from 'vuex'

export default {
  name: 'ForgotPass',
  data () {
    return {
      password: null,
      userkey: null
    }
  },
  methods: {
    validate () {
      const password = document.getElementById('password')
      const confirm = document.getElementById('confirm-password')
      if (password.value !== confirm.value) {
        console.log('Password Doesnt Match')
      } else {
        console.log('password match')
      }
    },
    ...mapActions({
      onResetPassword: 'auth/onResetPassword'
    }),
    resetPassword () {
      const ukey = {
        password: this.password,
        userkey: this.$route.query.userkey
      }
      this.onResetPassword(ukey).then(result => {
        window.location = '/login'
      }).catch(err => this.alertError(err))
    },
    alertError () {
      Swal.fire({
        icon: 'error',
        title: 'Oops...',
        text: 'Reset password Failed, Something went wrong!'
      })
    }
  }
}
</script>
