<template>
<div class="LOGIN">
    <h2>sign in</h2>
    <form>
        <div class="input">
            <input v-model='username' type="text" name="" required="required">
            <span>username</span>
        </div>
        <div class="input">
            <input type="password" name="" required="required">
            <span>password</span>
        </div>
        <div class="input">
            <input @click='LoginInfo(true)' type="submit" value="login">
        </div>
        <a href="#">forgot password <span @click='LoginInfo(false)'>click here</span><p>{{username + ' '+ password}}</p></a>
    </form>
</div>
</template>
<script>
module.exports ={
    data: function(){
        return {
            username:"",
            password:'',
            forgotPassword:false
        }
    },
    methods: {
        LoginInfo: function(login){
            if (login) {
                this.username= document.querySelector('input[type="text"].value');
                this.password= document.querySelector('input[type="password"].value');
                this.forgotPassword=false;
            }else {
                this.forgotPassword=true;
                this.username="";
                this.password="";
            }
        }
    },
}
</script>
<style>
.LOGIN{
    text-align:center;
    width:350px;
    box-sizing:border-box;
    padding:40px;
    background:white;
}
.LOGIN h2 {
    margin: 0 0 20px;
    padding:0;
    font-size:30px;
    text-transform:uppercase;
}
.input{
    position:relative;
    width:100%;
    margin-bottom:25px;
}
.input input{
    height:50px;
    width:100%;
    padding:0 20px;
    box-sizing:border-box;
    font-size:18px;
    outline:none;
    border: 1px solid #000;
    }
.input span{
        position:absolute;
        top:12px;
        left:20px;
        padding:0;
        transition:0.5s;
        pointer-events:none;
        background:#fff;
        text-transform:uppercase;
    }
    .input input:focus ~ span, .input input:valid ~ span{
        top:-12px;
        left:12px;
        font-size:12px;
        padding:2px 4px;
        border:1px solid #000;
        background:#77aa77;
    }
    .input input[type="submit"]{
        background:#77aa77;
        border:none;
        box-shadow:none;
        cursor:pointer;
        text-transform:uppercase;
        font-weight:600;
    }
    .input input[type="submit"]:hover{
        background:white;
    }
    .LOGIN a{
        color:#666;
        text-decoration:none;
        display:block;
        text-align:left;
    }
    a span{
        color:262626;
        font-weight:600;
    }


</style>
