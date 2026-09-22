<script setup>

</script>

<template>
    <v-contanier max-width="100%">
        <v-row>
            <v-col>
                <v-carousel cycle hide-delimiters>
                    <v-carousel-item src="/images/carousel1.jpg" cover></v-carousel-item>
                    <v-carousel-item src="/images/carousel2.jpg" cover></v-carousel-item>
                    <v-carousel-item src="/images/carousel3.jpg" cover></v-carousel-item>
                    <v-carousel-item src="/images/carousel4.jpg" cover></v-carousel-item>
                </v-carousel>
            </v-col>
        </v-row>
    </v-contanier>

    <!--About us -->
    <v-container max-width="100%">
        <v-row>
            <v-col>
                <v-card align="center">
                    <v-card-title>Welcome to Faras Hospital</v-card-title>
                    <v-card-text class="text-body-large">Welcome to Faras Hospital, a premier Level 5 healthcare institution dedicated to delivering advanced clinical care and medical excellence. Our state-of-the-art facility features modern diagnostic technologies and comprehensive specialized departments, ensuring every patient receives world-class, compassionate treatment tailored to their needs.</v-card-text>
                    <v-card-text class="text-body-large">As a leading referral hospital, our team of expert specialists and dedicated medical staff is committed to elevating community wellness. We combine cutting-edge technology with patient-centered care, providing 24/7 emergency services, specialized surgical interventions, and compassionate recovery support to keep you healthy.</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!--clinic-->
    <v-container>
        <v-row>
            <v-col md="3">
                <v-card width="100%">
                    <v-img src="/clinic/clinic1.jpg" cover></v-img>
                    <v-card-title>Laboratory Services</v-card-title>
                    <v-card-text>Faras Services</v-card-text>
                    <v-btn>Learn More</v-btn>
                </v-card>
            </v-col>
              <v-col md="3">
                <v-card width="100%">
                    <v-img src="/clinic/clinic2.jpg" cover></v-img>
                    <v-card-title>Laboratory Services</v-card-title>
                    <v-card-text>Faras Services</v-card-text>
                    <v-btn>Learn More</v-btn>
                </v-card>
            </v-col>
             <v-col md="3">
                <v-card width="100%">
                    <v-img src="/clinic/clinic3.jpg" cover></v-img>
                    <v-card-title>Laboratory Services</v-card-title>
                    <v-card-text>Faras Services</v-card-text>
                    <v-btn>Learn More</v-btn>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card width="100%">
                    <v-img src="/clinic/clinic4.jpg" cover></v-img>
                    <v-card-title>Laboratory Services</v-card-title>
                    <v-card-text>Faras Services</v-card-text>
                    <v-btn>Learn More</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!--footer-->
    <v-container max-width="100%" class="mt-6 bg-secondary">
          <v-row>
        <v-col md="4">
            <v-card height="300px" color="secondary" flat>
            <v-card-title>Subscribe to our mailing page</v-card-title>
            <v-card-text>Get the latest news, health tips, and hospital updates delivered to your email. </v-card-text>
            <v-text-field v-model="inputValue" label="Email address" outlined class="ma-4">
                <template v-slot:append-inner>
                    <v-btn color="primary">Subcribe</v-btn>
                </template>
            </v-text-field>
            <div class="text centre">
                <p>Follow us on:</p>
                <v-icon icon="mdi-instagram"></v-icon>
                <v-icon icon="mdi-twitter"></v-icon>
                <v-icon icon="mdi-facebook"></v-icon>
            </div>
            </v-card>
        </v-col>

        <v-col md="4">
            <v-card height="300px" color="secondary" flat>
                <v-card-title>contact information</v-card-title>
                <v-card-text>
                    <p>
                        <v-icon icon="mdi-map-marker-radius-outline"></v-icon>
                        The Faras Hospital
                    </p>
                    <p> 123, Main Street Madaraka, Nairobi </p>
                    <p>
                        <v-icon icon="mdi-email-outline"></v-icon>
                        info@farashospital.com 
                    </p>
                </v-card-text>
            </v-card>
        </v-col>

        <v-col>
            <v-card height="300px" color="secondary" >
                <v-card-title>Quick Links</v-card-title>
                <v-card-text>About Us</v-card-text>
                <v-card-text>Clinics</v-card-text>
                <v-card-text>Find a Doctor</v-card-text>
                <v-card-text>News and Events</v-card-text>
            </v-card>
        </v-col>
    </v-row>
    </v-container>
</template>
    