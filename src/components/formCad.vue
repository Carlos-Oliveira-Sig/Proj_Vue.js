<template>
  <div class="container">
    <div class="card">
    <h1 id="title"> Cadastrar </h1>
    <form id="user-cad" @submit="createCadastro">
      <div class="input-container">
        <label for="nome">Nome Completo</label>
        <input type="text" id="nome" name="name" v-model="nome">
      </div>
      <div class="input-container">
        <label for="telefone">Telefone</label>
        <input type="text" id="telefone" name="phone" v-model="telefone">
      </div>
      <div class="input-container">
        <label for="gitHub">GitHub</label>
        <input type="url" id="github" name="github" v-model="github">
      </div>
      <div class="input-container">
        <label for="email">E-mail</label>
        <input type="email" id="email" name="mail" v-model="email">
      </div>
      <div class="input-container">
        <label for="senha">Senha</label>
        <input type="password" id="senha" name="password" v-model="senha">
      </div>
      <div class="input-container">
        <label for="confirmesenha">Confirmar Senha</label>
        <input type="password" id="confirmesenha" name="confirmepassword" v-model="confirmesenha">
      </div>
      <div class="containerbtncad">
        <input type="submit" class="submit-btn" value="CADASTRAR">
      </div>
    </form>
    <h3 id="linklogin"> Já sou Cadastrado! </h3>
    </div>
  </div>    
</template>


<script>
export default {
  name: 'formCad',
  data() {
    return {
        nome: null,
        telefone: null,
        github: null,
        email: null,
        senha: null,
        confirmesenha: null
    }
  },
  methods: {
    async createCadastro(e) {

      e.preventDefault();

      const data = {
        nome: this.nome,
        telefone: this.telefone,
        github: this.github,
        email: this.email,
        senha: this.senha,
        confirmesenha: this.confirmarsenha
      }

      const dataJson = JSON.stringify(data)
      const req = await fetch("http://localhost:3000/registros", {
        method: "POST",
        headers: {"Content-Type":"application/json"},
        body: dataJson
      });

      const res = await req.json();
      console.log(res);
    }
  }
}
</script>

<style scope>
  .container {
    display: flex;
    justify-content: space-around;
    width: 460px;
    height: 100%; 
  }

  .card {
    display: flex;
    background-color: white;
    padding: 30px;
    border-radius: 2%;
    box-shadow: 3px 3px 3px 3px #00000060;
    height: 600px;
    width: 400px;
    flex-direction: column;
  }

  h1 {
    font-weight: bold;
    text-align: center;
    color: black;
  }

  .input-container{
    position: relative;
    padding-top: 13px;
    margin-top: 4%;
    margin-bottom: 4%;
  }

  .input-container input{
    width: 100%;
    padding: 10px 8px;
    display: inline-block;
    border: 0;
    border-bottom: 2px solid #07070720;
    background-color: transparent;
    outline: none;
    min-width: 180px;
    font-size: 16px;
    transition: all .3s ease-out;
  }

  .input-container input:focus{
    border-bottom: 3px solid #07070760;
  }

  .input-container label{
    color: #07070760;
    pointer-events: none;
    position: absolute;
    top: 0;
    left: 0;
    margin-top: 13px;
    transition: all .3s ease-out;
  }

.input-container input:focus + label {
  font-size: 8px;
  margin-top: 0;
  color: #07070740;
}

.containerbtncad input {
  background-color: green;
  border-radius: 12px;
  border-color: green;
  width: 100%;
  padding: 10px;
  font-weight: bold;
  font-size: 12pt;
  color:white;
  border-style: solid;
  margin-top: 16px;
  cursor: pointer;
  outline: none;
  transition: all .4s ease-out;
}

.containerbtncad input:hover {
  background-color: white;
  color: green
}

  h3 {
    text-align: center;
    margin-top: 8px;
    color: #07070760;
    font-size: 14pt;
  }

  h3:hover {
    cursor: pointer;
    color: #07070790;
  }

</style>
