<template>
    <section class="projects">
        <div class="projects__element projects__element--one" v-scroll-reveal="{ origin: 'left', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="projects__links links">
                <a class="links__link" href="#">All</a>
                <a class="links__link" href="#">House</a>
                <a class="links__link" href="#">Commercial</a>
                <a class="links__link" href="#">Personal</a>
                <a class="links__link" href="#">Studio Lab</a>
            </div>
            <h1 class="projects__title">projects</h1>
        </div>
        <div class="projects__element projects__element--two" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 600 }">
            <div class="projects__info">
                <h2 class="projects__name">FONDUE</h2>
                <p class="projects__description"><b>Project Assistant:</b> Francesco Dompieri</p>
                <p class="projects__description"><b>Material:</b> Glass and Metal</p>
                <p class="projects__description"><b>Typology:</b> Suspension lamp</p>
                <p class="projects__description"><b>Client:</b> David Design</p>
                <p class="projects__description"><b>Year:</b> 2014</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--three" v-scroll-reveal="{ origin: 'right', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="projects__info">
                <h2 class="projects__name">potter</h2>
                <p class="projects__description"><b>for</b> stelton</p>
                <p class="projects__description projects__description--lowercase">Potter focuses on the functionality and process of preparing tea. a big sieve allows the flavor of to evenly brewed.</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--four" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 600 }">
            <div class="projects__info">
                <h2 class="projects__name">tabano</h2>
                <p class="projects__description"><b>DESIGNER:</b> PATRICIA URQUIOLA</p>
                <p class="projects__description"><b>Typology:</b> Armchairs</p>
                <p class="projects__description"><b>Client:</b> B&B ITALIA</p>
                <p class="projects__description"><b>Year:</b> 2014</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--five" v-scroll-reveal="{ origin: 'left', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="projects__info">
                <h2 class="projects__name">louis xx</h2>
                <p class="projects__description"><b>DESIGNER:</b> philippe starck</p>
                <p class="projects__description"><b>Typology:</b> chairs</p>
                <p class="projects__description"><b>Client:</b> vitra</p>
                <p class="projects__description"><b>Year:</b> 2012</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--six" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 600 }">
            <div class="projects__info">
                <h2 class="projects__name">395-396 P22</h2>
                <p class="projects__description"><b>DESIGNER:</b> Patrick Norguet</p>
                <p class="projects__description"><b>Typology:</b> ARMchairs</p>
                <p class="projects__description"><b>Client:</b> Cassina</p>
                <p class="projects__description"><b>Year:</b> 2013</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--seven" v-scroll-reveal="{ origin: 'right', duration: 1000, distance: '25rem', delay: 300 }">
            <div class="projects__info">
                <h2 class="projects__name">FIJI</h2>
                <p class="projects__description"><b>DESIGNER:</b> Cuno Frommherz</p>
                <p class="projects__description"><b>Typology:</b> armchairs</p>
                <p class="projects__description"><b>Year:</b> 2012</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--eight" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 600 }">
            <div class="projects__info">
                <h2 class="projects__name">Sesann</h2>
                <p class="projects__description"><b>DESIGNER:</b> Gianfranco Frattini</p>
                <p class="projects__description"><b>Typology:</b> armchairs</p>
                <p class="projects__description"><b>Client:</b> cassina</p>
                <p class="projects__description"><b>Year:</b> 1970</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--nine" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 700 }">
            <div class="projects__info">
                <h2 class="projects__name">Alessi</h2>
                <p class="projects__description"><b>DESIGNER:</b> Piero Lissoni</p>
                <p class="projects__description"><b>Client:</b> Alessi</p>
                <p class="projects__description"><b>Year:</b> 2013</p>
            </div>
            <div class="projects__counter">
                <a class="projects__view" href="#">
                    <span>view project</span>
                </a>
                <p class="projects__like like">
                    <button aria-label="Like" class="like__btn">
                        <svg-icon class="i-icon" name="heart"></svg-icon>
                    </button>
                    <span class="like__counts">+ 200</span>
                </p>
            </div>
        </div>
        <div class="projects__element projects__element--ten" v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 800 }">
            <p class="projects__subtitle">timeline</p>
            <div class="projects__links links">
                <a class="links__link" href="#">2014</a>
                <a class="links__link" href="#">2013</a>
                <a class="links__link" href="#">2012</a>
                <a class="links__link" href="#">2011</a>
                <a class="links__link" href="#">2010</a>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Project"
    }
</script>

