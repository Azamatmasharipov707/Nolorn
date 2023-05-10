<template>
    <nav class="nav">
        <div class="container">
            <button class="nav-btn btn">
                <img src="../../public/image/header/nav-menu.svg" alt="">
                Browse All Categories
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" className="w-5 h-5">
                <path fillRule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clipRule="evenodd" />
                </svg>

            </button>
            <ul class="nav__list">
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        home
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" className="w-5 h-5">
                        <path fillRule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clipRule="evenodd" />
                        </svg>
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        about
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" className="w-5 h-5">
                        <path fillRule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clipRule="evenodd" />
                        </svg>
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        shop
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" className="w-5 h-5">
                        <path fillRule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clipRule="evenodd" />
                        </svg>
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        blog
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" className="w-5 h-5">
                        <path fillRule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clipRule="evenodd" />
                        </svg>
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        Our team
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        Contact
                    </a>
                </li>
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        <font-awesome-icon class="nav__link-icons" :icon="['fab', 'facebook']" />
                        <font-awesome-icon class="nav__link-icons" :icon="['fab', 'twitter']" />
                        <font-awesome-icon class="nav__link-icons" :icon="['fab', 'instagram']" />
                        <font-awesome-icon class="nav__link-icons" :icon="['fab', 'youtube']" />
                        <font-awesome-icon class="nav__link-icons" :icon="['fab', 'whatsapp']" />
                    </a>
                </li>
            </ul>
            <div class="nav__call">
                <a href="#!">
                    <font-awesome-icon class="nav__call-icon" :icon="['fas', 'phone-volume']" />
                    <p>
                        (406) 555-0120
                        <span>Men-F+9 00-20 00</span>
                    </p>
                </a>
            </div>
        </div>
    </nav>
</template>

<script setup>

</script>

<style lang="scss" scoped>

.nav {
    padding: 10px 0;
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    &-btn {
        display: flex;
        align-items: center;
        column-gap: 10px;
        letter-spacing: 0.06em;
        font-size: 16px;
        svg {
            width: 30px;
            height: 30px;
        }
    }
    .nav__list {
        display: flex;
        align-items: center;
        .nav__item {
            &:last-of-type {
                .nav__link {
                    display: flex;
                    margin-left: 10px;
                    &:hover {
                        color: unset;
                        .nav__link-icons {
                            transition: .5s ease-in-out;
                            &:hover {
                                color: var(--link-hover);
                                transform: rotate(360deg);
                            }
                        }
                    }
                    svg {
                        height: 18px;
                        width: 18px;
                    }
                }
            }
            .nav__link {
                display: flex;
                align-items: center;
                margin-right: 15px;
                column-gap: 7px;
                font-size: 13px;
                text-transform: capitalize;
                color: var(--link-2);
                letter-spacing: 0.06em;
                line-height: 15px;
                font-weight: 500;
                transition: .5s;
                &:hover {
                    color: var(--link-hover);
                }
                svg {
                    width: 25px;
                    height: 25px;
                }
            }
        }
    }
    .nav__call {
        a {
            display: flex;
            align-items: center;
            column-gap: 10px;
            color: var(--icon-color);
            .nav__call-icon {
                font-size: 19px;
            }
            p {
                span {
                    display: block;
                    font-size: 10px;
                    color: var(--link);
                    margin-top: 5px;
                }
            }
        }
    }
}

</style>