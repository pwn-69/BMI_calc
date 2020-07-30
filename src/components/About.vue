<template>
    <div>
        <div>
            <b-navbar toggleable="lg" type="dark" variant="dark">
                <b-dropdown href="" text="BMI">
                    <b-dropdown-item href="#/">Metric(Default)</b-dropdown-item>
                    <b-dropdown-item href="#/imp">Imperial</b-dropdown-item>
                    <div class="dropdown-divider"></div>
                    <b-dropdown-item href="#/help">Need Help?</b-dropdown-item>
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
                <b-card bg-variant="dark" text-variant="white" style="width:50%" class="ml-4">
                    <b-card-header>
                         <b-avatar size="6rem">
                             <img src="../assets/pwn.jpg" alt="me" style="width:130px">
                         </b-avatar>
                    </b-card-header>
                    <b-card-text>
                        <p><strong>Phyo Wai Nyunt</strong></p>
                        <p><strong>Third Year Computer Science Student</strong></p>
                    </b-card-text>
                    <br>
                    <b-card-text>
                    <p><strong>Get in touch...</strong></p>
                    <b-button bg-variant="outline-white" href="https://www.linkedin.com/in/phyo-wai-nyunt-56ba55195/"><b-icon icon="bell"></b-icon></b-button>
                    </b-card-text>
                </b-card>
            </div>
    </div>
</template>

<script>
    export default {
        name: 'About'
    }
</script>
