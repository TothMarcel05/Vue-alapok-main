<script setup>
    import {ref} from 'vue'

    import InputField from './components/InputField.vue';
    import MainNavigation from './components/MainNavigation.vue';
    import SiteFooter from './components/SiteFooter.vue';
    import SideContent from './components/SideContent.vue';

    // function logMessage (name)  {
    //     console.log("Input field changed!: ", name)
    // }

    function submitForm ()  {
        console.log("Form submitted!", formData)
        console.log("Form submitted!", JSON.stringify(formData))
    }


    const formData = reactive({
        email: '',
        firstname: '',
        lastname: ''
    })

</script>

<template> 
    <header>
        <MainNavigation :title="title"/>
        <!-- <MainNavigation /> -->
    </header>
    <main>
        <!-- email input -->
        <SideContent />
        <InputField 
        id="e-mail"
        type="email"
        placeholder="Enter your e-mail"
        label="E-mail address"
        @on-input="logMessage"/>

        <!-- firstname input -->
        <InputField
        id="firstname"
        type="text"
        placeholder="Enter your first name"
        label="First Name"
        @on-input="logMessage"/>

        <!-- lastname input -->
        <InputField
        id="lastname"
        type="text"
        placeholder="Enter your last name"
        label="Last Name"
        @on-input="logMessage"/>

        <button @click="submitForm">Submit</button>
    </main>
    <footer>
        <SiteFooter />
    </footer>
</template>

<style scoped>

</style>