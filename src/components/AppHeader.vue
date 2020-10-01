<template>
    <div class="container">
        <header class="header">
            <div class="cell">
                <div class="header__location"><i class="el-icon-location-outline"></i>Волгоградская область</div>
                <div class="header__service_container">
                    <div class="header__service">
                        <a href="#" class="header__link">Тендеры</a>
                    </div>
                    <div class="header__service">
                        <a href="#" class="header__link">База подрядчиков</a>
                    </div>
                    <div class="header__service">
                        <el-dropdown>
                            <span class="el-dropdown-link">
                                Другие сервисы<i class="el-icon-arrow-down el-icon--right"></i>
                            </span>
                            <el-dropdown-menu slot="dropdown">
                                <el-dropdown-item>Сервис 1</el-dropdown-item>
                                <el-dropdown-item>Сервис 2</el-dropdown-item>
                                <el-dropdown-item>Сервис 3</el-dropdown-item>
                            </el-dropdown-menu>
                        </el-dropdown>
                    </div>
                </div>
            </div>
        </header>
        <section class="menu cell">
            <img src="../assets/logo.png" alt="Logo">
            <el-button class="menu__custom_button menu__custom_button--yellow" icon="el-icon-s-fold">Каталог</el-button>
            <el-input class="menu__custom_input" autocomplete placeholder="Хочу найти..." v-model="wanna_find">
                <template slot="append"><el-button icon="el-icon-search"></el-button></template>
            </el-input>
            <el-button class="menu__custom_button menu__custom_button--gray" icon="el-icon-s-fold">Каталог</el-button>
            <el-avatar style="background-color: purple;">A</el-avatar>
        </section>
        <el-divider></el-divider>
    </div>
</template>

<script>
export default {
    name: "AppHeader",
    data () {
        return {
            wanna_find: ""
        }
    }
}
</script>

<style lang="scss" scoped>
.container {
    .header {
        background-color: #FAFBFC;
        padding: .5rem 0;

        .cell {
            display: flex;
            justify-content: space-between;
            align-items: center;
    
            .header__service_container {
                display: flex;
                justify-content: right;

                .header__service {
                    margin: 0 0.7rem;

                    .header__link {
                        color: #666;
                        text-decoration: none;
                    }
                }
            }
        }
    }

    .menu {
        padding: .5rem 0;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .menu__custom_button {
            color: #000;
            border-radius: 4px;
        }

        .menu__custom_button--yellow {
            background-color: #FED83D;
        }

        .menu__custom_button--gray {
            background-color: #ECEFF1;
        }

        .menu__custom_input {
            max-width: 30rem;
        }
    }
}
</style>