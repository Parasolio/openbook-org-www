<template>
    <div class="animated fadeIn">
        <section class="hero is-large has-border-bottom-gray">
            <div class="hero-body">
                <div class="container">
                    <div class="columns">
                        <div class="column">
                            <div class="columns is-centered has-padding-top-2x-mobile">
                                <div class="column is-narrow">
                                    <h1 class="subtitle is-size-3 has-text-grey-light has-text-centered-mobile">
                                        {{ $t('contact_us.title') }}
                                    </h1>
                                    <h2 class="title is-size-2 contact-text has-text-centered-mobile">
                                        {{ $t('contact_us.subtitle') }}
                                    </h2>
                                </div>
                            </div>
                        </div>
                        <div class="column">
                            <div class="columns is-centered is-vcentered contact-us-header-mailbox is-mobile">
                                <div class="column is-narrow">
                                    <ob-mailbox/>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="section">
            <div class="container">
                <div class="columns contact">
                    <div class="column is-4-tablet">
                        <div class="columns is-centered is-mobile">
                            <div class="column contact-information">
                                <div class="content">
                                    <h4>{{ $t('contact_us.info') }}</h4>
                                    <ob-address/>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="column">
                        <div class="columns is-centered is-mobile">
                            <div class="column contact-message padding-bottom-2x-mobile">
                                <div class="content">
                                    <h4 class="padding-bottom-2x">
                                        {{ $t('contact_us.message') }}
                                    </h4>
                                    <ob-message/>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<style lang="scss">

    .contact-text{
        @media (min-width: 768px){
            max-width:400px;
        }
    }

    .contact-us-header-envelope {
        @media(max-width: 768px) {
            padding-top: 1rem;
        }
    }

    .contact {
        @media(max-width: 768px) {
            display: flex;
            flex-direction: column-reverse;
        }
    }

    .contact-information {
        max-width: 250px;
    }

    .contact-message {
        max-width: 750px;
    }

</style>

<script>
    import ObMailbox from "./components/mailbox";
    import ObAddress from "./components/address";
    import ObMessage from "./components/message";

    export default {
        components: {
            ObMessage,
            ObAddress,
            ObMailbox
        }

    }
</script>
