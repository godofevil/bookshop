<template lang="pug">
    <div>
        .responsive__button(@click="menuVisible = true"  v-if="!this.menuVisible")
            img(src="@/assets/menu.svg")
        transition(name="fade")
            .responsive__menu(v-if="this.menuVisible")
                .responsive__close(@click="menuVisible = false")
                    img(src="@/assets/close.svg")
                ul.menu__list
                    li.menu__item
                        a.menu__link(href="#") eBook Purchase
                    li.menu__item
                        a.menu__link(href="#") eBook Preview
                    li.menu__item
                        a.menu__link(href="#") Reviews
                    li.menu__item
                        a.menu__link(href="#") Author
                    li.menu__item
                        a.menu__link(href="#") Contact
    </div>
</template>

<script>
    export default {
        data() {
            return {
                menuVisible: false
            }
        }
    }
</script>

<style lang="sass" scoped>
    .fade-enter, .fade-leave-to
        opacity: 0
    .fade-enter-to, .fade-leave
        opacity: 1
    .fade-enter-active, .fade-leave-active
        transition: opacity .5s

    @mixin button
        display: flex
        align-items: center
        justify-content: center
        position: absolute
        width: 50px
        height: 50px
        top: 25px
        right: 25px
        color: red
        box-sizing: border-box
    .responsive
        &__button
            @include button
            background: #fff
            display: none
            border-radius: 10px
            @media (max-width: 640px)
                display: flex
        &__menu
            position: absolute
            background: #fffffff0
            width: 100%
            height: auto
            top: 0
            left: 0
            display: flex
            justify-content: center
            padding: 50px 0
            z-index: 2
        &__close
            @include button
    img
        width: 35px
    .menu
        &__item
            padding-bottom: 20px
        &__link
            font-size: 1.5rem
            line-height: 20px
            font-weight: 700
            color: #1371a6
    .submenu__list
        .menu__item
            padding: 5px 0 5px 20px
        .menu__link
            font-size: 1.3rem
</style>
