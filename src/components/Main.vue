<template lang="pug">
    .main
        .main__wrap.wrap
            .main__left
                .main__text1 BACK TO SCHOOL
                .main__text2 SPECIAL 50% OFF
                .main__text3 For our student community
                button.main__button.button__gradient Get the deal
            .main__right
                img(src="@/assets/main.png" alt="Background")
                .main__slider 02 / 05
</template>

<style lang="sass" scoped>
    .main
        &__wrap
            box-sizing: border-box
            display: grid
            grid-template-columns: auto 755px
            border-bottom: 3px solid #ffffff0d
            overflow: hidden
            padding:
                top: 45px
                bottom: 90px
                left: 70px
        &__right
            z-index: 0
            & img
                position: relative
                left: -50px
        &__left
            align-self: center
            position: relative
            z-index: 1
        &__text1
            color: #75d1c6
            font-size: 22px
            letter-spacing: 0.02em
        &__text2
            color: #fff
            font-size: 56px
            padding: 28px 0
            letter-spacing: 0.02em
            white-space: no-wrap
            font-weight: 700
        &__text3
            color: #bbafca
            font-size: 28px
            letter-spacing: 0.02em
            padding-bottom: 53px
            font-weight: 300
            white-space: wrap

        &__slider
            padding-top: 40px
            font-size: 12px
    @media(max-width: 960px)
        .main
            &__wrap
                padding: 20px 15px
            &__text2
                padding: 20px 0
            &__text3
                padding-bottom: 20px
            &__right img
                left: 0
    @media(max-width: 640px)
        .main
            &__wrap
                grid-template-columns: auto
                grid-row-gap: 15px
                text-align: center
            &__text1, &__text3
                font-size: 18px
            &__text2
                font-size: 35px
                padding: 10px 0
                white-space: wrap
            &__right img
                right: 0
                left: 0
                width: 90vmin
</style>
