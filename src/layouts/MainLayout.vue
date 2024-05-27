<template>
    <q-layout view="lHr lpR lfr">
        <q-header class="bg-primary text-white" height-hint="98">
            <q-toolbar>
                <q-toolbar-title> ElizzaFlower </q-toolbar-title>
                <q-tabs align="left">
                    <q-route-tab to="/" label="Home" />
                    <q-route-tab to="/Product" label="Product" />
                    <q-route-tab to="/Contact" label="Contact" />
                </q-tabs>
            </q-toolbar>
        </q-header>
        <q-page-container>
            <router-view />
        </q-page-container>

        <q-footer class="bg-primary text-white" height-hint="98">
            <q-toolbar>
                <q-toolbar-title>
                    Copyright © ElizzaFlower®. All rights reserved.
                </q-toolbar-title>
            </q-toolbar>
        </q-footer>
    </q-layout>
</template>

<style>
.q-toolbar {
  padding: 0 75px !important;
}
.q-toolbar__title:first-child {
  padding-left: 32px !important;
}
.q-tab {
  padding: 0 20px !important;
  min-height: 75px !important;
}
</style>

