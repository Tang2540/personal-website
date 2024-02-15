<template>
    <div>
        <div>DevLab 3</div>
        <div id="dev-lab"></div>
    </div>

    <div>
        <div>Technical Assistant in 88 INNOVBIZ 2022</div>
        <div id="innobiz"></div>
    </div>
</template>

<style scoped>
    #dev-lab,#innobiz {
        width: 35rem;
        height: 35rem;
        background-size: contain;
        background-repeat: no-repeat;
    }

    #dev-lab {
        background-image: url('@/assets/certificate.png');
    }

    #innobiz {
        background-image: url('@/assets/innovbiz.jpg');
    }

    @media only screen and (max-width:576px) {
        #dev-lab,#innobiz {
            width: 15rem;
            height: 20rem;
        }
    }

</style>

<script>
export default {
  name: 'web-certs'
}
</script>