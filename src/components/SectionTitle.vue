<template>
  <h2 class="sectionTitle">
    <slot>Section Title</slot>
  </h2>
</template>

<style>
.sectionTitle {
  margin-bottom: 2rem;
  display: inline-block;
  position: relative;
}

.sectionTitle::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 30%;
  height: 4px;
  background-color: #fff;
}

@media (max-width: 768px) {
  .sectionTitle::after {
    bottom: unset;
    top: -14px;
    height: 6px;
  }
}
</style>