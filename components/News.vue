<template>
    <section class="news">
        <div class="news__left" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 300 }">
            <h2 class="news__title">News</h2>
        </div>
        <div class="news__right" v-scroll-reveal="{ origin: 'top', duration: 1000, distance: '25rem', delay: 300 }">
            <ul class="news__list">
                <li class="news__element">
                    <p class="news__subtitle">Mauris et dui sed justo placerat tristique.</p>
                    <time class="news__date" datetime="2014-07-11">11.07.2014</time>
                    <picture>
                        <source media="(min-width: 1500px)"
                                srcset="~/assets/img/news1-2x.jpg"
                        >
                        <img
                                class="news__img"
                                src="~/assets/img/news1.jpg"
                                srcset="~/assets/img/news1.jpg 1x,
                                         ~/assets/img/news1-2x.jpg 2x"
                                alt="Mauris et dui sed justo placerat tristique.">
                    </picture>
                    <p class="news__description">Maecenas imperdiet nisi lorem, sed fermentum tortor pretium eget. Sed mollis lacus quis nunc cursus cursus. Quisque et magna sit amet sapien fermentum scelerisque eu id massa. Mauris ornare massa vel mauris tempus, vitae tempus urna tincidunt.</p>
                    <p class="news__href">
                        <a class="news__link" href="#">read more</a>
                    </p>
                </li>
                <li class="news__element">
                    <p class="news__subtitle">Proin vehicula nibh massa</p>
                    <time class="news__date" datetime="2014-06-11">11.06.2014</time>
                    <picture>
                        <source media="(min-width: 1500px)"
                                srcset="~/assets/img/news2-2x.jpg"
                        >
                        <img
                                class="news__img"
                                src="~/assets/img/news2.jpg"
                                srcset="~/assets/img/news2.jpg 1x,
                                        ~/assets/img/news2-2x.jpg 2x"
                                alt="Proin vehicula nibh massa ">
                    </picture>
                    <p class="news__description">Praesent non mauris nec orci scelerisque faucibus. Nulla ac varius est. Aenean auctor nisl elit, nec sollicitudin lectus iaculis sed. Maecenas aliquam ligula vitae pharetra scelerisque.</p>
                    <p class="news__href">
                        <a class="news__link" href="#">read more</a>
                    </p>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
    export default {
        name: "News"
    }
</script>

<style lang="postcss" scoped>
    .news {
        display: grid;
        grid-template-columns: repeat(16, 1fr);
        &__left {
            grid-column: span 5;
            background-color: var(--bgNews);
            position: relative;

            @media (max-width: 980px) {
                grid-column: span 16;
            }

            &::before {
                content: '';
                position: absolute;
                left: 0;
                right: 0;
                top: 0;
                bottom: 0;
                width: 100%;
                height: 100%;
                background-image: url('data:image/svg+xml;utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%"><line x1="0" y1="100%" x2="100%" y2="0" stroke="rgb(255,255,255)" stroke-width="1"/></svg>');
            }
        }
        &__title {
            font-size: 48px;
            color: #fff;
            text-transform: uppercase;
            line-height: 1;
            margin: 62.3% 0 35.4% 46.2%;

            @media (max-width: 980px) {
                margin: 10% 0 30% 10%;
            }
            @media (max-width: 768px) {
                margin-bottom: 40%;
                font-size: 30px;
            }
        }
        &__right {
            grid-column: span 11;
            display: flex;
            align-items: center;
            padding-left: 9.6%;
            padding-right: 15.9%;

            @media (max-width: 1500px) {
                padding-right: 2%;
            }
            @media (max-width: 980px) {
                grid-column: span 16;
                padding-left: 2%;
                padding-top: 5%;
                padding-bottom: 5%;
                display: block;
            }
            @media (max-width: 560px) {
                padding-left: 5%;
                padding-right: 5%;
            }
        }
        &__list {
            display: flex;
            @media (max-width: 560px) {
                flex-direction: column;
            }
        }
        &__element {
            flex-basis: 48%;
            display: flex;
            flex-direction: column;

            @media (max-width: 560px) {
                margin-bottom: 4%;
                flex-basis: auto;
            }

            &:first-child {
                margin-right: 4%;
                @media (max-width: 560px) {
                    margin-right: 0;
                }
            }

        }
        &__subtitle {
            font-size: 24px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1;
            min-height: 50px;
            font-weight: 700;
            margin: 0;
            @media (max-width: 560px) {
                min-height: auto;
            }
        }
        &__date {
            font-size: 12px;
            color: rgb(106, 105, 105);
            text-transform: uppercase;
            line-height: 1.2;
            margin: 0 0 4.5% 0;
        }
        &__img {
            display: block;
            width: 100%;
        }
        &__description {
            font-size: 12px;
            color: rgb(106, 105, 105);
            line-height: 1.167;
            text-align: justify;
            margin: 5% 0 2% 0;
        }
        &__href {
            text-align: right;
            margin: auto 0 0 0;
        }
        &__link {
            font-size: 12px;
            color: var(--red);
            text-transform: uppercase;
            line-height: 1.167;
            text-decoration: none;

            &:hover {
                text-decoration: underline;
            }
        }
    }
</style>