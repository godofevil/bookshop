<template lang="pug">
    .reviews#reviews
        .reviews__wrap.wrap
            .review__title.block__title Clients Reviews
            .review__subtitle.block__subtitle A few reviews from satisfied clients.
            .reviews__carousel
                .reviews__item
                    .client__avatar
                        img(src="@/assets/client.png" alt="Client photo")
                    .client__name Andrei Fredy
                    .client__description client from romania
                    .client__review
                        p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel facilisis. et dolore magna aliqua. Tuis ipsum sus
                    .client__rate Rate this review
                    .client__stars
                        - for(var i = 0; i < 4; i++)
                            img(src="@/assets/star.png" alt="Rate")
                        img(src="@/assets/halfstar.png" alt="Rate")
                .reviews__item
                    .client__avatar
                        img(src="@/assets/client.png" alt="Client photo")
                    .client__name Andrei Fredy
                    .client__description client from romania
                    .client__review
                        p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel facilisis. et dolore magna aliqua. Tuis ipsum sus
                    .client__rate Rate this review
                    .client__stars
                        - for(var i = 0; i < 4; i++)
                            img(src="@/assets/star.png" alt="Rate")
                        img(src="@/assets/halfstar.png" alt="Rate")
                .reviews__item
                    .client__avatar
                        img(src="@/assets/client.png" alt="Client photo")
                    .client__name Andrei Fredy
                    .client__description client from romania
                    .client__review
                        p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel facilisis. et dolore magna aliqua. Tuis ipsum sus
                    .client__rate Rate this review
                    .client__stars
                        - for(var i = 0; i < 4; i++)
                            img(src="@/assets/star.png" alt="Rate")
                        img(src="@/assets/halfstar.png" alt="Rate")
</template>

<style lang="sass" scoped>
    .reviews
        &__wrap
            padding:
                top: 100px
                bottom: 80px
        &__carousel
            display: grid
            padding-top: 60px
            grid:
                template-columns: repeat(3, 1fr)
                gap: 30px
        &__item
            box-shadow: 0 0 10px 0px rgba(0, 0, 0, 0.18)
            padding: 27px 45px 17px 45px
            text-align: center
            letter-spacing: .1em
    .client
        &__name
            font-size: 14px
            line-height: 28px
            font-weight: 600
            text-transform: uppercase
        &__description
            font-size: 8px
            color: #006699
            line-height: 28px
            text-transform: uppercase
            font-weight: 800
        &__review
            font-size: 12px
            line-height: 16px
            color: #847893
            text-align: left
            padding-top: 30px
            padding-bottom: 30px
            border-bottom: 1px solid #0000004d
        &__rate
            font-size: 8px
            line-height: 14px
            padding:
                top: 30px
                bottom: 9px
        &__stars img
            margin-right: 5px
            &:last-child
                margin-right: 0
    @media(max-width: 960px)
        .reviews
            &__wrap
                padding-top: 20px
                padding-bottom: 30px
            &__carousel
                padding-top: 20px
                grid-template-columns: repeat(2, auto)
            &__item:last-child
                display: none
        .client__review
            padding-top: 15px
            padding-bottom: 15px
    @media(max-width: 640px)
        .reviews
            &__item
                padding: 20px
                &:last-child
                    display: block
            &__carousel
                grid-template-columns: auto
</style>
