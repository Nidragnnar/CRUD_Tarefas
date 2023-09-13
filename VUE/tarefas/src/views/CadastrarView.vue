<template>
    <div class="cadastrar-tudo">
        <div class="input-cadastrar">
            <h1>Cadastre-se</h1>
            <p>Nome</p>
            <div class="input-group input-group-sm mb-3">
                <input type="text" placeholder="Nome Completo" class="form-control" aria-label="Sizing example input"
                aria-describedby="inputGroup-sizing-sm">
                
                
            </div>
            <p>E-mail</p>
            <div class="input-group input-group-sm mb-3">
                <input type="text" placeholder="Adicione seu E-Mail" class="form-control" aria-label="Sizing example input"
                aria-describedby="inputGroup-sizing-sm">
                
                
            </div>
            <p>Senha</p>
            <div class="input-group input-group-sm mb-3">
                <input type="text" placeholder="Senha para Cadastrar" class="form-control" aria-label="Sizing example input"
                aria-describedby="inputGroup-sizing-sm">
                
                
            </div>
            <div class="d-flex justify-content-between">
                <RouterLink to="/cadastrar" class="text-decoration-none" ><RouterLink to="/" class="text-decoration-none">Já tem conta?</RouterLink></RouterLink> 
                <button type="button" class="btn btn-outline-secondary"><RouterLink to="/tarefas" class="text-decoration-none">Acesse</RouterLink></button>
            </div>
        </div>
        <div class="capa"></div>
    </div>   
</template>

<script>
export default {

}


</script>

<style scoped>
*{
    font-family: Arial, Helvetica, sans-serif;
    padding: 20px;
    padding-top: 30px;
    margin: 0;
    
   
    
}
input-cadastrar{
    width: 60%;
    display: flex;
    justify-content: space-between;
    
    
}
.cadastrar-tudo{
    height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.capa{
    background-image: url(https://th.bing.com/th/id/OIP.EkCb-DCvBCV81RMksIESuAHaLj?pid=ImgDet&rs=1);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: left  center;}
    </style>