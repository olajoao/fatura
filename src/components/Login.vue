<template>
  <div>
    <section class="login">
      <div class="container-fluid">
        <div class="row">
          <div class="login__area col-12 col-sm-8 mx-auto col-md-5 col-lg-4 col-xl-3 min-vh-100 max-vw-100">
            <div class="row h-100 flex-column justify-content-between">
              <div class="col-12">
                <h1 class="logo text__color--dark fw-bold mt-4">LOGO</h1>
              </div>
              <div class="col-12">
                <h2 class="text__color--dark fs-3 mb-5">Login</h2>
                <h3 class="text__color--dark fs-5 mb-5">Relatório de Faturas</h3>
                <form class="form">
                  <div class="login__group mb-5 position-relative">
                    <svg class="login__icon position-absolute" style="width:20px;height:20px" viewBox="0 0 24 24">
                      <path fill="currentColor" d="M12,4A4,4 0 0,1 16,8A4,4 0 0,1 12,12A4,4 0 0,1 8,8A4,4 0 0,1 12,4M12,14C16.42,14 20,15.79 20,18V20H4V18C4,15.79 7.58,14 12,14Z" />
                    </svg>
                    <input type="text" class="login__input rounded-0 w-100" id="cliente" placeholder=" ">
                    <label for="cliente" class="login__label position-absolute">Cliente</label>
                  </div>
                  <div class="login__group mb-3 position-relative">
                    <svg class="login__icon position-absolute" style="width:20px;height:20px" viewBox="0 0 24 24">
                      <path fill="currentColor" d="M12,17C10.89,17 10,16.1 10,15C10,13.89 10.89,13 12,13A2,2 0 0,1 14,15A2,2 0 0,1 12,17M18,20V10H6V20H18M18,8A2,2 0 0,1 20,10V20A2,2 0 0,1 18,22H6C4.89,22 4,21.1 4,20V10C4,8.89 4.89,8 6,8H7V6A5,5 0 0,1 12,1A5,5 0 0,1 17,6V8H18M12,3A3,3 0 0,0 9,6V8H15V6A3,3 0 0,0 12,3Z" />
                    </svg>                  
                    <input type="password" class="login__input rounded-0 w-100" id="senha" placeholder=" ">
                    <label for="senha" class="login__label position-absolute">Senha</label>
                  </div>
                  <input class="mt-4 w-100 py-2 fw-bold bg__color--dark text-white border-0" type="submit" value="Acessar">
                </form>
              </div>
              <div class="col-12 mb-4">
                <small class="text__color--dark">
                  Todos os direitos reservados - MaxTech
                </small>
              </div>

            </div>
          </div>
          <div class="background d-none d-md-block col-md-7 col-lg-8 col-xl-9 min-vh-100 max-vw-100">
            
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>

export default {
  setup() {
    
    const state = {
      name: 'Joao'
    }
    return state
  }
}
</script>

<style scoped>
  .background {
    background-image: url('../assets/bg.jpg');
    background-position: top center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  
  .login__area { 
    padding: 0 2.5rem;
  }

  .login__label {
    font-size:0.9rem;
    left: 2rem;
    opacity: 0.7;
    transition: all 0.3s ease;
  }

  .login__input {
    border: 0;
    border-bottom: 1px solid #21232990;
    outline: none;
    padding-left: 2rem;
  }

  .login__icon {
    left: 0.2rem;
    opacity: 0.7;
  }

  /* form login animations */
  
  /* 
  * check if the input is focused, if true
  * move the label to the top 
  */
  .login__input:focus ~ .login__label {
    transform: scale(1.1) translate(-1.5rem , -1.5rem);
  }

  /* 
  * check if the input is not empty, if true
  * maintain the label on top 
  */
  .login__input:not(:placeholder-shown) ~ .login__label {
    transform: scale(1.1) translate(-1.5rem , -1.5rem);
  }
  /* end form login animations */
</style>