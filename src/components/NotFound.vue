<template>
    <div role="tablist" class="mt-4">
        <b-card no-body class="mb-1" style="width:50%; margin-left:25%">
            <b-card-header header-tag="header" class="p-1" role="tab">
                <b-button block v-b-toggle.accordion-2 variant="danger"><strong>404</strong></b-button>
            </b-card-header>

            <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                <b-card-body style="text-align:center">
                <b-card-text><strong>{{ text }}</strong></b-card-text>
                <b-button href="/"><strong>Come back Home...</strong></b-button>
                </b-card-body>
            </b-collapse>
        </b-card>
  </div>
</template>

<script>
    export default {
        name: 'NotFound',
        data() {
            return {
               text: 'Are You Lost, Baby Girl??'
            }
        },
    }
</script>

