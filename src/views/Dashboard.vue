<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <Navbar> </Navbar>
    <RouterView />
</template>

<script>
import Navbar from '@/components/NavBar.vue'

export default {
    components: {
        Navbar,
    },

    created() {
        const token = document.cookie.replace(/(?:(?:^|.*;\s*)hexTokem\s*=\s*([^;]*).*$)|^.*$/, "$1")
        console.log(token);
        this.$http.defaults.headers.common.Authorization = token;
        const api = `${import.meta.env.VITE_APP_API}api/user/check`
        this.$http.post(api, this.user)
            .then((res) => {
                if (!res.data.success) {
                    this.$router.push('/login')
                }

            })
    }
}
</script>