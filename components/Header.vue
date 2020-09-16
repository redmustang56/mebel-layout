<template>
    <section>
        <header class="h">
            <div class="h__lf"  v-scroll-reveal="{ origin: 'left', duration: 1000, distance: '25rem', delay: 300 }">
                <img class="h__logo"
                     src="~/assets/img/logo.png"
                     srcset="~/assets/img/logo.png 1x,
                        ~/assets/img/logo-2x.png 2x"
                     alt=""
                >
                <p>ASSOCIATES <br> STUDIO <br> DESIGN</p>
                <Social class="h__social" />
            </div>
            <div class="h__rh" v-scroll-reveal="{ origin: 'right', duration: 1000, distance: '25rem', delay: 300 }">
                <p class="h__address">90802 California<br> Long beach<br> PO Box 68789<br> 300 East Ocean<br> Boulevard</p>
                <p class="h__contacts">
                    <a class="h__tel" href="tel:+6493456758">+64 9 345 6758</a>
                    <br>
                    <a class="h__mail" href="mailto:info@dsgn-studio.com">info@dsgn-studio.com</a>
                </p>
            </div>
        </header>
        <Menu />
    </section>
</template>

<script>
    import Social from '~/components/Social'
    import Menu from '~/components/Menu'

    export default {
        name: "Header",
        data: () => ({
            bgImage: require("~/assets/img/image1.png"),
            isOpenMenu: false
        }),
        components: {
            Social,
            Menu
        },
        methods: {

        }
    }
</script>
<!--<style lang="scss">-->
<!--    /*-->
<!--    @mixin dynamicText($minSizePercent, $maxSize, $minSize, $minWidthPx, $maxWidth, $minWidth) {-->
<!--        font-size: calc(#{$minSizePercent} + (#{$maxSize} - #{$minSize}) * (100vw - #{$minWidthPx}) / (#{$maxWidth} - #{$minWidth}));-->
<!--    }-->
<!--    .h__address, .h__contacts, .h__lf p {-->
<!--        @media (min-width: 1500px) {-->
<!--            @include dynamicText(112.5%, 36, 18, 1500px, 3000, 1500);-->
<!--        }-->
<!--    }-->
<!--    */-->
<!--</style>-->
<style lang="postcss" scoped>
    .h {
        display: grid;
        grid-template-columns: repeat(16, 1fr);
        @media (max-width: 560px) {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr;
        }
        &__lf {
            grid-column: span 11;
            padding-left: 15.9%;
            padding-top: 4.8%;
            padding-bottom: 8.7%;
            background-image: url('../static/img/image1.png');
            background-position: center;
            background-repeat: no-repeat;
            background-size: 100%;

            @media (min-resolution: 2dppx), (min-width: 1500px) {
                background-image: url('../static/img/image1-2x.png');
            }
            @media (max-width: 980px) {
                grid-column: span 9;
            }
            @media (max-width: 560px) {
                grid-column: span 1;
                grid-row: 2 / 3;
            }

            p {
                font-size: 18px;
                color: var(--colorText);
                text-transform: uppercase;
                line-height: 1;
                margin: 5px 0 0;
            }
        }
        &__rh {
            position: relative;
            grid-column: span 5;
            background: var(--bluelight);
            padding-top: 10.7%;
            @media (max-width: 980px) {
                grid-column: span 7;
            }
            @media (max-width: 560px) {
                grid-column: span 1;
                grid-row: 1 / 2;
            }
            &:before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                width: 100%;
                height: 100%;
                background-image: url('data:image/svg+xml;utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%"><line x1="0" y1="100%" x2="100%" y2="0" stroke="rgb(255,255,255)" stroke-width="1"/></svg>');
            }
        }
        &__logo {
            display: flex;
            max-width: 100%;
        }
        &__social {
            margin: 60px 15px 15px 0;
        }
        &__address {
            font-size: 13px;
            color: #fff;
            text-transform: uppercase;
            line-height: 1.077;
            position: absolute;
            left: 12.9%;
            bottom: 36.5%;
            margin: 0;
            @media (max-width: 560px) {
                position: static;
                margin-left: 10%;
                margin-top: 10%;
            }
        }
        &__contacts {
            font-size: 13px;
            color: #fff;
            text-transform: uppercase;
            line-height: 1.077;
            left: 29%;
            bottom: 20%;
            position: absolute;
            margin: 0;
            @media (max-width: 560px) {
                position: static;
                margin-left: 35%;
                margin-top: 20%;
                margin-bottom: 20%;
            }
        }
        &__tel, &__mail {
            color: #fff;
            line-height: 1.077;
            text-decoration: none;
            display: inline-block;

            &:hover {
                color: var(--activeTextColor);
            }

        }
    }
</style>