<template>
    <div>
        <app-landing-page></app-landing-page>
        <v-spacer></v-spacer>
        <app-footer></app-footer>    
    </div>
</template>


<script>

import AppFooter from './AppFooter'
import AppLandingPage from './AppLandingPage.vue'


export default {
    components : {
        AppFooter,
        AppLandingPage
    }
    
}
</script>