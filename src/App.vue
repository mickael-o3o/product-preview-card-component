<template>
  <main>
    <article class="c-card">
      <header class="c-card__header">
        <picture>
          <source media="(min-width: 27rem)" srcset="/images/image-product-desktop.jpg" />
          <source srcset="/images/image-product-mobile.jpg" />
          <img class="c-card__image" src="/images/image-product-mobile.jpg" alt="" />
        </picture>
      </header>

      <section class="c-card__body">
        <p class="c-card__category">Perfume</p>

        <header class="c-card__title">Gabrielle Essence Eau De Parfum</header>

        <p class="c-card__description">
          A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator
          for the House of CHANEL.
        </p>

        <p class="c-card__pricing">
          <span class="c-card__price"> $149.99</span>
          <span class="c-card__price c-card__price--old">$169.99</span>
        </p>

        <button class="c-card__add-to-cart">
          <img src="/images/icon-cart.svg" alt="" />Add to Cart
        </button>
      </section>
    </article>
  </main>
  <footer>
    <section class="attribution">
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
      Coded by
      <a href="https://github.com/mickael-o3o/product-preview-card-component.git">Mickael-o3o</a>.
    </section>
  </footer>
</template>

<style lang="scss" scoped>
@use './assets/utils/functions.scss' as *;

main {
  min-block-size: 100vh;
  display: grid;
  place-items: center;
}

.c-card {
  border-radius: var(--spacing-1);
  overflow: hidden;
  background-color: var(--color-neutral-white);
  inline-size: calc(100% - var(--spacing-2) * 2);
  max-inline-size: calc-rem(600);

  @media (min-width: 27rem) {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  &__image {
    inline-size: 100%;
    block-size: auto;
    display: block;

    @media (min-width: 27rem) {
      block-size: 100%;
      object-fit: cover;
    }
  }

  &__body {
    display: flex;
    flex-direction: column;
    padding: calc-rem(26);
    padding-block-start: calc-rem(23);

    @media (min-width: 27rem) {
      padding: calc-rem(32);
      padding-block-start: calc-rem(30);
    }
  }

  &__category {
    text-transform: uppercase;
    letter-spacing: calc-rem(5);
    font-size: calc-rem(12);
    margin-block-end: var(--spacing-1);
  }

  &__title {
    font: {
      family: var(--font-family-2);
      size: calc-rem(32);
    }
    line-height: 100%;
    color: var(--color-neutral-black);
    margin-block-end: var(--spacing-2);
  }

  &__description {
    margin-block-end: calc-rem(15);

    @media (min-width: 27rem) {
      margin-block-end: calc-rem(20);
    }
  }

  &__pricing {
    display: flex;
    align-items: center;
    gap: var(--spacing-2);
    margin-block-end: var(--spacing-1);

    @media (min-width: 27rem) {
      margin-block-end: calc-rem(20);
    }
  }

  &__price {
    font: {
      family: var(--font-family-2);
      size: calc-rem(31);
    }
    color: var(--color-primary);
  }

  &__price--old {
    text-decoration: line-through;
    font-family: var(--font-family-1);
    color: var(--color-neutral-grey);
    font: {
      size: 1rem;
      weight: 500;
    }
  }

  &__add-to-cart {
    background-color: var(--color-primary);
    color: var(--color-neutral-white);
    border: none;
    inline-size: 100%;
    padding: calc-rem(16) 0;
    border-radius: calc-rem(7);
    font-family: var(--color-primary);
    font-weight: var(--font-weight-bold);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: calc-rem(10);
  }
}

footer {
  border: calc-rem(1) solid transparent;
}

.attribution {
  font-family: monospace;
  border: calc-rem(1) solid var(--color-neutral-grey);
  color: var(--color-neutral-black);
  inline-size: fit-content;
  margin: 1rem auto;
  padding: 1rem 3rem;
  font-weight: normal;

  a {
    color: var(--color-primary);
  }
}
</style>
