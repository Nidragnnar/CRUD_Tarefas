<template>
  <div>
    <div class="nav">
      <ul class="nav nav-underline px-5">
        <li class="nav-item">
          <a class="nav-link active px-5" aria-current="page" href="#">👌</a>
        </li>
        <li class="nav-item px-5">
          <a class="nav-link px-5" href="#"></a>
        </li>
        <li class="nav-item px-5">
          <a class="nav-link px-5" href="#"></a>
        </li>
        <li class="nav-item px-5">
          <a class="nav-link disabled px-5" aria-disabled="true"></a>
        </li>
        <li class="nav-item px-5">
          <a class="nav-link px-5" href="#"
            ><img
              class="icon"
              src="https://image.freepik.com/free-icon/interrogation-mark-in-a-circle_318-9651.jpg"
              alt="Sobre"
          /></a>
        </li>
        <li class="nav-item px-5">
          <a class="nav-link px-5" href="#"
            ><img
              class="icon"
              src="https://th.bing.com/th/id/OIP.UBB7tvACM31xW9ZJ6xOfSAHaHv?pid=ImgDet&rs=1"
              alt="Notificação"
          /></a>
        </li>

        <li class="nav-item px-5">
          <a class="nav-link px-5" href="#"
            ><img
              class="icon"
              src="https://www.pngarts.com/files/3/Plus-Symbol-Transparent-Images.png"
              alt="Criar"
          /></a>
        </li>
      </ul>
    </div>
    <div>
      <h1>Lista de Usuários</h1>
      <ul>
        <li v-for="item in tarefa" :key="item.id">
          {{ item.titulo }}
        </li>
      </ul>
    </div>
    <div>
    <p v-if="tarefa && tarefa.id">ID da Tarefa: {{ tarefa.id }}</p>
    <p v-else>Os dados da tarefa ainda não foram carregados.</p>
    </div>
    <div>
    <p v-if="tarefa">ID da Tarefa: {{ tarefa.id }}</p>
    <p v-else>A tarefa não foi carregada ou não existe.</p>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tarefa: [{ id: null}, {titulo: ''}, {data_vencimento: '' }], // Armazenar os dados da API aqui
    };
  },
  created() {
    // Chamada à API usando fetch no ciclo de vida created
    fetch("http://localhost:8080/api/tarefas/")
      .then((response) => response.json())
      .then((data) => {
        this.tarefa = data; // Preenche a lista com os dados da API
      })
      .catch((error) => {
        console.error("Erro ao buscar dados da API:", error);
      });
  },
};
</script>

<style scoped>
.nav {
  padding: 5px;
  padding-right: 20px;
  padding-left: 20px;
}

.icon {
  width: 30px;
  margin-left: 10px;
}
</style>
