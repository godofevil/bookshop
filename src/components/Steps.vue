<template lang="pug">
    .steps#steps
        .steps__wrap.wrap
            .steps__title.block__title It’s easy as this
            .steps__subtitle.block__subtitle Four easy steps to get your new eBook. What are your waiting for?
            .steps__list
                .steps__item
                    .step__icon.circle__icon(steps-number="1")
                        img(src="@/assets/book.png" alt="Step 1")
                    .step__title eBook Preview
                    .step__description
                        |Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                .steps__divider
                .steps__item
                    .step__icon.circle__icon(steps-number="2")
                        img(src="@/assets/cash-register.png" alt="Step 2")
                    .step__title eBook Preview
                    .step__description
                        |Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                .steps__divider
                .steps__item
                    .step__icon.circle__icon(steps-number="3")
                        img(src="@/assets/support.png" alt="Step 3")
                    .step__title eBook Preview
                    .step__description
                        |Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                .steps__divider
                .steps__item
                    .step__icon.circle__icon(steps-number="4")
                        img(src="@/assets/reading.png" alt="Step 4")
                    .step__title eBook Preview
                    .step__description
                        |Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
            button.steps__button.button__gradient Get the deal
</template>

<style lang="sass" scoped>
    @import './../sass/_colors.sass'
    .steps
        &__wrap
            text-align: center
            padding:
                top: 52px
                bottom: 80px
            border-bottom: 3px solid #ffffff0d
        &__list
            display: grid
            grid-template-columns: repeat(7, auto)
            justify-items: center
            padding:
                top: 60px
                bottom: 78px
                left: 100px
                right: 100px
        &__divider
            height: 30%
            width: 76px
            border-bottom: 2px solid #101835
    .step
        &__icon::before
            position: absolute
            width: 35px
            height: 35px
            background: #12608e
            content: attr(steps-number)
            border-radius: 50%
            box-sizing: border-box
            top: 15px
            left: 20px
            padding: 9px
            font-size: 14px
            font-weight: 600
        &__title
            font-size: 18px
            font-weight: 600
            padding-top: 30px
            padding-bottom: 15px
        &__description
            font-size: 12px
            color: $font-violet
            font-weight: 300
            line-height: 18px
    @media(max-width: 1200px)
        .steps
            &__list
                padding-left: 0
                padding-right: 0
    @media(max-width: 960px)
        .steps
            &__wrap
                padding-top: 20px
                padding-bottom: 30px
            &__list
                grid-template-columns: repeat(2, 1fr)
                grid-gap: 10px
                padding: 30px 0 60px 0
            &__divider
                display: none
        .step
            &__title
                padding: 10px 0
            &__icon
                width: 100px
                height: 100px
                &::before
                    top: 5px
                    left: 5px
                    width: 25px
                    height: 25px
                    font-size: 12px
                    padding: 5px
                & img
                    width: 50px
    @media(max-width: 320px)
        .steps__list
            grid-template-columns: auto
            grid-gap: 20px

</style>
