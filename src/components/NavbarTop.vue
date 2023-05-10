<template>
    <div class="navbar-top">
        <div class="container">
            <a href="#!" class="navbar-top__logo"><img src="../../public/image/logo.svg" alt=""></a>
            <div class="navbar-top__input">
                <select name="" id="">
                    <option value="">All cotegories</option>
                    <option value="">asdad</option>
                    <option value="">asdad</option>
                </select>
                <div>
                    <input type="search" placeholder="Search..">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                    <path strokeLinecap="round" strokeLinejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
                    </svg>
                </div>
            </div>
            <div class="navbar-top__right">
                <div class="navbar-top__selects">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                    <path strokeLinecap="round" strokeLinejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                    <path strokeLinecap="round" strokeLinejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
                    </svg>
                    <select name="" id="">
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                    </select>
                </div>
                <div class="navbar-top__shop">
                    <button>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                        <path strokeLinecap="round" strokeLinejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
                        </svg>
                        Wishlist
                    </button>
                    <button>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                        <path strokeLinecap="round" strokeLinejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                        </svg>
                        card
                    </button>
                    <button>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                        <path strokeLinecap="round" strokeLinejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
                        </svg>
                        Account
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

.navbar-top {
    padding: 30px 0;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .navbar-top__input {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 466px;
            width: 100%;
            padding: 11px 20px;
            border: 1px solid var(--border-2);
            border-radius: 5px;
            select {
                border: none;
                outline: none;
                font-family: var(--Inter);
                font-weight: 600;
                line-height: 15px;
                margin-right: 15px;
                cursor: pointer;
            }
            div {
                display: flex;
                width: 100%;
                input {
                    border: none;
                    width: 100%;
                    padding-left: 15px;
                    border-left: 1px solid var(--border);
                    &::placeholder {
                        font-weight: 600;
                        color: var(--link);
                    }
                }
                svg {
                    width: 22px;
                    height: 22px;
                    color: var(--link);
                }
            }
        }
        .navbar-top__right {
            display: flex;
            justify-content: space-between;
            align-items: center;
            column-gap: 30px;
            .navbar-top__selects {
                display: flex;
                padding: 10px;
                border-radius: 5px;
                color: var(--link);
                cursor: pointer;
                transition: .5s;
                &:hover {
                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.1);
                    select {
                        color: var(--link-hover);
                    }
                }
                svg {
                    width: 30px;
                    height: 25px;
                }
                select {
                    border: none;
                    outline: none;
                    cursor: pointer;
                    transition: .5s;
                    color: var(--link);
                }
            }
            .navbar-top__shop {
                display: flex;
                column-gap: 20px;
                button {
                    display: flex;
                    align-items: center;
                    column-gap: 5px;
                    font-size: 14px;
                    color: var(--icon-color);
                    padding: 10px;
                    border-radius: 5px;
                    transition: .5s;
                    &:hover {
                        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.1);
                        color: var(--link-hover);
                    }
                    svg {
                        width: 26px;
                        height: 26px;
                    }
                }
            }
        }
    }
}



</style>