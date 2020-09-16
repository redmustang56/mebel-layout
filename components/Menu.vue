<template>
    <nav class="menu">
        <nav class="menu__list"
             :class="isOpenMenu ? 'menu__list--active' : ''">
            <a href="#">Home</a>
            <a href="#">Projects</a>
            <a href="#">Studio</a>
            <a href="#">News</a>
            <a href="#">Contact</a>
        </nav>
        <button class="menu__hamburger hamburger"
                :class="isOpenMenu ? 'hamburger--active' : ''"
                @click="openMenu"
                aria-label="Кнопка меню">
            <span class="hamburger__element"></span>
        </button>
    </nav>
</template>

<script>
    export default {
        name: "Menu",
        data: () => ({
            isOpenMenu: false
        }),
        methods: {
            openMenu() {
                this.isOpenMenu = !this.isOpenMenu
            }
        }
    }
</script>

<style lang="postcss" scoped>
    .hamburger {
        background: none;
        display: block;
        cursor: pointer;
        border: 3px solid var(--hamburgerColor);
        transition-property: border-color;
        transition-duration: 500ms;

        &:hover, &:active {
            border-color: var(--hamburgerColorActive);
            .hamburger__element {
                background-color: var(--hamburgerColorActive);
                &::after, &::before {
                    background-color: var(--hamburgerColorActive);
                }
            }
        }
        &:focus {
            border-color: var(--hamburgerColorActive);
        }
        &__element {
            width: 40px;
            height: 3px;
            background-color: var(--hamburgerColor);
            display: block;
            margin: 0 auto;
            transition-property: background-color;
            transition-duration: 500ms;

            &::after, &::before {
                content: '';
                width: 40px;
                height: 3px;
                background-color: var(--hamburgerColor);
                display: block;
                margin: 0 auto;
                transition-property: background-color;
                transition-duration: 500ms;
            }

            &::after {
                transform: translateY(4px);
            }

            &::before {
                transform: translateY(-7px);
            }

        }
        &--active {
            position: relative;
            z-index: 1;
            border-color: var(--hamburgerColorActive);

            &:hover, &:active {
                border-color: var(--hamburgerColorActive);

                .hamburger__element {
                    background-color: var(--hamburgerColor);

                    &::after, &::before {
                        background-color: var(--hamburgerColor);
                    }
                }
            }

            .hamburger__element {
                transform: rotate(45deg);

                &::after {
                    transform: rotate(-90deg);
                    position: relative;
                    z-index: 1;
                }

                &::before {
                    display: none;
                }

            }

        }
    }
    .menu {
        position: absolute;
        right: 11%;
        top: 50px;
        @media (max-width: 980px) {
            right: 30px;
            top: 30px;
        }
        @media (max-width: 768px) {
            height: 100%;
        }
        &__hamburger {
            width: 119px;
            height: 114px;
            @media (max-width: 768px) {
                width: 70px;
                height: 70px;
            }
        }
        &__list {
            background: var(--menuBg);
            list-style: none;
            margin: 0;
            align-items: center;
            flex-wrap: wrap;
            position: absolute;
            right: 0;
            top: 0;
            bottom: 0;
            min-width: 725px;
            padding-right: 119px;
            padding-left: 25px;
            box-sizing: border-box;
            display: none;
            z-index: -9999;
            @media (min-width: 1500px) {
                min-width: 1100px;
            }
            &--active {
                display: flex;
                z-index: 1;
                animation-duration: 500ms;
                animation-name: menu;
                @media (max-width: 768px) {
                    display: block;
                    min-width: auto;
                    padding-right: 70px;
                    padding-top: 15px;
                    overflow-y: auto;
                }
            }
            a {
                font-size: 14px;
                color: #fff;
                text-transform: uppercase;
                line-height: 1.786;
                text-decoration: none;
                padding: 30px;
                @media (max-width: 768px) {
                    display: block;
                    padding: 7px 80px 7px 0;
                }
                &:hover {
                    color: var(--black);
                }
            }
        }
    }
    @keyframes menu {
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
</style>