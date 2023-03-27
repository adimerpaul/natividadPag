<template>
  <q-layout view="hHh lpR fFf" class="bg-grey-3">
    <q-header reveal class="bg-white text-black">
      <q-toolbar>
        <q-toolbar-title>
          <div class="row items-center">
            <q-img src="images/logo.jpg" width="50px" />
            <q-space />
            <q-list v-if="$q.screen.gt.sm">
              <q-item>
                <q-item-section side >
                  <q-icon name="o_place" color="primary" />
                </q-item-section>
                <q-item-section>
                  <q-item-label>Dirección</q-item-label>
                  <q-item-label caption lines="2">Bolivar Nº 753, entre Arica e Iquique</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
            <q-list>
              <q-item>
                <q-item-section side >
                  <q-icon name="o_phone" color="primary" />
                </q-item-section>
                <q-item-section>
                  <q-item-label>Teléfono</q-item-label>
                  <q-item-label caption lines="2">52 54721 - 52 83667</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </div>
        </q-toolbar-title>
      </q-toolbar>
      <q-tabs align="right" class="bg-primary text-white">
        <q-route-tab label="Inicio" href="#Home" exact />
        <q-route-tab label="Nosotros" href="#About" />
        <q-route-tab label="Servicios" href="#Services" />
        <q-route-tab label="Contacto" href="#Contact" />
      </q-tabs>
    </q-header>

    <q-page-container>
      <router-view />
<!--      <div elevated reveal class="bg-amber">-->
<!--        <q-toolbar>-->
<!--          <q-toolbar-title>-->
<!--            <q-avatar>-->
<!--              <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">-->
<!--            </q-avatar>-->
<!--            <div>Title</div>-->
<!--          </q-toolbar-title>-->
<!--        </q-toolbar>-->
<!--      </div>-->
    </q-page-container>
  </q-layout>
</template>
