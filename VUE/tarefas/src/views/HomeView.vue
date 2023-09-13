<template>
  <Div class="login-tudo">
      <div class="capa">
          

      </div>
      <div class="input-login">
          <h1>Login</h1>
          <p>Endereço de E-Mail</p>
          <div class="input-group input-group-sm mb-3">
              <input type="text" placeholder="email@email.com" class="form-control"
                  aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm">
          </div>
          <P>Senha</P>
          
          <div class="input-group input-group-sm mb-3">
              <input type="text" placeholder="*******" class="form-control"
                  aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm">
          </div>
          <div class="d-flex justify-content-between">
          <RouterLink to="/cadastrar" class="text-decoration-none">Não tem conta?!</RouterLink>
          <button type="button" class="btn btn-outline-secondary"><RouterLink to="/tarefas" class="text-decoration-none">Acesse</RouterLink></button>
          </div>
      </div>
  </Div>
</template>

<script>
export default {

}
</script>


<style scoped>
*{
  font-family: Arial, Helvetica, sans-serif;
  padding: 25px;
  padding-top: 30px;
  margin: 0;
  
 
  
}
input-login{
  width: 60%;
  display: flex;
  justify-content: space-between;
  
  
}
.login-tudo{
  height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.capa{
  background-image: url(https://th.bing.com/th/id/OIP.EkCb-DCvBCV81RMksIESuAHaLj?pid=ImgDet&rs=1);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: right  center;}

</style>
