<script>
    import { fade } from 'svelte/transition';
    import Preload from "../../components/Preload.svelte";
    import {link} from "svelte-routing";
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
                <div class="form-group text-left mb-4"><span>Username</span>
                    <label for="username"><i class="lni-user"></i></label>
                    <input class="form-control" autocomplete="off" id="username" type="text" placeholder="info@example.com">
                </div>
                <div class="form-group text-left mb-4"><span>Password</span>
                    <label for="password"><i class="lni-lock"></i></label>
                    <input class="form-control" autocomplete="off" id="password" type="password" placeholder="********************">
                </div>
                <button class="btn btn-success btn-lg w-100">Login</button>
            </form>
        </div>
        <div class="login-meta-data text-dark"><a class="forgot-password d-block mt-3 mb-1" href="/forget" use:link>Forgot Password?</a>
            <p class=" mb-0">Didn't have an account?<a class="ml-2" href="/register" use:link>Register</a></p>
        </div>
    </div>
</div>
