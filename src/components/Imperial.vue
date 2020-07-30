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
        <div class="mt-4">
            <b-card bg-variant="light">
                <b-form-group
                label-cols-lg="3"
                label="BMI input"
                label-size="lg"
                label-class="font-weight-bold pt-0"
                class="mb-0"
                >
                <b-form-group
                    label-cols-sm="3"
                    label="Feet :"
                    label-align-sm="right"
                    label-for="nested-height"
                >
                    <b-form-input id="nested-height" v-model="feet"></b-form-input>
                </b-form-group>

                 <b-form-group
                    label-cols-sm="3"
                    label="Inches :"
                    label-align-sm="right"
                    label-for="nested-height"
                >
                    <b-form-input id="nested-height" v-model="inches"></b-form-input>
                </b-form-group>
                <br>

                <b-form-group
                    label-cols-sm="3"
                    label="Weight(lb):"
                    label-align-sm="right"
                    label-for="nested-weight"
                >
                    <b-form-input id="nested-weight" v-model="weight"></b-form-input>
                </b-form-group>
                </b-form-group>
            </b-card>
        </div>
        <br>
        <div>
            <b-jumbotron lead="Your BMI is :">
                <p><strong>{{bmiCalculation}}</strong></p> 
            </b-jumbotron>
        </div>
    </div>
   
</template>

<script>
    export default {
        name : 'Imperial',
        data() {
            return {
                height: null,
                weight: null
            }
        },
        computed: {
            bmiCalculation: function() {
            var weight = parseInt(this.weight);
            var feet = parseInt(this.feet);
            var inches = parseInt(this.inches);

            var inch = (feet * 12) + inches;

            var bmi = (weight / (inch*inch)) * 703;

            if(bmi < 18.5) {
                return 'Underweight: ' + bmi.toFixed(2) + 'kg/m2';
            }
            else if (bmi >=18.5 && bmi <24.9 ) {
                return 'Nomral: ' + bmi.toFixed(2) + 'kg/m2';
            }
            else if (bmi >=25.0 && 29.9 ) {
                return 'Overweight: ' + bmi.toFixed(2) + 'kg/m2';
            }
            else if (bmi >=30 ) {
                return 'Obesity: ' + bmi.toFixed(2) + 'kg/m2';
            }
            }
        }
    }
</script>
