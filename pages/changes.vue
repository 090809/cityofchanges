<template>
<div>
    <h2 class="title">Платформа перемен</h2>

    <p class="p1">
        В рамках работы Движения <span>«Петербург-город перемен!»</span> <br/> создана проектная площадка <span>«Платформа перемен»</span>.
    </p>

    <div class="date">
        <!-- <div class="day">
            <h1>11</h1>
            <h1>мая</h1>
        </div> -->
        <p>Это <span>конкурс проектов</span>, в результате которого лучшие инициативы будут включены в <span>проектную площадку</span> и получат методическую, организационную и финансовую <span>поддержку</span>.</p>
    </div>

    <section class="steps">
      <div class="step">
        <img src="~/assets/request.png" alt="">
        <h3>Подай заявку</h3>
        <p>Заявка на конкурс подается в <span>электронном виде</span> на почту Движения <a href="mailto:press@gorodperemen.spb.ru">press@gorodperemen.spb.ru</a></p>
      </div>
      <div class="step">
        <img src="~/assets/start.png" alt="">
        <h3>Защити проект</h3>
        <p> Будет проведена серия 
            <span>публичных защит</span> поданных проектов.</p>
      </div>
      <div class="step">
        <img src="~/assets/support.png" alt="">
        <h3>Получи поддержку</h3>
        <p><span>Лучшие проекты </span>получат поддержку и будут включены в проектную площадку <span>«Платформа перемен»</span>.</p>
      </div>
    </section>

    <section class="aims">
        <h2 class="aims">Направления конкурса</h2>
        <main>
            <div class="aim">социальный город</div>
            <div class="aim">культурный город</div>
            <div class="aim">комфортный город</div>
            <div class="aim">спортивный город</div>
            <div class="aim">инновационный город</div>
        </main>
    </section>

    <!-- <router-link class="toInfo" to="/about">Положение о конкурсе</router-link> -->

    <!-- <p class="p1">Срок окончания подачи заявок <span>26 мая 2019 г. до 21:00.
    29 мая 2019 г.</span> будут подведены итоги конкурса.</p> -->

    <h2 class="best_wishes">Желаем всем удачи!</h2>
    <a class="SignInButton takePart takePartRow" href="/files/anketa.docx" target="_blank">Подать заявку</a>
</div>
</template>

<script>
import Contacts from '~/components/Contacts.vue'
import Navbar from '~/components/Navbar.vue'
import miniModal from '~/components/miniModal.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Contacts,
    Navbar,
    miniModal,
    Footer
  }
}
</script>

<style>
.takePart {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    font-weight: 500;
    font-size: 2rem;
    background: #71D5A2;
    padding: 1rem 2rem;
    border: none;
    border-radius: 100px;
    text-decoration: none;
    color: white;
    margin-bottom: 4rem;
    cursor: pointer;
    height: 5rem;
}

.title {
    text-align: center;
    font-size: 3rem;
    margin: 4rem 0;
    font-weight: 500;
}

.wrapper .p1 {
    grid-column: 4/12;
    text-align: center;
    font-size: 1.5rem;
}

p > span {
    font-weight: 500;
}

.date {
    width: 100%;
    margin: 4rem 0;
    grid-column: 4/12;
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-gap: 2vw;
}

/* .wrapper .date .day {
    grid-column: 1/2;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.date h1 {
    text-align: center;
    font-size: 3em;
    line-height: 4rem;
    color: #0C6293;
} */

.date p {
    font-size: 1.5rem;
    grid-column: 1/9;
    line-height: 2rem;
    text-align: center;
}

.steps {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 1vw;
  margin: 5vw 0;
}

.step {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.step img {
  width: 50%;
}

.step h3 {
  padding: 2rem 0;
  font-weight: 500;
  text-align: center;
}

.step p {
    text-align: center;
    line-height: 2rem;
}

.step a {
    color: #0C6293;
}

h2.aims {
    text-align: center;
    font-size: 2rem;
    font-weight: 500;
    margin: 3rem 0;
}

section.aims main {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 2vw;
}

.aim {
    width: 100%;
    font-size: 1.7rem;
    font-weight: 500;
    padding: 2.5rem 1rem;
    color: #000;
    background: #fff;
    box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.15);
    border-radius: 30px;
    text-align: center;
}

.toInfo {
    grid-column: 6/10;
    margin: 4rem 0;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    padding: 0.7rem 1.2rem;
    background: transparent;
    font-family: 'Rubik', sans-serif;
    border: 1px solid #023C71;
    border-radius: 100px;
    text-decoration: none;
    color: #023C71;
    font-weight: 500;
}

.best_wishes {
    text-align: center;
    font-size: 2rem;
    margin: 4rem 0;
    font-weight: 500;
}

.takePartRow {
  grid-column: 6/10;
}

@media (max-width: 780px) {
  .date {
    grid-gap: 4vw;
  }
  .takePart {
    grid-column: 5/11;
  }
  .toInfo {
    grid-column: 5/11;
  }
}

@media (max-width: 700px) {
  .steps {
    grid-template-columns: 1fr;
    grid-gap: 1vw;
    margin: 1vw 0;
  }
  .step{
      padding: 1rem 2rem;
  }
  .step img {
      width: 30%;
  }
}

@media (max-width: 576px) {
  .wrapper .takePart {
    grid-column: 4/12;
  }
  .wrapper .toInfo {
    grid-column: 4/12;
  }
}

@media (max-width: 420px) {
  .title {
      margin: 6rem 0 3rem;
  }
  section.aims main {
    grid-template-columns: 1fr 1fr;
    grid-gap: 2vw;
  }
  .aim {
    font-size: 1.5rem;
    padding: 2rem 1rem;
  }
  .p1 {
    grid-column: 3/13;
  }
  .date {
    grid-column: 3/13;
  }
  .toInfo {
    grid-column: 5/11;
  }
}
</style>