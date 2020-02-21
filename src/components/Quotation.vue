<template lang="pug">
    .quotation#author
        img(src="@/assets/quotation.png" alt="Background")
        .quotation__wrap.wrap
            .quotation__left
            .quotation__right
                .quotation__title “This book is a piece from heaven”
                .quotation__text “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel facilisis.”
                .quotation__author
                    span Mark Jackson
                    | - Author
                button.quotation__button.button__gradient Buy Ebook
</template>

<style lang="sass" scoped>
    .quotation
        position: relative
        & img
            position: absolute
            top: -28%
            z-index: -1
        &__wrap
            display: grid
            border-bottom: 3px solid #ffffff0d
            letter-spacing: 0.02em
            grid:
                template-columns: repeat(2, 1fr)
            padding:
                top: 300px
                bottom: 170px

        &__right
            text-align: center
            padding-left: 30px
            grid-area: 1 / 2 / 2 / 3
        &__title
            font-size: 30px
            font-weight: 700
            padding-bottom: 25px
        &__text
            font-size: 16px
            color: #8e819e
            line-height: 24px
        &__author
            font-size: 18px
            padding:
                top: 50px
                bottom: 42px
            & span
                font-weight: 700
    @media(max-width: 1200px)
        .quotation
            img
                top: -15%
                left: -5%
                width: 50vmax
            &__wrap
                padding-top: 50px
                padding-bottom: 30px

    @media(max-width: 640px)
        .quotation
            & img
                top: 0
                width: 50vmax
            &__wrap
                grid-template-columns: auto
            &__right
                padding-left: 0
            &__author
                padding-top: 20px
                padding-bottom: 20px


</style>
