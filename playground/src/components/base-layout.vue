<script></script>

<template>
  <div class="wrapper">
    <main class="main">
      <slot name="main"></slot>
    </main>
    <aside class="sidebar">
      <slot name="sidebar"></slot>
    </aside>
    <footer class="footer">
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<style>
.sidebar {
  border: 2px solid red;
}
.main {
  border: 2px solid green;
}
.footer {
  border: 2px solid blue;
}
</style>
