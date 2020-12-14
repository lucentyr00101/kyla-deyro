<template>
  <div class="cats">
    <div class="cat cat--1">
      <img src="https://cdn.dribbble.com/users/218750/screenshots/2090988/sleeping_beauty.gif" alt="">
    </div>
    <div class="cat cat--2">
      <img src="https://cdn.dribbble.com/users/6191/screenshots/1192777/catpurr.gif" alt="">
    </div>
    <div class="cat cat--3">
      <img src="https://cdn.dribbble.com/users/6191/screenshots/2211315/meal.gif" alt="">
    </div>
    <div class="cat cat--4">
      <img src="https://cdn.dribbble.com/users/6191/screenshots/1189704/walkingcat.gif" alt="">
    </div>
    <div class="cat cat--5">
      <img src="https://cdn.dribbble.com/users/6191/screenshots/3661586/cat_sleep_dribbble.gif" alt="">
    </div>
  </div>
</template>

<style lang="scss" scoped>
$first: #abe7db;
$second: #f67c61;
$third: #fff9e8;
$forth: #58a5a3;
$fifth: #172535;

$list: ('1': $first, '2': $second,'3': $third,'4': $forth,'5': $fifth);

@mixin grid($column-start, $column-end, $row-start: $column-start, $row-end: $column-end) {
  grid-column-start: $column-start;
  grid-column-end: $column-end;
  grid-row-start: $row-start;
  grid-row-end: $row-end;
}

body, html {
  margin: 0;
  padding: 0;
}

.cats {
  display: grid;
  grid-auto-flow: dense;
  overflow: hidden;
}
@media screen and (min-width: 45em) {
  .cats {
    height: 100vh;
    grid-template-columns: 29% 29% 43.5%;
    grid-template-rows: 50% 16% 34%;
  }
}
@media screen and (max-width: 45em) and (min-width: 25em) {
  .cats {
    grid-template-columns: repeat(2, (100vw / 2));
    grid-template-rows: repeat(3, 1fr);
  }
}
@media screen and (max-width: 25em) {
  .cats {
    grid-template-columns: 100vw;
    grid-template-rows: repeat(5, 1fr);
  }
}

.cat {
  img {width:100%;}
  @each $i in map-keys($list) {
    &.cat--#{$i} {
      background-color: map-get($list, $i);
    }
  }
  &.cat--1 {
    @include grid(1, 3);
  }
  &.cat--2 {
    @include grid(1, 2, 3, 4);
  }
  &.cat--3 {
    @include grid(2, 3, 3, 4);
  }
  &.cat--4 {
    @include grid(3, 4, 1, 2);
  }
  &.cat--5 {
    @include grid(3, 4, 2, 4);
  }
  @media screen and (max-width: 45em) and (min-width: 25em) {
    @for $j from 4 through 5 {
      &.cat--#{$j} {
        @include grid($j - 3, $j - 2, 4, 5);
      }
    }
  }
  @media screen and (max-width: 25em) {
    @for $k from 1 through 5 {
      &.cat--#{$k} {
        @include grid(1, 2, $k, $k + 1);
      }
    }
  }
}
</style>
