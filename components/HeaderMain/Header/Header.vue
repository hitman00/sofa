<template>
  <div :class="$style.header_top_main">
    <div :class="$style.logo">Fundo</div>
    <div :class="$style.menobar">
      <ul>
        <li>Home</li>
        <li>About us</li>
        <li>Furniture</li>
        <li>Blog</li>
        <li>Contact us</li>
        <li>Login</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" module>
.header_top_main {
  width: 100%;
  display: flex;
  padding: 5% 0;
}

.logo {
  width: 20%;
  font-weight: 500;
  font-size: 20px;
}

.menobar {
  width: 80%;
  font-weight: 600;
  ul {
    display: flex;
    justify-content: end;
    li {
      padding: 1% 2%;
      transition: all 0.3s ease;
      border-radius: 50px;
      cursor: pointer;
      &:hover {
        background: #000;
      }
    }
  }
}
</style>
