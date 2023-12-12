<template>
  <div class="ems-tab loginboxbg mxw-400 tab-them d-block p-5 p-lg-7 ml-0 ml-lg-7 position-relative ems-tab-activeted">
    <q-tabs v-model="activeTab" align="left" class="mb-4 mb-lg-7">
      <q-tab name="login" label="ÜYE OL" />
    </q-tabs>
      <q-tab-panel name="signup">
        <div class="ems-signup tab-pane selected" rel="tab-2" id="pills-uyeol" role="tabpanel" aria-labelledby="pills-uyeol-tab" tabindex="0">
          <div class="signup-form-container">
            <form id="signup" action="/tr/CreateMember" class="ems-form row g-3 needs-validation response-form-inline ems-form" method="POST" novalidate>
              <!-- Ad Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label for="Name" class="fs-13 fw-500 font-fira color-dark mb-1 required"><span style="color: red;">*</span>Ad</label>
                <input class="form-control" id="Name" type="text" name="Name" value="" required="true">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Soyad Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label class="fs-13 fw-500 font-fira color-dark mb-1 required" for="Surname"><span style="color: red;">*</span>Soyad</label>
                <input class="form-control" id="Surname" type="text" name="Surname" required="true" value="">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- E-posta Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label class="fs-13 fw-500 font-fira color-dark mb-1 required" for="Email"><span style="color: red;">*</span>E-posta</label>
                <input class="form-control" id="Email" type="mail" name="Email" value="" required="true">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Şifre Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label class="fs-13 fw-500 font-fira color-dark mb-1 required" for="Password"><span style="color: red;">*</span>Şifre</label>
                <input class="form-control" id="Password" type="password" tabindex="3" name="Password" required="true" autocomplete="off">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Şifre Tekrar Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label class="fs-13 fw-500 font-fira color-dark mb-0 required" for="Password"><span style="color: red;">*</span>ŞİFRE TEKRAR</label>
                <input class="form-control" id="Password" type="password" tabindex="3" name="Password Again" required="true" autocomplete="off">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Cinsiyet Select -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0 label-anim">
                <label class="form-label fs-13 fw-500 font-fira color-dark mb-1" for="Gender">Cinsiyet</label>
                <select class="form-select form-control" id="Gender" name="Gender">
                  <option value="">Seçiniz</option>
                  <option value="1">Erkek</option>
                  <option value="2">Kadın</option>
                </select>
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Cep Telefonu Input -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-1 mt-0">
                <label class="fs-13 fw-500 font-fira color-dark mb-1 required" for="MobilePhone"><span style="color: red;">*</span>Cep Telefonu</label>
                <input class="form-control custom-phone-masker" name="MobilePhone" id="MobilePhone" type="tel" value="" required="true">
                <div class="ems-field-feedback position-relative"></div>
              </div>

              <!-- Remaining form fields -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-2 mt-2">
                <div class="form-check ">
                    <label class="fs-13 fw-400 font-fira color-dark mb-1 required" for="MembershipAgreement"><span style="color: red;">*</span> Üyelik Sözleşmesini okudum, onaylıyorum. <a data-title="Üyelik Sözleşmesi" class="text-underline gray-txt lgn-txt" data-sourcetype="json" onclick="customModal.onShowModal(this);" href="#" data-key="MembershipAgreement" data-type="ajx" data-uri="/tr/Api/Version/1.0/MemberApi/GetMembershipAgreement"><strong>Sözleşme metni için tıklayınız</strong></a></label>
                    <input class="form-check-input bg-white border border-dark rounded-0 fs-15" id="MembershipAgreement" type="checkbox" name="MembershipAgreement" value="true">
                    <div class="ems-field-feedback position-relative"></div>
                </div>
            </div>

            <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-2 mt-2">
                <div class="form-check ">
                    <label class="fs-13 fw-400 font-fira color-dark mb-1 required" for="MembershipAgreement">E-posta ve SMS yoluyla reklam, promosyon, kampanya vb. amaçlarla tarafıma ticari elektronik ileti gönderilmesini kabul ediyorum.</label>
                    <input class="form-check-input bg-white border border-dark rounded-0 fs-15" id="MembershipAgreement" type="checkbox" name="MembershipAgreement" value="true">
                    <div class="ems-field-feedback position-relative"></div>
                </div>
            </div>

            <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-2 mt-2">
                <div class="form-check ">
                    <label class="fs-13 fw-400 font-fira color-dark mb-1 required" for="MembershipAgreement"> Açık Rıza Metni kapsamında, kişisel verilerimin işlenmesine ve paylaşılmasına onay veriyorum. </label>
                    <input class="form-check-input bg-white border border-dark rounded-0 fs-15" id="MembershipAgreement" type="checkbox" name="MembershipAgreement" value="true">
                    <div class="ems-field-feedback position-relative"></div>
                </div>
            </div>
              <!-- Üye Ol Button -->
              <div class="col-12 col-lg-12 ems-field mb-2 mb-lg-2 mt-2">
                <button type="submit" class="btn btn-dark them-btn w-100">ÜYE OL</button>
              </div>
            </form>
          </div>
        </div>
      </q-tab-panel>
  
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const activeTab = ref('login');

</script>

<style scoped>

@import 'src/css/style.css';
</style>
