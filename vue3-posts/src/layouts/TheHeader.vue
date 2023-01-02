<template>
    <header>
        <nav
            class="navbar navbar-expand-sm navbar-dark bg-body-tertiary bg-primary"
        >
            <div class="container-fluid">
                <a class="navbar-brand" href="#">GYM CODING</a>
                <button
                    class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent"
                    aria-controls="navbarSupportedContent"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                >
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div
                    class="collapse navbar-collapse"
                    id="navbarSupportedContent"
                >
                    <ul class="navbar-nav me-auto">
                        <li class="nav-item">
                            <router-link class="nav-link" to="/">
                                Home
                            </router-link>
                        </li>
                        <li class="nav-item">
                            <router-link class="nav-link" to="/about">
                                About
                            </router-link>
                        </li>
                        <li class="nav-item">
                            <router-link class="nav-link" to="/posts">
                                게시글
                            </router-link>
                        </li>
                        <!-- <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/about">About</a>
            </li> -->
                    </ul>
                    <div class="d-flex">
                        <button
                            class="btn btn-outline-success"
                            type="button"
                            @click="goPage"
                        >
                            글쓰기
                        </button>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();
const goPage = () => {
    router.push({
        name: 'PostCreate',
    });
    // ('/posts/create');
};
</script>

<style lang="scss" scoped></style>
