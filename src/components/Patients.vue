<script setup>
import {ref} from 'vue'
import { id } from 'vuetify/locale'

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

//models
const firstName = ref(null)
const lastName = ref(null)
const email = ref(null)
const phone = ref(null)
const residence = ref(null)
const nationalId = ref(null)
const dob = ref(null)

function handleAddPatient(){
    const data = {
        id: 5,
        firstName: firstName.value,
        lastName: lastName.value,
        email: email.value,
        phone: phone.value,
        residence: residence.value,
        nationalId: nationalId.value,
        dob: dob.value,
    }
    patients.push(data)
    showAddDialog.value= false
    console.log(patients)

}

</script>

<template>
    <v-container class="mt-6"> 
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
                <v-table class="border" sripped="even">
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
                                <v-btn color="primary" size="small" to="/viewpatient"> <v-icon icon=""
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
    <v-dialog v-model="showAddDialog" max-width="50%">
        <v-form>
            <v-card class="pa-4">
                <v-row>
                <v-card-text>Add Patient</v-card-text>
                <v-spacer></v-spacer>
                <v-btn class="ma-2" color="primary" icon="mdi-close" @click="showAddDialog = false"></v-btn>
                </v-row>
                    <v-divider class="mb-4" color="primary" opacity=".7" thickness="3" gradient></v-divider>
             <v-row>
                 <v-col md="6">
                <v-text-field label="First Name" variant="outlined" prepend-icon="mdi-account-badge" v-model="firstName"></v-text-field>
                </v-col>
                <v-col md="6">
                 <v-text-field label="Last Name" variant="outlined" prepend-icon="mdi-account-badge" v-model="lastName"></v-text-field>
                 </v-col>
             </v-row>
             <v-row>
                <v-col md="6">
                <v-text-field label="Email" variant="outlined" prepend-icon="mdi-email-fast-outline" v-model="email"></v-text-field>
                </v-col>
                <v-col md="6">
                 <v-text-field label="Phone" variant="outlined" prepend-icon="mdi-phone-outline" v-model="phone"></v-text-field>
                 </v-col>
            </v-row>
             <v-row>
                <v-col md="6"> 
                <v-text-field label="Residence" variant="outlined" prepend-icon="mdi-home-outline" v-model="residence"></v-text-field>
                </v-col>
                <v-col md="6">
                    <v-text-field label="National ID" variant="outlined" prepend-icon="mdi-id-card" v-model="nationalId"></v-text-field>
                 </v-col>
            </v-row>
             <v-row>
                <v-col md="6">
                <v-date-input label="Date Of Birth" prepend-icon="mdi-calendar-outline"></v-date-input>
                </v-col>
            </v-row>
                 <v-divider class="mb-4" color="primary" opacity=".7" thickness="3" gradient></v-divider>
                 <v-row>
                    <v-col>
                        <v-card-actions>
                            <v-btn color="primary" variant="outlined"><v-icon icon="mdi-close"></v-icon> Close</v-btn>
                            <v-spacer/>
                            <v-btn color="primary" variant="outlined" @click="handleAddPatient"><v-icon icon="mdi-content-save-outlined"></v-icon> Save</v-btn>
                        </v-card-actions>
                    </v-col>
                 </v-row>
            </v-card>
        </v-form>
    </v-dialog>
</template>