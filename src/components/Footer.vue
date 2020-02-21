<template lang="pug">
    .footer
        .footer__wrap.wrap
            .footer__top
                .footer__logo
                    img(src="@/assets/logo-footer.png" alt="Logo")
                nav.footer__nav
                    ul.footer__list
                        li.footer__item
                            a.footer__link(href="#steps") eBook Purchase
                        li.footer__item
                            a.footer__link(href="#preview") eBook Preview
                        li.footer__item
                            a.footer__link(href="#reviews") Reviews
                        li.footer__item
                            a.footer__link(href="#author") Author
                        li.footer__item
                            a.footer__link(href="#contacts") Contact
                .footer__socials
                    a(href="fb.com")
                        img(src="@/assets/facebook.svg" alt="Facebook")
                    a(href="instagram.com")
                        img(src="@/assets/instagram.svg" alt="Instagram")
                    a(href="pinterest.com")
                        img(src="@/assets/pinterest.svg" alt="Pinterest")
            .footer__credits © 2018 Hogash Studio. All rights reserved.
</template>

<style lang="sass" scoped>
    .footer
        background: linear-gradient(90deg, #07020e80 0%, #19083580 100%)
        &__wrap
            padding:
                top: 50px
                bottom: 40px
        &__top
            display: grid
            align-items: center
            justify-content: center
            grid:
                template-columns: repeat(3, auto)
                gap: 110px
        &__list
            display: flex
        &__item
            margin-right: 40px
            &:last-child
                margin-right: 0
        &__link
            font-size: 16px
            color: #605c6a
            line-height: 30px
            transition: color .3s
            &:hover
                color: #fff
        &__socials a
            margin-right: 30px
            &:last-child
                margin-right: 0
        &__credits
            padding-top: 58px
            font-size: 12px
            text-align: center

    @media(max-width: 1200px)
        .footer
            &__top
                grid-gap: 50px
            &__item
                margin-right: 20px

    @media(max-width: 960px)
        .footer
            &__wrap
                padding-top: 20px
                padding-bottom: 30px
            &__top
                grid-template-columns: repeat(3, 1fr)
                grid-gap: 0
                text-align: center
            &__list
                flex-direction: column
                align-items: center
            &__item
                margin-right: 0
            &__credits
                padding-top: 20px
    @media(max-width: 640px)
        .footer
            &__top
                grid-template-columns: auto
                grid-gap: 20px
            &__link
                line-height: 20px
</style>
