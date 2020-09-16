<template>
    <section class="studio">
        <div class="studio__left" v-scroll-reveal="{ origin: 'left', duration: 1000, distance: '25rem', delay: 300 }">
            <h2 class="studio__title">studio</h2>
        </div>
        <div class="studio__right" v-scroll-reveal="{ origin: 'right', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="studio__information">
                <p class="studio__text studio__text--bold-italic">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus sollicitudin eros sit amet nulla rhoncus dictum.</p>
                <p class="studio__text studio__text--bold-italic">Nam rhoncus fringilla dolor vitae vulputate. Nullam quis eros lorem. Integer cursus erat a orci congue feugiat. Cras rhoncus mollis libero, id aliquet purus varius sed.</p>
                <p class="studio__text">Aenean ullamcorper porta nisl, ac lobortis elit commodo placerat.</p>
                <p class="studio__text">Vivamus eget laoreet enim. Sed nunc dui, egestas vel diam convallis, faucibus iaculis sapien. Sed ut vulputate nisi.</p>
                <p class="studio__text">Proin tempor risus tellus. Maecenas sit amet fringilla urna, vel iaculis velit. Sed ac felis et sem mollis dictum sed id orci.</p>
            </div>
            <div class="studio__description">
                <picture>
                    <source media="(min-width: 1500px)"
                            srcset="~/assets/img/studio-img-2x.jpg"
                    >
                    <img
                            class="studio__img"
                            src="~/assets//img/studio-img.jpg"
                            srcset="~/assets//img/studio-img.jpg 1x,
                                    ~/assets//img/studio-img-2x.jpg 2x"
                            alt="Фотография студии">
                </picture>
                <h3 class="studio__subtitle">awards</h3>
                <div class="studio__list">
                    <div class="studio__list-item">Aenean ullamcorper porta nisl,
                        ac lobortis elit
                        commodo placerat.
                        Vivamus </div>
                    <div class="studio__list-item">Aenean ullamcorper porta nisl,
                        ac lobortis elit
                        commodo placerat.
                        Vivamus </div>
                </div>
            </div>
        </div>
        <div class="studio__staff"  v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 300 }">
            <p class="studio__staff-title">STAFF.</p>
            <p class="studio__staff-text">Sit amet laoreet sapien dictum. Sed eget eros augue. Pellentesque tempor mi sit amet nisi tincidunt tincidunt. Fusce malesuada lectus sed mauris pharetra faucibus.</p>
            <p class="studio__staff-text">Aenean diam tortor, hendrerit ac pulvinar vel, condimentum ac velit. Phasellus eu odio elit. Aenean volutpat mi quam, ut ornare augue tempus ut.</p>
            <p class="studio__staff-text">Morbi sagittis diam mauris, in adipiscing nulla convallis ut.</p>
        </div>
        <div class="studio__persons"  v-scroll-reveal="{ origin: 'top', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="persons">
                <div class="persons__item">
                    <picture>
                        <source media="(min-width: 1500px)"
                                srcset="~/assets//img/person1-2x.jpg"
                        >
                        <img
                                class="persons__img"
                                src="~/assets//img/person1.jpg"
                                srcset="~/assets//img/person1.jpg 1x,
                                        ~/assets//img/person1-2x.jpg 2x"
                                alt="philippe starck">
                    </picture>
                    <p class="persons__name">philippe starck</p>
                    <p class="persons__post">designer</p>
                    <div class="persons__info">
                        <a class="persons__cv" href="#">
                            <span>CV</span>
                        </a>
                        <Social :isMiniSvg="isMiniSvg" />
                    </div>
                </div>
                <div class="persons__item">
                    <picture>
                        <source media="(min-width: 1500px)"
                                srcset="~/assets//img/person2-2x.jpg"
                        >
                        <img
                                class="persons__img"
                                src="/~/assets/img/person2.jpg"
                                srcset="~/assets//img/person2.jpg 1x,
                                        ~/assets//img/person2-2x.jpg 2x"
                                alt="mario bellini">
                    </picture>
                    <p class="persons__name">mario bellini</p>
                    <p class="persons__post">designer</p>
                    <div class="persons__info">
                        <a class="persons__cv" href="#">
                            <span>CV</span>
                        </a>
                        <Social :isMiniSvg="isMiniSvg" />
                    </div>
                </div>
                <div class="persons__item">
                    <picture>
                        <source media="(min-width: 1500px)"
                                srcset="~/assets//img/person3-2x.jpg"
                        >
                        <img
                                class="persons__img"
                                src="~/assets//img/person3.jpg"
                                srcset="~/assets//img/person3.jpg 1x,
                                        ~/assets//img/person3-2x.jpg 2x"
                                alt="patricia urquiola">
                    </picture>
                    <p class="persons__name">patricia urquiola</p>
                    <p class="persons__post">designer</p>
                    <div class="persons__info">
                        <a class="persons__cv" href="#">
                            <span>CV</span>
                        </a>
                        <Social :isMiniSvg="isMiniSvg" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import Social from '~/components/Social'

    export default {
        name: "Studio",
        data: () => ({
            isMiniSvg: true
        }),
        components: {
            Social
        }
    }
