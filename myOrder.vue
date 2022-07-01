

<script setup>
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
//import { initializeApp } from 'firebase/firestore';
import { getFirestore,setDoc,doc } from 'firebase/firestore';
import { ref } from 'vue';
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
const firebaseConfig = {
  apiKey: "AIzaSyBp_fspW7z6-_F652TqkPqSfRF74HQn4BY",
  authDomain: "vuefirebase-58bc4.firebaseapp.com",
  projectId: "vuefirebase-58bc4",
  storageBucket: "vuefirebase-58bc4.appspot.com",
  messagingSenderId: "908192511283",
  appId: "1:908192511283:web:03f3de1db16043d0347a46"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
//
const db=getFirestore(app);
const no=ref('');
const name=ref('');
const price=ref(0);
const qty=ref(0);

const setData=async()=>{
  await setDoc(doc(db,'product',no.value),{
    name:name.value,
    price:price.value,
    qty:qty.value
  }).then(function(){
    console.log('OKOKOKOKOKOK');
  })
}
</script>

<template>
<div>
  <input type="text" v-model='no'/>
  <input type="text" v-model='name'/>
  <input type="number" v-model='price'/>
  <input type="number" v-model='qty'/>
  <p>{{no}}</p>
  <p>{{name}}</p>
  <p>{{price}}</p>
  <p>{{qty}}</p>
  <button v-on:click="setData">ORDER！！！！</button>
</div>
</template>