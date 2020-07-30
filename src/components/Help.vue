<template>
        <div>
            <b-navbar toggleable="lg" type="dark" variant="dark">
                <b-dropdown text="BMI">
                    <b-dropdown-item href="#/" >Metric(Default)</b-dropdown-item>
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
            <b-card-group>
                <b-card title="Chart" img-alt="Image">
                    <b-img :src="image1" fluid thumbnail></b-img>
                        <b-card-text>
                        </b-card-text>
                        <template v-slot:footer>
                            <small class="text-muted">&copy; 2020 PWN</small>
                        </template>
                </b-card>

                <b-card title="Men" img-alt="Image">
                    <b-img :src="image2" fluid thumbnail></b-img>
                        <b-card-text>
                        </b-card-text>
                        <template v-slot:footer>
                            <small class="text-muted">&copy; 2020 PWN</small>
                        </template>
                </b-card>

                <b-card title="Women" img-alt="Image">
                    <b-img :src="image3" fluid thumbnail></b-img>
                        <b-card-text>
                        </b-card-text>
                        <template v-slot:footer>
                            <small class="text-muted">&copy; 2020 PWN</small>
                        </template>
                </b-card>            
            </b-card-group>    
        </div>

</template>

<script>
    export default {
        name: 'Help',
        data() {
            return {
                image1: require('../assets/bmi_chart.jpg'),
                image2: require('../assets/bmi_1.png'),
                image3: require('../assets/bmi_2.jpg')
            }
        },
    }
</script>