<template>
  <form @submit.prevent="handleSubmit">
      <label >Nom complet:</label>
      <input type="text" required v-model="fullname">


      <label >Carte d'identité nationale</label>
      <input type="text" required v-model="cin">

      <label >Numero de téléphone:</label>
      <input type="text" required v-model="phonenumber">
      
      <div class="submit">
          <button>Envoyer</button>
      </div>


      

  </form>
  
  
</template>

<script>
export default {
    data() {
        return {
            fullname: '',
            phonenumber: '',
            cin: ''




        }
    },
    methods: {
    handleSubmit() {
        console.log('form submitted')
    }
    }

}
</script>

<style>
form{
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label{
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input{
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}
button {
    background: #0b6dff;
    border: 0;
    padding:10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
}
.submit {
    text-align: center;
}


</style>