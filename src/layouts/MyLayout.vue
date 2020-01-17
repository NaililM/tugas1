<template>
  <q-layout view="lHh Lpr lFf">
    <q-header >
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        />

      </q-toolbar>
      <div class="q-px-lg q-pt-xl q-mb-md">
       <div class="text-h3">Tabungan Siswa App</div>
        <div class="text-subtitle">Sunday 5 January</div>
      </div>
    </q-header>

    <q-footer >
         <q-tabs
      >
        <q-tab name="mails" icon="mail" label="Mails" />
        <q-tab name="alarms" icon="alarm" label="Alarms" />
        <q-tab name="smartphone" icon="smartphone" label="Smartphone" />
      </q-tabs>
    </q-footer>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-2"
    >
      <q-list>
        <q-item-label header>MI Roudlotul Mustarsyidin</q-item-label>

        <q-item
        to="Home"
        exact
         clickable >
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Home</q-item-label>
          </q-item-section>
        </q-item>
        <q-item
        to="Siswa"
         clickable >
          <q-item-section avatar>
            <q-icon name="people_outline" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Siswa</q-item-label>
          </q-item-section>
        </q-item>
        <q-item
        to="Tabungan"
         clickable >
          <q-item-section avatar>
            <q-icon name="menu_book" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Tabungan</q-item-label>
          </q-item-section>
        </q-item>
        <q-item
        to="settings"
         clickable >
          <q-item-section avatar>
            <q-icon name="settings" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Settings</q-item-label>
          </q-item-section>
        </q-item>
             </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MyLayout',

  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
