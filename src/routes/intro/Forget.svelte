<script>
    import Preload from "../../components/Preload.svelte";
    import {fade} from "svelte/transition";
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
    <div class="container"><img class="big-logo" src="{ps.env.LOGO_APP}" alt="">
        <!-- Register Form-->
        <div class="register-form mt-5 px-4">
            <form onsubmit="return false">
                <div class="form-group text-left mb-4"><span>Email or Username</span>
                    <label for="email"><i class="lni-user"></i></label>
                    <input class="form-control" id="email" type="text" placeholder="info@you.com">
                </div>
                <button class="btn btn-warning btn-lg w-100" on:click={()=>navigate("/login",{replace:true})}>Reset Password</button>
            </form>
        </div>
    </div>
</div>
