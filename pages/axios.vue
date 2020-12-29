<template>
  <section class="container">
    <div>
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    </div>
  </section>
</template>

<script>
import firebase from "firebase";


export default {
  data: function(){
    return {
      title:'Auth',
      message: 'this is message.',
    };
  },
  created:function(){
    var config = {
        apiKey: "AIzaSyBV3Wqnb7PMbSFPT4oaanRpXnognbuFU5U",
        authDomain: "app-ikdysk.firebaseapp.com",
        databaseURL: "https://app-ikdysk-default-rtdb.firebaseio.com",
        projectId: "app-ikdysk",
        storageBucket: "app-ikdysk.appspot.com",
        messagingSenderId: "674052188721",
        appId: "1:674052188721:web:313cf70a56c75b3f95c310",
        measurementId: "G-7KKVVBH1H4"
    };
    firebase.initializeApp(config);


    var provider = new firebase.auth.GoogleAuthProvider();
    var self = this;
    firebase.auth().signInWithPopup(provider)
      .then(function(result) {
        self.message = result.user.displayName + ', ' 
          + result.user.email;
      });
  },
};
</script>


<style>
tr th {
    width:150px;
    background-color: darkblue;
    color:white;
    font-size:16pt;
}
tr td {
    padding:5px 10px;
    background-color:#eef;
    font-size:14pt;
}
</style>