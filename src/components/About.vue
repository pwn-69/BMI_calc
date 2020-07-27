<template>
    <div>
        <div>
            <b-navbar toggleable="lg" type="dark" variant="dark">
                <b-dropdown href="" text="BMI">
                    <b-dropdown-item href="#/">Metric(Default)</b-dropdown-item>
                    <b-dropdown-item href="#/imp">Imperial</b-dropdown-item>
                </b-dropdown>

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item href="#/about">About</b-nav-item>
                </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
        <br>
        <div>
            <b-jumbotron  style="max-width: 50rem;">
                <template v-slot:header>Created By...</template>

                <template v-slot:lead>
                    Phyo Wai Nyunt
                </template>

                <hr class="my-4">

                <p>
                    Get in touch...
                </p>

                 <b-button variant="outline-dark" href="https://www.linkedin.com/in/phyo-wai-nyunt-56ba55195/"><b-icon icon="bell"></b-icon></b-button>
            </b-jumbotron>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'About'
    }
</script>
