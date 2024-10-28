<script>
export default {
    name: 'SignUp',
    data() {
        return {
            name: '',
            email: '',
            password: '',
        }
    },
    methods: {
        signup() {
            alert(this.name)
        }
    }
}
</script>


<template>
    <div class="signup-container">
        <!-- Background video -->
        <video class="background-video" autoplay muted loop>
            <source src="C:\Users\prathama\Documents\Vue\Vue 3\src\assets\videoplayback.mp4" type="video/mp4">
        </video>

        <!-- Sign up card -->
        <div class="signup-card">
            <!-- Left side: logo and text -->
            <div class="left-side">
                <img class="logo" src="C:\Users\prathama\Documents\Vue\Vue 3\src\assets\kfc.png">
                <h1>Sign Up to Today :)</h1>
            </div>

            <div class="right-side">
                <div class="register">
                    <input type="text" v-model="name" placeholder="Enter name" required>
                    <input type="email" v-model="email" placeholder="Enter email" required>
                    <input type="password" v-model="password" placeholder="Enter password" required>
                    <button v-on:click="signup()">Submit</button>



                </div>

            </div>

        </div>


    </div>

</template>


<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.signup-container {
    position: relative;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}

.background-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    z-index: -1;
    filter: brightness(50%) sepia(100%) hue-rotate(-50deg);
}

.signup-card {
    display: flex;
    justify-content: space-between;
    width: 55%;
    max-width: 900px;
    background-color: #181818;
    border-radius: 20px;
    padding: 40px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    z-index: 1;
}

.left-side {
    flex: 1;
    text-align: center;
    padding-right: 20px;
}

.logo {
    height: 200px;
    width: 200px;
    border-radius: 50%;

}

h1 {
    color: white;
    font-family: cursive;
    margin-top: 20px;
}

.right-side {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.register input {
    width: 100%;
    height: 45px;
    padding-left: 20px;
    margin-bottom: 20px;
    border-radius: 15px;
    border: none;
    outline: none;
    background-color: #222;
    color: white;
    font-size: 14px;
    transition: all 0.3s ease;
}

.register input::placeholder {
    color: #aaa;
}

.register input:hover,
.register input:focus {
    background-color: #333;
}

.register button {
    width: 100%;
    height: 45px;
    border-radius: 15px;
    border: none;
    background-color: #AD2237;
    color: white;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

.register button:hover {
    background-color: darkred;
}
</style>