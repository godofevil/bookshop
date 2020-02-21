<template lang="pug">
    header.header
        .header__wrap.wrap
            .header__top
                a.header__link(href="/")
                    img.header__logo(src="@/assets/logo.png" alt="Logo")
                    .header__title Bookshop
                .header__search
                    input.search__input(placeholder="Search..." type="search")
                .header__login
                    a(href="/")
                        img(src="@/assets/login.svg" alt="Login")
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

    .search-fade-enter input
        width: 20%
    .search-fade-enter-to input
        width: 100%
    .search-fade-enter-active
        transition: opacity .5s

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
        background: url('./../assets/search.svg') no-repeat 18px 50%
        width: 580px
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
            width: 200%
        .nav__item
            margin-right: 30px

    @media(max-width: 640px)
        .header__nav, .header__login
            display: none
        .header
            &__top
                grid-template-columns: 1fr
        .search__input
            width: 30%
            transition: width .3s
            &:focus
                width: 100%
</style>
