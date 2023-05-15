<template>

<div>

    <button class="btn">
        Shop Now
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
        </svg>
        
    </button>
</div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.btn{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 145px;
    column-gap: 10px;
    padding: 15px 0;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.06em;
    line-height: 15px;
    transition: 0.5s;
    &:hover{
        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.272);
    }

    svg{
        width: 30px;


    }
}

</style>