<style lang="postcss" scoped>
    .projects {
        display: grid;
        grid-template-columns: repeat(16, 1fr);
        @media (max-width: 560px) {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr;
        }
        &__element {
            &--one {
                background-color: var(--thirty);
                grid-column: span 5;
                grid-row: span 2;
                position: relative;

                @media (max-width: 980px) {
                    grid-column: span 7;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
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

                .projects__title {
                    font-size: 48px;
                    color: #fff;
                    text-transform: uppercase;
                    line-height: 1;
                    font-weight: normal;
                    margin: 12.9% 0 34.4% 46.2%;
                    @media (max-width: 980px) {
                        font-size: 30px;
                    }
                }

                .projects__links {
                    margin-top: 36.5%;
                    margin-left: calc(27.9% - 25px);
                    margin-bottom: 12.9%;
                    position: relative;
                    z-index: 1;
                    @media (max-width: 980px) {
                        margin-left: 20%;
                    }
                }

            }
            &--two {
                background: url('../static/img/image2.png') right top no-repeat #ffffff;
                background-size: cover;
                grid-column: span 6;
                grid-row: span 2;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image2-2x.png');
                }

                @media (max-width: 980px) {
                    grid-column: span 9;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }
                .projects__info {
                    margin-left: 17.5%;
                    margin-top: 15.7%;
                    @media (max-width: 768px) {
                        margin-left: 8%;
                        margin-top: 7%;
                    }
                }

                .projects__counter {
                    margin-left: 19.2%;
                    margin-top: 11.4%;
                    margin-bottom: 12.2%;
                    @media (max-width: 768px) {
                        margin-left: 9%;
                        margin-top: 7%;
                        margin-bottom: 3%;
                    }
                }

            }
            &--three {
                background: url('../static/img/image3.png') left center no-repeat var(--bgThree);
                background-size: cover;
                grid-column: span 5;
                grid-row: span 1;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image3-2x.png');
                }

                @media (max-width: 980px) {
                    grid-column: span 9;
                    grid-row: span 2;
                    background-size: 100%;
                }
                @media (max-width: 768px) {
                    background-position: -100px 100%;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                    background-position: 40px 100%;
                }
                .projects__like {
                    margin-top: 5.8%;
                }

                .projects__description {
                    max-width: 39%;
                }


                .projects__info {
                    margin-left: 8.6%;
                    margin-top: 7.5%;
                }

                .projects__counter {
                    margin-top: 4%;
                    margin-bottom: 4.5%;
                    margin-left: 8.6%;
                }

            }
            &--four {
                background: url('../static/img/image4.png') center top no-repeat var(--bgFour);
                background-size: 100%;
                grid-column: span 5;
                grid-row: span 2;
                padding-top: 72%;
                display: flex;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image4-2x.png');
                }
                @media (max-width: 980px) {
                    grid-column: span 7;
                    grid-row: span 2;
                }
                @media (max-width: 768px) {
                    display: block;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }

                .projects__counter {
                    display: flex;
                    align-items: flex-start;
                    margin-top: 32px;
                    margin-right: 3%;
                    margin-bottom: 3%;
                    @media (max-width: 980px) {
                        display: block;
                    }
                    @media (max-width: 768px) {
                        margin-left: 8%;
                    }
                }

                .projects__like {
                    margin-top: 0;
                    @media (max-width: 980px) {
                        margin-top: 15%;
                    }
                    @media (max-width: 768px) {
                        margin-top: 8%;
                    }
                }

                .projects__info {
                    margin-left: 12.9%;
                    margin-right: 4.3%;
                    margin-bottom: 7.5%;
                    @media (max-width: 768px) {
                        margin-left: 8%;
                        margin-right: 2%;
                    }
                }

            }
            &--five {
                background: url('../static/img/image5.png') center top no-repeat;
                background-size: cover;
                grid-column: span 3;
                grid-row: span 2;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image5-2x.png');
                }
                @media (max-width: 980px) {
                    grid-column: span 4;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }
                .projects__info {
                    margin-top: 10%;
                    margin-left: 10%;
                    margin-bottom: 12.9%;
                }

                .projects__counter {
                    margin-left: 10%;
                    margin-bottom: 70%;
                }

                .projects__like {
                    margin-top: 9.2%;
                }

                .projects__view {
                    color: #ffffff;

                    &:hover {

                        span {
                            border-color: #ffffff;
                        }

                    }

                }

                .projects__description, .projects__name {
                    color: #ffffff;
                }

                .like__btn {

                    svg {
                        fill: #fff;
                    }

                }

                .like__counts {
                    color: #fe7c7c;
                }

            }
            &--six {
                background: url('../static/img/image6.png') center top no-repeat var(--bgSix);
                background-size: cover;
                grid-column: span 8;
                grid-row: span 2;
                display: flex;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image6-2x.png');
                }

                @media (max-width: 980px) {
                    grid-column: span 12;
                }
                @media (max-width: 768px) {
                    background-position: -70px 20px;
                    display: block;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }
                .projects__info {
                    margin-left: 48.1%;
                    margin-top: 12.1%;
                    margin-bottom: 4%;
                    @media (max-width: 768px) {
                        margin-left: 40%;
                        margin-top: 6%;
                    }
                }

                .projects__counter {
                    margin-left: 4%;
                    margin-top: 12.1%;
                    margin-bottom: 4%;
                    @media (max-width: 768px) {
                        margin-left: 62%;
                        margin-top: 6%;
                    }
                }

                .projects__like {
                    margin-top: 12.5%;
                }

            }
            &--seven {
                background: url('../static/img/image7.png') left top no-repeat #fff;
                background-size: 100%;
                grid-column: span 5;
                grid-row: span 1;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image7-2x.png');
                }
                @media (max-width: 980px) {
                    grid-column: span 7;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }

                .projects__info {
                    margin-left: 52.6%;
                    margin-top: 10.7%;
                }

                .projects__counter {
                    margin-left: 52.6%;
                    margin-top: 5%;
                    margin-bottom: 5.3%;
                }

                .projects__like {
                    margin-top: 9.1%;
                }

            }
            &--eight {
                background: url('../static/img/image8.png') left top no-repeat var(--bgEight);
                background-size: 100%;
                grid-column: span 8;
                grid-row: span 1;
                display: flex;
                padding-top: 27.2%;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image8-2x.png');
                }
                @media (max-width: 980px) {
                    grid-column: span 9;
                }
                @media (max-width: 768px) {
                    display: block;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }
                .projects__info {
                    margin-left: 20.4%;
                    margin-bottom: 2.7%;
                    @media (max-width: 768px) {
                        margin-left: 9%;
                    }
                }

                .projects__counter {
                    display: flex;
                    margin-top: 32px;
                    margin-left: 6.1%;
                    margin-bottom: 2.7%;
                    align-items: flex-start;
                    flex-basis: 210px;
                    justify-content: space-between;
                    @media (max-width: 980px) {
                        display: block;
                    }
                }

                .projects__like {
                    margin-top: 0;
                    @media (max-width: 980px) {
                        margin-top: 11%;
                    }
                    @media (max-width: 768px) {
                        margin-top: 6%;
                    }
                }

            }
            &--nine {
                background: url('../static/img/image9.png') left top no-repeat var(--bgNine);
                background-size: 100%;
                grid-column: span 3;
                grid-row: span 1;

                @media (min-resolution: 2dppx), (min-width: 1500px) {
                    background-image: url('../static/img/image9-2x.png');
                }
                @media (max-width: 980px) {
                    grid-column: span 9;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
                }

                .projects__info {
                    margin-left: 50%;
                    margin-top: 25%;
                    margin-bottom: 8.3%;
                }

                .projects__counter {
                    margin-left: 40%;
                    margin-bottom: 11.6%;
                }

                .projects__like {
                    margin-top: 14.7%;
                }

            }
            &--ten {
                background-color: var(--thirty);
                grid-column: span 5;
                grid-row: span 1;
                position: relative;

                @media (max-width: 980px) {
                    grid-column: span 7;
                }
                @media (max-width: 560px) {
                    grid-column: span 1;
                    grid-row: span 1;
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
                    background-image: url('data:image/svg+xml;utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%"><line x1="0" y1="100%" x2="65%" y2="0" stroke="rgb(255,255,255)" stroke-width="1"/></svg>');
                }

                .projects__links {
                    position: relative;
                    z-index: 1;
                    margin-left: calc(21.5% - 25px);
                    margin-bottom: 32.2%;
                }

                .projects__subtitle {
                    font-size: 14px;
                    color: var(--colorText);
                    text-transform: uppercase;
                    line-height: 1;
                    margin-bottom: 0;
                    margin-left: 21.5%;
                    margin-top: 11.8%;
                }

            }
        }
        &__name {
            font-size: 24px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1;
            margin: 0 0 10px 0;
        }
        &__description {
            font-size: 12px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1;
            &--lowercase {
                text-transform: initial;
            }
        }
        &__view {
            font-size: 18px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1;
            display: inline-block;
            background: url('../static/img/arrow-view.svg') left center no-repeat;
            padding-left: 25px;
            padding-right: 25px;
            text-decoration: none;

            span {
                border-bottom: 1px solid transparent;
                transition-property: border-color;
                transition-duration: 500ms;
            }

            &:hover {
                span {
                    border-color: var(--colorText);
                }
            }

        }
        &__like {
            max-width: 145px;
            text-align: center;
            margin: 22.3% 0 0 0;
        }
    }
    .like {
        &__btn {
            background: none;
            border: none;
            box-shadow: none;
            cursor: pointer;
            padding: 0;

            svg {
                width: 24px;
                height: 22px;
                transition-duration: 500ms;
                transition-property: fill;
            }

            &:hover {
                svg {
                    color: var(--red);
                }
            }

        }
        &__counts {
            font-size: 11px;
            color: var(--red);
            text-transform: uppercase;
            line-height: 1.091;
            display: block;
            margin: 5px 0 0 0;
        }
    }
    .links {
        &__link {
            font-size: 13px;
            color: #fff;
            text-transform: uppercase;
            line-height: 1.077;
            text-decoration: none;
            padding-left: 25px;
            transition-property: color;
            transition-duration: 500ms;

            &:hover {
                color: var(--black);
                background: url('../static/img/arrow.svg') left center no-repeat;
            }

        }
    }
</style>