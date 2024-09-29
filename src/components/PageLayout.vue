<script setup>
    import defineProps from 'vue';
    defineProps(['name', 'age']);
</script>

<template>
    <div class="PageLayout">

        <header>
            <slot name="header"></slot>
        </header>


        <default>
            <slot></slot>
        </default>


        <footer>
            <slot name="footer"></slot>
        </footer>

    </div>
</template>



<style>
header{
    text-align: center;
}
</style>