</script>

<style lang="postcss" scoped>
    .studio {
        display: grid;
        grid-template-columns: repeat(16, 1fr);

        @media (max-width: 560px) {
            grid-template-columns: 1fr;
        }

        &__left, &__staff {
            grid-column: span 5;
            @media (max-width: 560px) {
                grid-column: span 1;
            }
        }

        &__right, &__persons {
            grid-column: span 11;
            @media (max-width: 1500px) {
                padding-right: 2%;
            }
            @media (max-width: 560px) {
                grid-column: span 1;
            }
        }
        &__persons {
            @media (max-width: 768px) {
                padding-top: 2%;
            }
            @media (max-width: 560px) {
                padding-right: 5%;
                padding-left: 5%;
            }
        }
        &__left {
            background-color: var(--bgStudio);
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
            padding-left: 9.6%;
            padding-top: 9.1%;
            padding-bottom: 4.3%;
            padding-right: 15.9%;
            display: flex;
            @media (max-width: 980px) {
                grid-column: span 16;
                padding-left: 2%;
            }
            @media (max-width: 560px) {
                display: block;
                padding-left: 5%;
                padding-right: 5%;
            }
        }
        &__information {
            flex-basis: 48%;
            margin-right: 4%;
        }
        &__description {
            flex-basis: 48%;
        }
        &__text {
            font-size: 18px;
            color: var(--colorText);
            line-height: 1;
            margin: 5.4% 0;

            &:first-child {
                margin-top: 0;
            }
            &--bold-italic {
                font-weight: 500;
            }
        }
        &__img {
            display: block;
            width: 100%;
        }
        &__subtitle {
            font-size: 14px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1.286;
            margin: 9.4% 0 5%;
            border-bottom: 1px solid rgba(0, 0, 0, 0.18);
            font-weight: 700;
        }
        &__list {
            list-style: none;
            padding: 0;
            display: flex;
            margin: 2.5% 0;
            &-item {
                font-size: 12px;
                color: var(--colorText);
                text-transform: uppercase;
                line-height: 1.167;

                &:first-child {
                    margin-right: 9.4%;
                }
            }
        }
        &__staff {
            padding-left: 35.4%;
            padding-right: 6.4%;
            padding-top: 12.9%;
            padding-bottom: 19.3%;

            @media (max-width: 980px) {
                padding-left: 4%;
                padding-right: 4%;
            }
            @media (max-width: 768px) {
                padding-top: 2%;
                padding-bottom: 2%;
            }
            @media (max-width: 560px) {
                padding-left: 5%;
                padding-right: 5%;
            }

            &-text {
                font-size: 14px;
                color: var(--colorText);
                line-height: 1;
                margin: 7.4% 0;
                font-weight: 300;

                @media (max-width: 768px) {
                    margin: 3% 0;
                }

                &:last-child {
                    margin-bottom: 0;
                }
            }
            &-title {
                font-size: 14px;
                color: var(--colorText);
                text-transform: uppercase;
                line-height: 1;
                margin: 0 0 7.4% 0;
                font-weight: 700;

                @media (max-width: 768px) {
                    margin: 3% 0;
                }
            }
            &__persons {
                padding-top: 5.7%;
                padding-right: 15.9%;
            }
        }
    }
    .persons {
        display: flex;
        @media (max-width: 980px) {
            flex-wrap: wrap;
        }
        @media (max-width: 560px) {
            flex-direction: column;
            flex-wrap: nowrap;
        }
        &__item {
            flex-basis: 31%;
            margin-right: 3.4%;

            @media (max-width: 980px) {
                flex-basis: 47%;
                margin-right: 3%;
                margin-top: 3.5%;
                margin-bottom: 3.5%;
            }
            @media (max-width: 560px) {
                flex-basis: auto;
                margin-right: 0;
            }

            &:last-child {
                margin-right: 0;
            }
            &:nth-child(even) {
                @media (max-width: 560px) {
                    margin-right: 0;
                }
            }
        }
        &__img {
            display: block;
            width: 100%;
        }
        &__name {
            font-size: 13px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1.231;
            margin: 5.5% 0 0 0;
            font-weight: 700;
        }
        &__post {
            font-size: 12px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1.333;
            margin: 0 0 5.5% 0;
        }
        &__info {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        &__cv {
            font-size: 14px;
            color: var(--red);
            text-transform: uppercase;
            line-height: 1.143;
            text-decoration: none;
            padding-right: 25px;
            background: url('../static/img/arrow-left.svg') right center no-repeat;

            &:hover {
                span {
                    border-color: var(--red);
                }
            }

            span {
                border-bottom: 1px solid transparent;
                transition-duration: 500ms;
                transition-property: border-color;
            }
        }
    }
</style>