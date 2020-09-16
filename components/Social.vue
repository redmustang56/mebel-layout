<template>
    <div class="socials">
        <a href="#" class="socials__l" aria-label="facebook">
            <svg-icon class="i-icon i-icon--fb" :class="isMiniSvg ? 'i-icon--fbm' : ''" name="fb"></svg-icon>
        </a>
        <a href="#" class="socials__l"  aria-label="facebook">
            <svg-icon class="i-icon i-icon--tw" :class="isMiniSvg ? 'i-icon--twm' : ''" name="twitter"></svg-icon>
        </a>
        <a href="#" class="socials__l" aria-label="facebook">
            <svg-icon class="i-icon i-icon--ld" :class="isMiniSvg ? 'i-icon--ldm' : ''" name="linked"></svg-icon>
        </a>
        <a href="#" class="socials__l" aria-label="facebook">
            <svg-icon class="i-icon i-icon--gg" :class="isMiniSvg ? 'i-icon--ggm' : ''" name="google"></svg-icon>
        </a>
    </div>
</template>

<script>
    export default {
        name: "Social",
        props: {
            isMiniSvg: {
                type: Boolean,
                default: false
            }
        }
    }
</script>

<style lang="postcss" scoped>
    .socials {
        display: flex;
        align-items: flex-end;
        &__l {
            .i-icon   {
                color: var(--bluelight);
                margin: 0 6px;
                &:last-child {
                    margin-right: 0;
                }
                &--fb {
                    width: 10px;
                    height: 22px;
                }
                &--fbm {
                    width: 6px;
                    height: 13px;
                    color: var(--red);
                }
                &--tw {
                    width: 26px;
                    height: 21px;
                }
                &--twm {
                    width: 13px;
                    height: 10px;
                    color: var(--red);
                }
                &--ld {
                    width: 24px;
                    height: 23px;
                }
                &--ldm {
                    width: 13px;
                    height: 12px;
                    color: var(--red);
                }
                &--gg {
                    width: 19px;
                    height: 19px;
                }
                &--ggm {
                    width: 14px;
                    height: 13px;
                    color: var(--red);
                }
            }
        }
    }
</style>