<template>
    <q-layout view="hHh Lpr lFf">
      <!-- Sol Taraf Çekme Menüsü -->
      <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered content-class="bg-grey-2">
        <q-scroll-area style="height: calc(100% - 50px);">
          <q-list link inset-delimiter>
            <q-item v-for="item in menuItems" :key="item.label">
              <q-item-section>
                <q-item-label>
                  <q-icon :name="item.icon" />
                  {{ item.label }}
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>
  
      <!-- Ana İçerik Alanı -->
      <q-page-container>
        <q-page>
          <!-- Başlık Çubuğu -->
          <q-header elevated>
            <q-toolbar>
              <q-btn
                flat
                dense
                round
                icon="menu"
                @click="leftDrawerOpen = !leftDrawerOpen"
              />
              <q-toolbar-title>Quasar Cat Menu Örneği</q-toolbar-title>
            </q-toolbar>
          </q-header>
  
          <!-- Ana İçerik -->
          <q-page-sticky position="top">
            <q-toolbar>
              <q-toolbar-title>İçerik Başlığı</q-toolbar-title>
            </q-toolbar>
          </q-page-sticky>
  
          <!-- İçerik Gövdesi -->
          <q-page padding>
            <q-card>
              <q-card-section>
                <!-- İçerik Buraya Gelecek -->
                <p>Hoş geldiniz! Buraya uygulamanızın içeriğini ekleyebilirsiniz.</p>
              </q-card-section>
            </q-card>
          </q-page>
        </q-page>
      </q-page-container>
    </q-layout>
  </template>
  
  <script lang="ts">
  export default {
    data() {
      return {
        leftDrawerOpen: false,
        menuItems: [
          { label: 'Ana Sayfa', icon: 'home' },
          { label: 'Haberler', icon: 'rss_feed' },
          { label: 'Profil', icon: 'person' },
          { label: 'Ayarlar', icon: 'settings' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Gerekirse stil ekleyebilirsiniz */
  </style>
  