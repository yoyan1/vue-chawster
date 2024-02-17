<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="title">
        <h1><b class="primary">chaw</b>ster</h1>
    </div>
    <a href="#" class="icon" ><i class="fa-solid fa-bars"></i></a>
    <div class="nav-bar">
        <RouterLink to="/">Home</RouterLink>
        <div class="dropdown-center">
        <button class="btn text-light dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Category
        </button>
        <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="article.php?category=health">Health</a></li>
            <li><a class="dropdown-item" href="article.php?category=technology">Technology</a></li>
            <li><a class="dropdown-item" href="article.php?category=nature">Nature</a></li>
            <li><a class="dropdown-item" href="article.php?category=short stories">Short stories</a></li>
            <li><a class="dropdown-item" href="article.php?category=relationship">Relationship</a></li>
            <li><a class="dropdown-item" href="article.php?category=mythology">Mythology</a></li>
            <li><a class="dropdown-item" href="article.php?category=art">Art</a></li>
        </ul>
        </div>
        <RouterLink to="/about">Article</RouterLink>
        <div class="login-wrap">
            <a href="" data-bs-toggle="modal" data-bs-target="#login" id="click" class="login">login</a> /
            <a href="" data-bs-toggle="modal" id="click1" data-bs-target="#register">Register</a>
        </div>
    </div>
        

    <!-- Modal -->
    <div class="modal fade" id="create" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <form action="../php/create.php" method="POST" enctype="multipart/form-data" class="modal-content">
        <div class="modal-header">
            <h1 class="modal-title fs-5" id="exampleModalLabel">Create</h1>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
            <div class="modal-body">
                <input type="number" style="display: none" name="id" >
                <div class="mb-3">
                <label for="exampleFormControlInput1" class="form-label">Author</label>
                <input type="text" name="name"  class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
                <div class="mb-3">
                <label for="exampleFormControlInput1" class="form-label">title</label>
                <input type="text" name="title" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
                <div class="mb-3">
                <label for="exampleFormControlInput1" class="form-label">image</label>
                <input type="file" name="image" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
                <div class="mb-3">
                    <select name="category" class="form-select d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" aria-label="Default select example" required>
                        <option selected>select category</option>
                        <option>health</option>
                        <option>technology</option>
                        <option>nature</option>
                    </select>
                </div>
                <div class="mb-3">
                <label for="exampleFormControlTextarea1" class="form-label">content</label>
                <textarea name="content" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlTextarea1" rows="3" required></textarea>
                </div>
            </div>
        <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            <button type="submit" name="submit" class="btn text-white bg-success">Save</button>
        </div>
        </form>
    </div>
    </div>

    <!-- register -->
    <div class="modal fade" id="register" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <form action="../php/signup.php" method="POST" enctype="multipart/form-data" class="modal-content">
            <div class="modal-header">
                <h1 class="modal-title fs-5" id="exampleModalLabel">Sign up</h1>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <div class="mb-3">
                    <label for="exampleFormControlInput1" class="form-label">Fullname</label>
                    <input type="text" name="name" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
                <div class="mb-3">
                    <label for="exampleFormControlInput1" class="form-label">Email</label>
                    <input type="email" name="email" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" placeholder="name@example.com" required>
                </div>
                <div class="mb-3">
                    <label for="exampleFormControlInput1" class="form-label">Password</label>
                    <input type="password" name="password" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
                <div class="mb-3">
                    <label for="exampleFormControlInput1" class="form-label">Profile</label>
                    <input type="file" name="image" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                </div>
            </div>
            <div class="modal-footer">
                <button type="submit" name="submit"  class="btn text-white bg-success">Sign up</button>
            </div>
        </form>
    </div>
    </div>
        
    <!-- log in -->
    <div class="modal fade" id="login" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <form action="../php/signin.php" method="POST" class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h1 class="modal-title fs-5" id="exampleModalLabel">Sign in</h1>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="mb-3">
                        <label for="exampleFormControlInput1" class="form-label">Email</label>
                        <input type="email" name="email" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" placeholder="name@example.com" required>
                    </div>
                    <div class="mb-3">
                        <label for="exampleFormControlInput1" class="form-label">Password</label>
                        <input type="password" name="password" class="form-control d-inline-flex focus-ring py-1 px-2 text-decoration-none border rounded-2" style="--bs-focus-ring-color: rgba(var(--bs-success-rgb), .25)" id="exampleFormControlInput1" required>
                    </div>
                </div>
                <div class="modal-footer">
                    <button type="submit" name="submit" class="btn text-white bg-success">Sign in</button>
                </div>
            </div>
        </form>
    </div>

</template>

<style scoped>

    .modal-title{
        color: black;
    }
    .form-label{
        color: black;
    }
</style>