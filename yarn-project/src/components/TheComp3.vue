<template>
  <div class="ems-tab loginboxbg mxw-400 tab-them d-block p-5 p-lg-7 ml-0 ml-lg-7 position-relative ems-tab-activeted">
    <q-tabs v-model="activeTab" align="left" class="mb-4 mb-lg-7">
      <q-tab name="login" label="GİRİŞ YAP" />
    </q-tabs>

    <q-tab-panels v-model="activeTab">
      <q-tab-panel name="login">
        <div class="ems-signin" rel="tab-1" id="pills-giris" role="tabpanel" aria-labelledby="pills-giris-tab" tabindex="0">
          <div class="login-form-container">
            <form id="login" action="/tr/LogOn" class="ems-form row g-3 needs-validation" method="POST">
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
  <label for="UserNameOrEmail" class="fs-13 fw-500 font-fira color-dark mb-1 required" required="true" style="outline: none;"><span style="color: red;">*</span>E-posta </label>
</div>
<div class="col-12 col-lg-12 ems-field mb-1 mb-lg-1 mt-0">
  <input name="UserNameOrEmail" type="text" id="UserNameOrEmail" value="" maxlength="50"  required="true" attribute="mail" autocomplete="email" class="form-control">
  <div class="ems-field-feedback position-relative"></div>
</div>


<div class="col-12 col-lg-12 ems-field mb-1 mb-lg-1 mt-0">
  <label for="Password" class="fs-13 fw-500 font-fira color-dark mb-1 required" required="true"><span style="color: red;">*</span>Şifre</label>
</div>
<div class="col-12 col-lg-12 ems-field mb-1 mb-lg-1 mt-0">
  <input name="Password" id="Password" type="password" tabindex="2" required="true" autocomplete="off" class="form-control">
  <div class="ems-field-feedback position-relative"></div>
</div>

              <div class="ems-field col-6 col-lg-6 mb-2 mb-lg-2 mt-0 py-3">
                <div class="form-check">
                  <input type="checkbox" class="form-check-input bg-white border border-dark rounded-0 fs-15" id="RememberMe" name="RememberMe" value="true">
                  <label for="RememberMe" class="form-check-label fs-15 fw-400 font-fira color-dark lh-1 mt-1 m-0 p-0">Beni hatırla</label>
                  <div class="ems-field-feedback position-relative"></div>
                </div>
              </div>
              <div class="col-6 col-lg-6 ems-field mb-2 mb-lg-2 mt-0 py-4 text-end">
                <a href="/sifremi-unuttum" title="Şifremi Unuttum" class="text-black-50 fw-400 font-fira">Şifremi Unuttum</a>
              </div>
              <div class="ems-field">
              </div>
              <div class="col-12 col-lg-12 ems-field mb-0 mt-0">
                <q-btn type="submit" class="btn btn-dark them-btn w-100">Giriş Yap</q-btn>
              </div>
              <div class="col-12 col-lg-12 ems-field mb-0 mt-1"><p class="mb-50"><br></p>
</div>
              <div class="mx-auto justify-content-center text-center">
                <p class="mb-50">veya</p>
              </div>
              <div class="col-12 col-lg-12 ems-field mb-0 mt-1"><p class="mb-50"><br></p>
</div>
<div class="d-flex mx-auto justify-content-center">
  <q-btn @click="loginWithFacebook" class="them-btn color-dark border border-gray border-opacity-50 px-5 px-lg-7 d-flex align-items-center justify-content-center" title="Facebook" style="font-weight: bold;">FACEBOOK İLE BAĞLAN</q-btn>
</div>
              <div class="col-12 col-lg-12 ems-field mb-0 mt-6">
                <q-btn to="/uyeliksiz-alisveris" class="btn btn-dark them-btn w-100">ÜYE OLMADAN DEVAM ET</q-btn>
              </div>
              <input name="__RequestVerificationToken" type="hidden" value="">
              <input id="returnUrl" name="returnUrl" type="hidden" value="/tr/Widget/Get/LoginRaw">
            </form>
          </div>
        </div>
      </q-tab-panel>
    </q-tab-panels>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const activeTab = ref('login');
const props = defineProps(['loginWithFacebook']);
</script>

<style scoped>
/* Add your custom styles here */
@import 'src/css/style.css';
</style>
