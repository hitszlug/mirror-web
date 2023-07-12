<script lang="ts">
import { RouterLink } from 'vue-router';
import { ElMenu } from 'element-plus/lib/components/index.js';
export default {
    components: {
        RouterLink, ElMenu
    },
    data() {
        return {
            isMenuOpen: false,
        }
    },
    methods: {
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
            console.log("toggleMenu!");
        }
    }
}
</script>
<template>
    <div class="header">
        <div class="logo-container">
            <img src="../../assets/osa.png" alt="OSA Logo" class="logo" />
            <h1>HITsz LUG Mirror</h1>
        </div>
        <nav>
            <ul class="nav-list">
                <li><router-link to="/" class="nav-item">Home</router-link></li>
                <li><router-link to="/news" class="nav-item">News</router-link></li>
                <li>About</li>
            </ul>
        </nav>
        <div class="hamburger-container">
            <label for="check">
                <input type="checkbox" id="check" />
                <span></span>
                <span></span>
                <span></span>
            </label>
        </div>
    </div>
</template>

<style scoped>
@import url(./style/hamburger.css);

.header {
    height: 60px;
    width: 100%;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

nav {
    display: none;
}

@media screen and (min-width: 768px) {
    .header {
        height: 60px;
        width: 100%;
        padding: 0 40px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .hamburger-container {
        display: none;
    }

    nav {
        display: inline;
    }
}

@media screen and (min-width: 992px) {
    .header {
        height: 60px;
        width: 100%;
        padding: 0 80px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}

@media screen and (min-width: 1200px) {
    .header {
        height: 60px;
        width: 100%;
        padding: 0 200px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}

.logo-container {
    display: flex;
    align-items: center;
    gap: 1rem;
}

.logo {
    width: 40px;
    height: 40px;
}

.nav-list {
    list-style: none;
    display: flex;
    gap: 2rem;
}

.nav-list li {
    transition: color .2s ease-in-out;
}

.nav-item {
    color: inherit;
    text-decoration: none;
}

.nav-list li:hover {
    color: #6689BE;
    cursor: pointer;
}
</style>