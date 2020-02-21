<template lang="pug">
    header.header
        .header__wrap.wrap
            .header__top
                a.header__link(href="/")
                    img.header__logo(src="@/assets/logo.png")
                    .header__title Bookshop
                .header__search
                    input.search__input(placeholder="Search..." type="search")
                .header__login
                    a(href="/")
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" width="22.15" height="23.156" viewBox="0 0 22.15 23.156">
                          <path d="M16.098,14.210 C17.991,12.751 19.212,10.494 19.212,7.954 C19.212,3.556 15.564,-0.010 11.066,-0.010 C6.567,-0.010 2.919,3.556 2.919,7.954 C2.919,10.494 4.140,12.751 6.034,14.210 C2.638,15.901 0.248,19.244 -0.016,23.160 L1.467,23.160 C1.753,19.493 4.191,16.420 7.546,15.129 C8.613,15.630 9.804,15.919 11.066,15.919 C12.328,15.919 13.518,15.630 14.585,15.129 C17.940,16.420 20.378,19.493 20.664,23.160 L22.147,23.160 C21.884,19.244 19.493,15.901 16.098,14.210 ZM11.066,14.471 C7.384,14.471 4.401,11.554 4.401,7.954 C4.401,4.354 7.384,1.437 11.066,1.437 C14.747,1.437 17.731,4.354 17.731,7.954 C17.731,11.554 14.747,14.471 11.066,14.471 Z" />
                        </svg>
            nav.header__nav.nav
                ul.nav__list
                    li.nav__item
                        a.nav__link(href="#steps") eBook Purchase
                    li.nav__item
                        a.nav__link(href="#preview") eBook Preview
                    li.nav__item
                        a.nav__link(href="#reviews") Reviews
                    li.nav__item
                        a.nav__link(href="#author") Author
                    li.nav__item
                        a.nav__link(href="#contacts") Contact
            <Responsive />
</template>

<script>
    import Responsive from '@/components/Responsive'
    export default {
        name: 'Header',
        components: {
            Responsive
        }
    }
</script>

<style lang="sass" scoped>
    @import './../sass/_colors.sass'

    .header
        background: linear-gradient(270deg, rgba(26,35,75,1) 0%, rgba(22,22,55,1) 100%)
        &__wrap
            box-sizing: border-box
            padding:
                left: 70px
                right: 70px
        &__top
            padding:
                top: 17px
                bottom: 43px

            display: grid
            grid-template-columns: repeat(3, auto)
            align-items: center
        &__link
            display: flex
            align-items: center
        &__title
            padding-left: 10px
            text-transform: uppercase
            font-size: 24px
            color: #fff
            transition: color .3s
        &__login svg
            fill: #fff
            transition: fill .3s
        &__login:hover svg
                fill: $primary-blue

    .search__input
        background: url('./../assets/search.svg') no-repeat 20px 50%
        min-width: 580px
        height: 50px
        outline: 0
        border: 1px solid $primary-grey
        padding: 18px 20px 17px 60px
        border-radius: 50px
        font-size: 18.13px
        color: #fff
        font-weight: 300
        letter-spacing: 0.04em
        font-family: Montserrat
        font-weight: 300
        transition: background-color .3s
        &::placeholder
            color: #fff
        &:focus
            background-color: #75d1bf0d
    .nav
        &__list
            display: flex
            justify-content: center
            padding-bottom: 28px
        &__item
            margin-right: 50px
            padding-bottom: 12px
            transition: border-bottom .3s
            border-bottom: 3px solid transparent
            &:hover, &:active
                border-bottom: 3px solid $primary-blue
                & .nav__link
                    color: #fff
            &:last-of-type
                margin-right: 0
        &__link
            color: $primary-grey
            font-size: 16.12px
            letter-spacing: 0.04em
            transition: color .3s

    @media(max-width: 960px)
        .header
            &__wrap
                padding-left: 15px
                padding-right: 15px
            &__top
                grid:
                    template-columns: repeat(2, 50%)
                row-gap: 20px
                padding-bottom: 20px
            &__login
                grid-area: 1 / 2 / 2 / 3
                justify-self: flex-end
            &__search
        .search__input
            min-width: 200%
        .nav__item
            margin-right: 30px

    @media(max-width: 640px)
        .header__nav, .header__login
            display: none
        .header
            &__top
                grid-template-columns: 50%
        .search__input
            min-width: 100%
</style>
