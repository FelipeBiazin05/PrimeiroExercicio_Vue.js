<script setup>
import { reactive } from 'vue';

const nome = "Gian Souza"

const meuObj = {
  nome: "Gian",
  filmeFavorito: "Rocky"
}

function dizOla() {
  return `${nome} diz oi`
}

const enderecoDaImagemDoBatman = "data:image/jpeg;base64,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"
const enderecoDaImagemDoSuperman = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQl7SoGEkeaBeU0lZLk7DywwRESDzUVWWAvpg&s"

const botaoEstaDesabilitado = false;

const gostaDoBatman = false;
const gostaDoSuperman = false;

const estaAutorizado = false;

// let contador = 0;
const estado = reactive({
  contador: 0,
  email: '',
  saldo: 5000,
  transferindo: 0,
  nomes: ["Gian", "Paulo", "Luisa", "Monica"],
  nomeAInserir: '',
})

function incrementar() {
  estado.contador++;
}

function decrementar() {
  estado.contador--;
}

function alteraEmail(evento) {
  estado.email = evento.target.value;
}

function mostraSaldoFuturo() {
  const {saldo, transferindo} = estado;
  return saldo - transferindo;
}

function validaValorDaTransferencia() {
  const {saldo, transferindo} = estado;
  return saldo >= transferindo;
}

function cadastrarNome() {
  if (estado.nomeAInserir.length >= 3) {
    estado.nomes.push(estado.nomeAInserir)
  }else {
    alert("Digite mais caracteres")
  }
  console.log(estado)
}
</script>

<template>
  <h1>{{ dizOla() }}</h1>
  <img v-if="gostaDoBatman" :src="enderecoDaImagemDoBatman" alt="Imagem do Batman">
  <img v-else-if="gostaDoSuperman" :src="enderecoDaImagemDoSuperman" alt="Imagem do Superman">
  <h2 v-else>Não curte herois da DC</h2>

  <h1 v-if="estaAutorizado">Bem Vindo</h1>
  <h1 v-else>Não possui acesso</h1>

  <button :disabled="botaoEstaDesabilitado">Enviar mensagem</button>

  <br>
  <hr>

  {{ estado.contador }}

  <button @click="incrementar"type="button">+</button>
  <button @click="decrementar" type="button">-</button>

  <br>
  <hr>

  {{ estado.email }}
  <input type="email" @keyup="alteraEmail">

  <br>
  <hr>

  Saldo: {{ estado.saldo }} <br>
  Transferindo: {{ estado.transferindo }} <br>
  Saldo depois da transfêrencia: {{ mostraSaldoFuturo() }} <br>
  <input class="campo" :class="{ invalido: !validaValorDaTransferencia}" @keyup="evento => estado.transferindo = evento.target.value" type="number" placeholder="Quantia para transferir">
  <button v-if="validaValorDaTransferencia()" >Transferir</button>
  <span v-else>Valor maior que o saldo</span>

  <br>
  <hr>

  <ul>
    <li v-for="nome in estado.nomes">
      {{ nome }}
    </li>
  </ul>
  <input @keyup="evento => estado.nomeAInserir = evento.target.value" type="text" placeholder="Digite um novo nome">
  <button @click="cadastrarNome" type="button">Cadastrar nome</button>

  <h3 v-for="nome in estado.nomes">{{ nome }}</h3>
</template>

<style scoped>
  img {
    max-width: 200px;
  }

  .invalido {
    outline-color: red;
    border-color: red;
  }

  .campo {
    border: 2px solid #000;
  }
</style>
