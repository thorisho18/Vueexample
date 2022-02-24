<template>
    <div class ="media">
        <p>Page width is {{ $screen.width }} px</p>
        <p>Page height is {{ $screen.height }} px</p>
        <p>Current breakpoint is {{ $screen.breakpoint }} px</p>
        <p>VueScreen</p>
    </div>
    
</template>
<script>
Vue.use(VueWindowSize);
export default {
    computed: {
        media() {
            return {
                'is-phone': this.$screen.sm,
                'is-tablet': this.$screen.md,
                'is-desktop': this.$screen.lg,
                'can-touch': this.$screen.touch,
                'breakpoint': this.$screen.breakpoint,
            };
        }
    }
}

</script>

