<template>
    <nav class="navbar navbar-expand navbar-dark bg-dark">
        <a href="/" class="navbar-brand">Contactbook management app</a>
        <div class="mr-auto navbar-nav">
            <li class="nav-item">
                <router-link :to="{ name: 'contactbook' }" class="nav-link">
                    Contactbook
                    <i class="fas fa-address-book" />
                </router-link>
            </li>
        </div>
    </nav>
</template>