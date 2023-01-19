<template>
  <div class="header">
    <slot name="header"></slot>
  </div>
  <div class="body">
    <h1>Title</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores sint reiciendis omnis? Sapiente eaque dolorum aliquid laudantium enim veritatis officia, dignissimos mollitia ut illo. Error placeat iste nulla quam quaerat.</p>
    <slot></slot>
  </div>
  <div class="footer">
    <slot name="footer"></slot>
  </div>
</template>