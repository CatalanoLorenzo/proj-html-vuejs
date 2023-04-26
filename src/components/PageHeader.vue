<script>
export default {
    name: 'PageHeader',
    data() {
        return {

        }
    },
}
</script>
<template>
    <header>
        <nav class="navbar position-fixed  w-100">
            <div class="container ">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logotype.png" alt="Bootstrap" width="30" height="24">
                </a>

                <ul class="navbar-nav d-flex ">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Pricing</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link disabled">Disabled</a>
                    </li>
                </ul>

            </div>
        </nav>

    </header>
</template>
