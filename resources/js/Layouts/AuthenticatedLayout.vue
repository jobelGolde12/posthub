<script setup>
import { ref } from 'vue';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';
import NavLink from '@/Components/NavLink.vue';
import ResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import { Link } from '@inertiajs/vue3';

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div>
        <div class="min-h-screen bg-gray-100">
            <nav
                class="border-b border-gray-100 bg-light"
            >
                <!-- Primary Navigation Menu -->
                <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
                    <div class="flex h-16 justify-between">
                        <div class="flex">
                            <!-- Logo -->
                            <div class="flex shrink-0 items-center">
                                <Link :href="route('dashboard')" class="text-dark text-decoration-none">
                                   PostHub
                                </Link>
                            </div>

                            <!-- Navigation Links -->
                            <div
                                class="hidden space-x-8 sm:-my-px sm:ms-10 sm:flex"
                            >
                                <!-- <NavLink
                                    :href="route('dashboard')"
                                    :active="route().current('dashboard')"
                                >
                                    Dashboard
                                </NavLink> -->
                            </div>
                        </div>

                        <div class="hidden sm:ms-6 sm:flex sm:items-center">
                            <!-- Settings Dropdown -->
                            <div class="relative ms-3">
                                <Dropdown align="right" width="48">
                                    <template #trigger>
                                        <span class="inline-flex rounded-md">
                                            <button
                                                type="button"
                                                class="inline-flex items-center rounded-md border border-transparent bg-white px-3 py-2 text-sm font-medium leading-4 text-gray-500 transition duration-150 ease-in-out hover:text-gray-700 focus:outline-none"
                                            >
                                                {{ $page.props.auth.user.name }}

                                                <svg
                                                    class="-me-0.5 ms-2 h-4 w-4"
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    viewBox="0 0 20 20"
                                                    fill="currentColor"
                                                >
                                                    <path
                                                        fill-rule="evenodd"
                                                        d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                                                        clip-rule="evenodd"
                                                    />
                                                </svg>
                                            </button>
                                        </span>
                                    </template>

                                    <template #content>
                                        <DropdownLink
                                            :href="route('profile.edit')"
                                        >
                                            Profile
                                        </DropdownLink>
                                        <DropdownLink
                                            :href="route('logout')"
                                            method="post"
                                            as="button"
                                        >
                                            Log Out
                                        </DropdownLink>
                                    </template>
                                </Dropdown>
                            </div>
                        </div>

                        <!-- Hamburger -->
                        <div class="-me-2 flex items-center sm:hidden">
                            <button
                                @click="
                                    showingNavigationDropdown =
                                        !showingNavigationDropdown
                                "
                                class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 transition duration-150 ease-in-out hover:bg-gray-100 hover:text-gray-500 focus:bg-gray-100 focus:text-gray-500 focus:outline-none"
                            >
                                <svg
                                    class="h-6 w-6"
                                    stroke="currentColor"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                >
                                    <path
                                        :class="{
                                            hidden: showingNavigationDropdown,
                                            'inline-flex':
                                                !showingNavigationDropdown,
                                        }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M4 6h16M4 12h16M4 18h16"
                                    />
                                    <path
                                        :class="{
                                            hidden: !showingNavigationDropdown,
                                            'inline-flex':
                                                showingNavigationDropdown,
                                        }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M6 18L18 6M6 6l12 12"
                                    />
                                </svg>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Responsive Navigation Menu -->
                <div
                    :class="{
                        block: showingNavigationDropdown,
                        hidden: !showingNavigationDropdown,
                    }"
                    class="sm:hidden"
                >
                    <div class="space-y-1 pb-3 pt-2">
                        <ResponsiveNavLink
                            :href="route('dashboard')"
                            :active="route().current('dashboard')"
                        >
                            Dashboard
                        </ResponsiveNavLink>
                    </div>

                    <!-- Responsive Settings Options -->
                    <div
                        class="border-t border-gray-200 pb-1 pt-4"
                    >
                        <div class="px-4">
                            <div
                                class="text-base font-medium text-gray-800"
                            >
                                {{ $page.props.auth.user.name }}
                            </div>
                            <div class="text-sm font-medium text-gray-500">
                                {{ $page.props.auth.user.email }}
                            </div>
                        </div>

                        <div class="mt-3 space-y-1">
                            <ResponsiveNavLink :href="route('profile.edit')">
                                Profile
                            </ResponsiveNavLink>
                            <ResponsiveNavLink
                                :href="route('logout')"
                                method="post"
                                as="button"
                            >
                                Log Out
                            </ResponsiveNavLink>
                        </div>
                    </div>
                </div>
            </nav>

            <!-- Page Heading -->
            <!-- <header
                class="bg-white shadow"
                v-if="$slots.header"
            >
                <div class="mx-auto max-w-7xl px-4 py-6 sm:px-6 lg:px-8">
                    <slot name="header" />
                </div>
            </header> -->

                <div class="container-fluid left-and-main-holder d-flex flex-row align-items-center px-0 justify-content-between">
                                    <div class="sidebar bg-light">
                                        <div class="logo">
                                        <i class="bi bi-bar-chart-line-fill"></i> Dashboard
                                        </div>
                                        
                                                <div class="container d-flex justify-content-center align-items-">
                                                    <button class="new-post  btn btn-success">New Post</button>
                                                </div>

                                                <ul class="nav flex-column mt-3">
                                                <li class="nav-item">
                                                    <a href="#" class="nav-link"><i class="bi bi-house"></i> Home</a>
                                                </li>
                                                <li class="nav-item">
                                                    <a href="#" class="nav-link"><i class="bi bi-people"></i> Profile</a>
                                                </li>
                                                <li class="nav-item">
                                                    <a href="#" class="nav-link"><i class="bi bi-list-check"></i> My post</a>
                                                </li>
                                                
                                                
                                                </ul>
                                  </div> 
                                  <!-- End of a sidenav -->
                  <!-- Page Content -->
                    <main class="main">
                        <slot />
                    </main>
            </div>
            
        </div>
                </div>
</template>
<style scoped>
.left-and-main-holder{
    height: 100vh;
}
 .sidebar {
      height: 100%;
      width: 20%;
      position: relative;
      padding-top: 20px;
    }
    .sidebar .logo {
      font-size: 24px;
      color: #6b7280;
      font-weight: bold;
      margin-bottom: 20px;
      padding-left: 20px;
    }
    .sidebar a {
      color: #374151;
      text-decoration: none;
      padding: 10px 20px;
      display: flex;
      align-items: center;
      font-size: 15px;
    }
    .sidebar a:hover {
      background-color: #e5e7eb;
    }
    .sidebar .nav-item.active > a {
      background-color: #e5e7eb;
      font-weight: bold;
    }
    .sidebar a i {
      margin-right: 10px;
    }
    .nav-link {
      padding-left: 45px;
    }
    .sidebar .new-post{
        width: 90%;
        position: relative;
        margin: auto;
        background-color: #4158D0;
        background-image: linear-gradient(43deg, #4158D0 0%, #C850C0 46%, #FFCC70 100%);
        border: none;

    }
    .sidebar .tab-buttons {
      display: flex;
      justify-content: space-around;
      padding: 0 20px;
      margin-bottom: 10px;
    }
    .sidebar .tab-buttons .btn {
      font-size: 13px;
      padding: 5px 15px;
      border-radius: 20px;
    }
    .main{
        position: relative;
        width: 70%;
        height: 100%;
    }
</style>