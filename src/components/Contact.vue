<template>
    <section>
    <div>pathanin.map@gmail.com</div>
    <div>099-242-5149</div>
    </section>
</template>

<style scoped>
section {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

section div {
    font-weight: 500;
    font-size: 2rem;
}

@media only screen and (max-width:576px) {
    section div {
        font-size: 1rem;
    }
}
</style>

<script>
export default {
    name: 'web-contact'
}
</script>