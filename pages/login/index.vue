<template>
    
</template>

<script>


export default {
   data(){
  return {
        email: null,
        senha: null
    }
   },
    methods: {
        async login(){
            try {
                await this.$auth.loginWith("local",{
                    data: {
                        email: this.email,
                        senha: this.senha
                    }
                });
                this.$router.push("/");
            } catch (e){
                console.log(e);
            }
        }
    }

}
</script>
