<template>
    <article class='modal-wrap'>
        <div class='container'>
            <span class='icon-close' @click="$emit('closeModal', {email})"/>
            <h1>Вход</h1>
            <form>
              <label class='label'>
                  Email
                  <input class='input' type='email' v-model='email' @keyup.enter="handleKeyUp">
              </label>
              <p>{{reverse}}</p>
              <label class='label'>
                  Пароль
                  <input class='input' type='password'>
                  <!--<button class='button' type="submit" @click.prevent="handleButtonClick">Войти</button>-->
                  <button class='button' type="submit" @click="$router.push('/about')">Войти</button>
              </label>
            </form>
        </div>
    </article>
</template>

<script>
    export default {
        data() {
          return {
            email: '',
            testData: 'hello',
          }
        },

        methods: {
          handleButtonClick(event) {
            console.log('clicked');
          },
          handleKeyUp(event){
            console.log(event, 'key pressed');
          }
        },
        computed: {
          reverse(){
            return this.email.split('').reverse().join('');
          }
        }
    }
</script>

<style scoped>
.modal-wrap{
    width: 100%;
    height: 100vh;
    position: absolute;
    top: 0;
    left: 0;
    background: rgba(0,0,0,.5);
}
.container{
    width: 400px;
    padding: 30px;
    margin: 0 auto;
    position: relative;
    top: 50%;
    transform: translateY(-50%);
    background: white;
    border-radius: 14px;
    cursor: pointer;
}
.icon-close{
    width: 20px;
    height: 20px;
    position: absolute;
    top: -25px;
    right: -25px;
}
.icon-close::before{
    width: 100%;
    content: '';
    border-bottom: 2px solid white;
    transform: rotate(45deg);
    position: absolute;
    top: 50%;
    left: 0;
}

.icon-close::after{
    width: 100%;
    content: '';
    border-bottom: 2px solid white;
    transform: rotate(-45deg);
    position: absolute;
    top: 50%;
    left: 0;
}
.label{
    display: flex;
    flex-direction: column;
    margin: 15px 0;
}
.input{
    padding: 7px 15px;
}
.button{
    width: 100%;
    margin-top: 35px;
    padding: 10px 20px;
    border: 1px solid black;
    background: white;
    color: black;
    cursor: pointer;
    border-radius: 30px;
    transition: .3s;
}
.button:hover{
    background: black;
    color: white;
    transition: .3s;
}

</style>
