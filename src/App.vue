<template lang="pug">
    #app
        .container
            <Header />
            <Main />
            <Steps />
            <Preview />
            <Reviews />
            <Info />
            <Quotation />
            <Contact />
            <Footer />
</template>

<script>
    import Header from '@/components/Header'
    import Main from '@/components/Main'
    import Steps from '@/components/Steps'
    import Preview from '@/components/Preview'
    import Reviews from '@/components/Reviews'
    import Info from '@/components/Info'
    import Quotation from '@/components/Quotation'
    import Contact from '@/components/Contact'
    import Footer from '@/components/Footer'

    export default {
        name: 'App',
        components: {
            Header, Main, Steps, Preview, Reviews, Info, Quotation, Contact, Footer
        }
    }
</script>

<style lang="sass">
    @import url('https://fonts.googleapis.com/css?family=Montserrat:300,400,600,700&display=swap')

    *
        margin: 0
        padding: 0
    html
        scroll-behavior: smooth
    body
        overflow-wrap: break-word
        font-family: 'Montserrat'
        background: linear-gradient(270deg, rgba(31,52,99,1) 0%, rgba(27,31,73,1) 100%)
        color: #fff
    a
        text-decoration: none
    ul
        list-style-type: none
    .container
        max-width: 100%
        min-width: 320px
        background: url('./assets/bg.png') right 280px no-repeat
    .wrap
        max-width: 1300px
        min-width: 290px
        padding: 0 15px
        margin: 0 auto
    .button__gradient
        box-sizing: border-box
        padding: 23px 86px 25px 86px
        color: #fff
        background: linear-gradient(90deg, #05be9e 0%, #146ea7 100%)
        border: 0
        text-transform: uppercase
        font-size: 14px
        border-radius: 30px
        cursor: pointer
        letter-spacing: 0.02em
        transition: background .3s
        white-space: nowrap
        &:hover
            background: linear-gradient(90deg, darken(#05be9e, 10%) 0%, darken(#146ea7, 10%) 100%)
    .block__title
        font-size: 36px
        letter-spacing: 0.02em
        font-weight: 700
        text-align: center
        @media(max-width: 320px)
            font-size: 32px
    .block__subtitle
        font-size: 18px
        color: #8e819e
        font-weight: 300
        padding-top: 25px
        text-align: center
        @media(max-width: 960px)
            padding-top: 15px
        @media(max-width: 320px)
            font-size: 16px
    .circle__icon
        display: flex
        align-items: center
        justify-content: center
        position: relative
        margin: auto
        width: 180px
        height: 180px
        border-radius: 50%
        background: #16062a
</style>
