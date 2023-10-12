<template>
  <div class="item">
    <div class="img">
      <slot name="image"></slot>
    </div>

    <div class="details">
      <h3>
        <slot name="texte" class="link-text"></slot>
      </h3>
      <p>
        <slot></slot>
      </p>
    </div>
  </div>
</template>
  
  <style scoped>
.item {
  display: grid;
  grid-template-columns: 1fr;
  padding: 1.5rem 3rem;
}
.img {
  width: 100%;
  height: fit-content;
  display: block;
}
.details {
  flex: 1;
  margin-top: 0.8rem;
}
h3 {
  font-family: "Montserrat", sans-serif;
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

@media (min-width: 768px) {
  .item {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 1.2rem;
    padding: 1.5rem 6rem;
  }
  .details {
    margin-top: 0;
  }
}
@media (min-width: 1135px) {
  .item {
    display: grid;
    grid-template-columns: 1fr;
    padding: 1.5rem 3rem;
  }
}
</style>