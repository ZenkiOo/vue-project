<template>
  <div>
    <h1>My App</h1>
    <hr />
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa qui quae
      impedit fuga deleniti deserunt recusandae temporibus odio maiores aliquid,
      nobis incidunt accusamus minus obcaecati cupiditate pariatur nihil quo
      cumque! Inventore laudantium, perferendis dolor quia voluptatibus,
      nesciunt alias saepe, expedita aliquam nulla ea quibusdam officia. Atque
      ab repellendus, hic voluptatum amet voluptatem doloribus provident error
      eius. Qui odit quo possimus. Neque fuga facilis, voluptates quia illum
      deserunt ipsum cupiditate praesentium adipisci hic, perferendis sapiente
      facere! Rem possimus, labore quidem placeat quam libero, corporis atque
      vel, tenetur at repellat molestiae dicta?
    </p>
    <router-link class="link" to="/todos">ToDos</router-link>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
};
</script>

<style lang="scss">
.link {
  color: inherit;
}
</style>
