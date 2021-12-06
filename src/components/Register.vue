<template>
   <div class="register">
      <div class="h-screen grid grid-cols-1 sm:grid-cols-3">
         <div
            class="w-4/5 col-span-2 container pl-16 md:pl-20 mt-4 custom-right-p"
         >
            <div class="my-12">
               <router-link to="./">
                  <img src="../img/Logo.svg" alt="" />
               </router-link>
            </div>
            <h1 class="inline-block">Créez votre compte gratuit</h1>
            <div class="hidden sm:block bg-gray-300 h-1 w-4/5 my-2"></div>
            <p>
               Vous avez déja un compte ?
               <a href="./" class="link">S'identifier</a>
            </p>
            <h4 class="font-bold my-4">Sélectionnez le type de compte</h4>
            <div class="flex flex-col md:flex-row">
               <div class="my-6 mr-6">
                  <input
                     type="radio"
                     name="typeCompte"
                     id="particulier"
                     hidden
                  />
                  <label
                     :class="registerType == 'particulier' ? 'checked' : ''"
                     @click="changeRegisterType('particulier')"
                     class="labelRadio"
                     for="particulier"
                     >particulier</label
                  >
               </div>
               <div class="my-6 mr-6">
                  <input
                     type="radio"
                     name="typeCompte"
                     id="professionnel"
                     hidden
                  />
                  <label
                     @click="changeRegisterType('professionnel')"
                     :class="registerType == 'professionnel' ? 'checked' : ''"
                     class="labelRadio"
                     for="professionnel"
                     >professionnel</label
                  >
               </div>
            </div>
            <h4 class="font-bold my-4">Informations générales</h4>

            <!--------------------- Particulier Form --------------------->

            <div v-if="registerType == 'particulier'">
               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-row justify-center my-14">
                  <button class="btn">S'incrire</button>
               </div>
            </div>

            <!--------------------- Professionnel Form --------------------->

            <div v-if="registerType == 'professionnel'">
               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input"
                        type="text"
                        placeholder="email"
                        name="email"
                     />
                     <i
                        class="fas fa-at text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-col md:flex-row mb-4">
                  <div class="w-full relative mr-4 mb-3">
                     <input
                        class="form-input focus:outline-none"
                        type="text"
                        placeholder="Nom Complet"
                        name="nomComplet"
                     />
                     <i
                        class="fas fa-user text-blue-500 absolute inset-y-0 right-4 flex items-center"
                     ></i>
                  </div>
               </div>

               <div class="flex flex-row justify-center my-14">
                  <button class="btn">S'incrire</button>
               </div>
            </div>
         </div>

         <div class="">
            <img src="../img/registerBG.jpg" alt="" class="register-bg" />
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "Register",
   data() {
      return {
         registerType: "particulier",
      };
   },
   methods: {
      changeRegisterType(x) {
         this.registerType = x;
      },
   },
};
</script>
