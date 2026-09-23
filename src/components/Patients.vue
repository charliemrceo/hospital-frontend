<script setup>
import {ref} from 'vue'

const patients = [
    {
        id: 1,
        firstName: "John",
        lastName: "Doe",
        email: "johndoe@gmail.com",
        Phone: "077870975",
        residence: "123, hunter Street",
        nationalId: "89706523",
        dob: "1977-14-07",
    },
    {
        
        id: 2,
        firstName: "Shane",
        lastName: "Wilson",
        email: "wilsonshane@gmail.com",
        Phone: "074567943",
        residence: "325, Odinga Street",
        nationalId: "67897065",
        dob: "1976-05-08",
         
    },
     {
        
        id: 3,
        firstName: "Patrick",
        lastName: "Jane",
        email: "patrickjane@gmail.com",
        Phone: "0756438967",
        residence: "123, Main Street",
        nationalId: "98076574",
        dob: "1976-06-05",
         
    },
    {
        
        id: 4,
        firstName: "Peter",
        lastName: "John",
        email: "johnpeter@gmail.com",
        Phone: "0728494766",
        residence: "557, Konja Street",
        nationalId: "35875609",
        dob: "1987-03-07",
         
    }
]

const showAddDialog = ref(false)

</script>

<template>
    <v-container>
        <v-row>
            <v-col md="10">
                <h1>Patients</h1>
            </v-col>
            <v-col md="2">
                <v-btn class="ma-2" color="primary" icon="mdi-plus" @click="showAddDialog = true"></v-btn>
            </v-col>
        </v-row>
    
        <v-row>
            <v-col>
                <v-table class="borde r">
                    <thead>
                        <tr>
                        <th>Name</th>
                        <th>Phone</th>
                        <th>Email</th>
                        <th>Residence</th>
                        <th>National ID</th>
                        <th>Date Of Birth</th>
                        <th>Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item in patients">
                            <td>{{ item.firstName + " " + item.lastName }}</td>
                            <td>{{ item.Phone }}</td>
                            <td>{{ item.email }}</td>
                            <td>{{ item.residence }}</td>
                            <td>{{ item.nationalId }}</td>
                            <td>{{ item.dob }}</td>
                            <td>
                                <v-btn color="primary" size="small">
                                    <v-icon> icon="mdi-eye"</v-icon>
                                    View
                                </v-btn>
                            </td>
                        </tr>
                    </tbody>
                </v-table>
            </v-col>
        </v-row>
    </v-container>
    <!--Add patients -->
    <v-dialog v-model="showAddDialog" max-width="600px">
        <v-from>
            <v-card>
                <v-row>
                <v-card-text>Add Patient</v-card-text>
                <v-spacer></v-spacer>
                <v-btn class="ma-2" color="primary" icon="mdi-close" @click="showAddDialog = false"></v-btn>
                </v-row>

             <v-row>
                 <v-col md="6">
                <v-text-field label="First Name"></v-text-field>
                </v-col>
                <v-col md="6">
                 <v-text-field label="Last Name"></v-text-field>
                 </v-col>
             </v-row>
             <v-row>
                <v-col md="6">
                <v-text-field label="Email"></v-text-field>
                </v-col>
                <v-col md="6">
                 <v-text-field label="Phone"></v-text-field>
                 </v-col>
            </v-row>
             <v-row>
                <v-col md="6">
                <v-text-field label="Residence"></v-text-field>
                </v-col>
                <v-col md="6">
                 <v-text-field label="National ID"></v-text-field>
                 </v-col>
            </v-row>
             <v-row>
                <v-col md="6">
                <v-text-field label="Date Of Birth"></v-text-field>
                </v-col>
            </v-row>

            </v-card>
        </v-from>
    </v-dialog>
</template>