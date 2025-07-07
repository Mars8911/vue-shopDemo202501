
<template>
<h1>測試</h1>

</template>

<script>
export default {
    created(){
       console.log(import.meta.env.VITE_APP_API, import.meta.env.VITE_APP_PATH);
    }
}
</script>
