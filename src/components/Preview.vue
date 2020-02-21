<template lang="pug">
    .preview#preview
        .preview__wrap.wrap
            .preview__title.block__title eBook Preview
            .preview__subtitle.block__subtitle This is how your new eBook will look.
            .preview__content
                .preview__left
                    .preview__text
                        p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices
                        p.preview__chapter Chapter IV
                        p Duis sed odio sit amet nibh vulputate cursus a sit roin gravida nibh vel velit auctor aliquet. Aenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsum, nec sagittis sem nibh id eliton neque elit ed ut imperdiet nisi massa sodales verbuctum etos. amet mauris morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt auctor a ornare odio. Sed non mauris vitae erat consequat auctor eu in elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.
                        p Mauris in erat justo dullam ac urna eu felis dapibus condimentum sit amet a augue. Sed non neque elit. Sed ut imperdiet nisi. Proin condimentum fermentum nunc setu retiam pharetra, erat sed fermentum feugiat, velit mauris egestas quam, ut aliquam massa nisl quis neque. Suspendisse in orci enim. Tur adipiscing elit nam dui lacuam nec tellus a odio tincidunt auctor a ornare odio. Sed non.Nam nec tellus a odio tincidunt auctor a ornare odio. Sed non mauris vitae erat consequat auctor eu in elit. Class aptent taciti sociosqu ad
                .preview__right
                    .preview__list
                        .preview__item
                            .preview__icon.circle__icon
                                img(src="@/assets/printer.png" alt="Ready to pint")
                            .preview__description
                                .preview__text--bg Ready to print
                                .preview__text--sm Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                        .preview__item
                            .preview__icon.circle__icon
                                img(src="@/assets/open-book.png" alt="Easy to read")
                            .preview__description
                                .preview__text--bg Easy to read
                                .preview__text--sm Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                        .preview__item
                            .preview__icon.circle__icon
                                img(src="@/assets/file.png" alt="Well organised")
                            .preview__description
                                .preview__text--bg Well organised
                                .preview__text--sm Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
</template>

<style lang="sass" scoped>
    @import './../sass/_colors.sass'
    .preview
        &__wrap
            padding:
                top: 85px
                bottom: 88px
            border-bottom: 3px solid #ffffff0d
            overflow: hidden
        &__subtitle
            // padding-top: 25px
        &__content
            padding-top: 55px
            display: grid
            grid:
                template-columns: 1fr 1fr
                column-gap: 160px
        &__right
            display: flex
        &__list
            display: grid
            grid-template-rows: repeat(3, auto)
            align-self: center
            grid-row-gap: 47px
        &__icon
            margin: 0
        &__text
            padding: 15px 27px 35px 30px
            position: relative
            background: #13091f
            color: $font-violet
            font-size: 14px
            line-height: 22px
            letter-spacing: 0.02em
            border:
                left-width: 45px
                right-width: 45px
                top-width: 50px
                bottom-width: 50px
                style: solid
                color: #16062a
            border-radius: 35px
            box-shadow: 0px 0px 19px -4px rgba(0,0,0,0.75)
            & p
                margin-bottom: 24px
            & p:last-child
                margin-bottom: 0
            & .preview__chapter
                font-size: 18px
                font-weight: 600
                color: #b9acc9
            &::after
                position: absolute
                width: 30px
                height: 30px
                content: ''
                background: #120424
                left: 50%
                transform: translateX(-50%)
                bottom: -40px
                border-radius: 50%
            &::before
                position: absolute
                content: url('./../assets/man.png')
                width: auto
                height: auto
                bottom: -130px
                right: -165px
        &__item
            display: grid
            grid:
                template-columns: 180px 1fr
                column-gap: 40px
        &__description
            align-self: center
        &__text--bg
            font-size: 24px
            padding-bottom: 20px
            font-weight: 600
        &__text--sm
            font-size: 12px
            line-height: 18px
            color: #847893

    @media(max-width: 960px)
        .preview
            &__wrap
                padding-top: 20px
                padding-bottom: 30px
            &__content
                padding-top: 15px
                grid-template-columns: auto
                grid-gap: 20px
            &__right
                justify-content: center
            &__list
                grid-row-gap: 20px
            &__item
                grid-template-columns: auto 1fr

    @media(max-width: 640px)
        .preview
            &__text
                border-left-width: 25px
                border-right-width: 25px
                border-top-width: 25px
                & p:last-child
                    display: none
                &::before
                    display: none

                &--bg
                    padding-bottom: 0
            &__item
                grid-template-columns: auto
                & .circle__icon
                    justify-self: center
            &__description
                text-align: center

    @media(max-width: 320px)
        .preview__text
            padding: 10px
            border: 20px solid #16062a

</style>
