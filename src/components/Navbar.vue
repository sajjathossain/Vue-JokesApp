<template>
    <div class="navbar">
        <div class="contained">
            <h2 class="navbar-brand">
                What a joke!
            </h2>

            <ul class="nav-items">
                <li class="nav-link">
                    <router-link tag="a" to="/">Jokes!</router-link>
                </li>
                <li class="nav-link">
                    <router-link tag="a" to="/about">About</router-link>
                </li>
                <li class="nav-link">
                    <router-link tag="a" to="/contact">Contact</router-link>
                </li>
            </ul>
        </div>
    </div>
  <router-view/>
</template>

<script>
export default {
    name: 'Navbar',
}
</script>

<style lang="scss" scoped>
    .navbar {
        display: flex;
        background-color: #000;
        padding: 2vh 3vw;

        .navbar-brand {
            font-size: 26px;
            padding: 0;
            margin: 0;
        }

        .contained {
            color: #fff;
            width: 100vw;
            display: flex;
            align-items: center;
            justify-content: space-between;

            .nav-items {
                margin: 0 2vw;
                display: flex;

                .nav-link {
                    padding: 0 2vw;
                    list-style: none;
                    a {
                        font-size: 22px;
                        font-weight: bold;
                        color: #fff;
                        text-decoration: none;
                        
                        &:hover{
                            color: orange;
                        }
                    }

                }
            }
        }
    }
</style>