<script>
    //some comment to push
    import Steps from './_components/Steps.svelte';
    import {push} from 'svelte-spa-router';
    import Subscribe from './_components/Subscribe.svelte';
    import Footer from './_components/Footer.svelte';
</script>
<header>
    <a href="/"><img id="logo" src="logo.svg" alt="cd"></a>
    <div class="social-icons">
        <a href="https://github.com/Common-Data-Team"><img src="./images/icons/Github_black.svg" alt="github-logo-icon"></a>
        <a href="https://www.patreon.com/commondatateam"><img src="./images/icons/Patreon_black.svg"
                                                              alt="patreon-logo-icon"></a>
        <a href="https://www.linkedin.com/company/common-data-team"><img src="./images/icons/LinkedIN_black.svg"
                                                                         alt="linkedin-logo-icon"></a>
        <a href="https://t.me/commondatateam"><img src="./images/icons/Telegram_black.svg" alt="telegram-logo-icon"></a>
    </div>
</header>
<main>
    <div class="first-view">
        <div class="first-block">
            <div class="description">
                <h1>Check the Data</h1>
                <p>Сервис для аналитики и улучшения датасетов</p>
                <button on:click={() => push('/service')}>Попробовать</button>
            </div>
            <div class="image">
                <img src="./images/main_img.svg" alt="main-image">
            </div>
        </div>
    </div>
    <div class="second-block">
        <h1>Для кого?</h1>
        <div class="cards">
            <div class="card">
                <img src="./images/developer.svg" alt="developer-image">
                <h3>Разработчики</h3>
                <p>Профессионалы могут удостовериться в качестве данных и ускорить процесс обработки датасета</p>
            </div>
            <div class="card">
                <img src="./images/new.svg" alt="new-analytics-image">
                <h3>Начинающие аналитики</h3>
                <p>Начинающие аналитики могут научиться обработке датасетов с помощью наших инструкций</p>
            </div>
            <div class="card">
                <img src="./images/not_it.svg" alt="not-it-image">
                <h3>Не ИТ специалисты</h3>
                <p>Те, кто принимают решения на основе данных, могут воспользоваться автоматизированным алгоритмом и
                    обработать датасет в один клик</p>
            </div>
        </div>
    </div>
    <Steps/>
    <h1 class="subscribe">Подписаться на новости сервиса</h1>
    <div class="subscribe">
        <Subscribe/>
    </div>
    <Footer/>
</main>

<style>
    button:hover {
        cursor: pointer;
    }

    main {
        width: 100%;
        height: 100%;
    }

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 30px;
    }

    .second-block h1 {
        text-align: center;
        margin: 100px 0 50px 0;
    }

    .cards {
        display: flex;
        justify-content: center;
        align-items: center;
        align-items: flex-start;
    }

    .card {
        background: #FFFFFF;
        width: 20%;
        margin: 2%;
        padding: 20px;
        height: auto;
        box-shadow: 0px 9.03px 27.09px rgba(176, 190, 197, 0.32), 0px 3.39px 5.64px rgba(176, 190, 197, 0.32);
        border-radius: 10px;
    }

    .description {
        text-align: left;
    }

    .description h1 {
        font-size: calc(36px + (48 - 36) * ((100vw - 300px) / (1440 - 300)));
    }

    .description p {
        font-size: calc(16px + (24 - 16) * ((100vw - 300px) / (1440 - 300)));
        max-width: 300px;
    }

    .first-view {
        width: 100%;
        height: 70vh;
    }

    .first-block {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .subscribe {
        display: flex;
        justify-content: center;
        text-align: center;
        margin-top: 3%;
    }

    header img {
        height: 60px;
    }

    .social-icons img {
        height: 36px;
        padding: 2px;
    }

    .image img {
        max-width: 600px;
    }

    .description button {
        background-color: #282828;
        font-family: 'Raleway', sans-serif;
        font-weight: 400;
        color: #FFFFFF;
        border-radius: 8px;
        padding: 15px 45px;
        margin: 20px auto;
    }

    .card img {
        width: 90%;
    }

    @media (max-width: 1270px) {

        .first-view {
            height: 30vh;
        }

        .first-block img {
            width: 400px;
        }
    }


    @media (max-width: 700px) {
        .cards {
            flex-direction: column;
        }

        .first-view {
            height: 70vh;
        }

        .card {
            width: 80%;
        }

        .first-block {
            flex-direction: column-reverse;
            text-align: center;
        }

        .first-block img {
            width: 80%;
        }

        .description {
            text-align: center;
        }

        .social-icons img {
            width: 24px;
        }

        #logo {
            width: 48px;
        }
    }

</style>