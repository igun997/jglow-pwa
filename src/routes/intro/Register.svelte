<script>
    import { fade } from 'svelte/transition';
    import Preload from "../../components/Preload.svelte";
    import {link, navigate} from "svelte-routing";
</script>
<style>
    /*1b1e21*/
    .register-form span{
        color: #1b1e21 !important;
    }
    .register-form .form-control {
        color: #1b1e21 !important;
    }
    .login-meta-data a{
        color: #1b1e21 !important;  
    }
    .register-form .form-control::placeholder {
        color: #1b1e21 !important;
        opacity: 0.5;
    }
    .register-form form > .form-group > label {
        color: #1b1e21 !important;
    }
</style>
<Preload timer="1000" />
<div class="login-wrapper d-flex align-items-center justify-content-center text-center" in:fade>
    <div class="background-shape"></div>
    <div class="container"><img class="big-logo" src="{ps.env.LOGO_APP}" alt="">
        <div class="register-form mt-5 px-4">
            <form  onsubmit="return false">
                <div class="form-group text-left mb-4"><span>Name</span>
                    <label for="name"><i class="lni-user"></i></label>
                    <input class="form-control" autocomplete="off" id="name" type="text" placeholder="Indra Gunanda">
                </div>
                <div class="form-group text-left mb-4"><span>Email</span>
                    <label for="email"><i class="lni-envelope"></i></label>
                    <input class="form-control" autocomplete="off" id="email" type="text" placeholder="info@example.com">
                </div>
                <div class="form-group text-left mb-4"><span>Password</span>
                    <label for="password"><i class="lni-lock"></i></label>
                    <input class="form-control" autocomplete="off" id="password" type="password" placeholder="********************">
                </div>
                <button class="btn btn-success btn-lg w-100" on:click={()=>navigate("/login",{replace:true})}>Register</button>
            </form>
        </div>
        <div class="login-meta-data text-dark">
            <p class=" mt-5">Have an account?<a class="ml-2" href="/login" use:link>Login</a></p>
        </div>
    </div>
</div>
