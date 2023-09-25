<template>
  <template v-if="props.use == 'nuxt-link'">
    <nuxt-link :to="props.url" :class="`anim-${props.btnStyle}`">
      <slot></slot>
    </nuxt-link>
  </template>
  <template v-else-if="props.use == 'vue-link'">
    <router-link :to="props.url" :class="`anim-${props.btnStyle}`">
      <slot></slot>
    </router-link>
  </template>
  <template v-else>
    <a :href="props.url" :class="`anim-${props.btnStyle}`"><slot></slot></a>
  </template>
</template>

<script setup lang="ts">
interface Props {
  btnStyle: string;
  url: string;
  use: "nuxt-link" | "vue-link" | "html-link";
}
const props = withDefaults(defineProps<Props>(), {
  btnStyle: "1",
  url: "#",
  use: "html-link",
});
</script>
<style>
.anim-1 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
}
.anim-1:hover {
  color: white;
}
.anim-1:hover:before {
  transform: rotate(0deg);
}
.anim-1:hover:after {
  transform: rotate(0deg);
}
.anim-1:before {
  content: "";
  background-color: #9a1aaa;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  position: absolute;
  transform-origin: left bottom;
  transform: rotate(-90deg);
  transition-property: transform;
  transition-duration: 1s;
  z-index: -1;
}
.anim-1:after {
  content: "";
  background-color: #9a1aaa;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  position: absolute;
  transform-origin: right top;
  transform: rotate(-90deg);
  transition-property: transform;
  transition-duration: 1s;
  z-index: -1;
}

.anim-2 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  font-size: 1rem;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
}
.anim-2:hover {
  color: white;
}
.anim-2:hover:before {
  transform: translatex(0px);
}
.anim-2:before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background-color: #9a1aaa;
  transform: translateX(-100%);
  transition: all 0.4s ease-out;
  z-index: -1;
}

.anim-3 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
}
.anim-3:hover {
  color: white;
}
.anim-3:hover:after {
  transform: rotateY(0deg);
}
.anim-3:hover:before {
  transform: rotateX(0deg);
}
.anim-3:before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background-color: #9a1aaa;
  transform: rotateX(90deg);
  transition: transform 0.9s;
  z-index: -1;
}
.anim-3:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background-color: #9a1aaa;
  transform: rotateY(90deg);
  transition-property: transform;
  transition-duration: 0.9s;
  z-index: -1;
}

.anim-4 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
}
.anim-4:hover {
  color: white;
}
.anim-4:hover:before {
  transform: translatey(0%);
}
.anim-4:before {
  content: "Want to Send?";
  font-size: xx-small;
  position: absolute;
  margin: auto;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  transform: translatey(-100%);
  background-color: #9a1aaa;
  transition: all 1s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.anim-5 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  letter-spacing: 6px;
  transition: all 0.4s;
  color: #fff;
  text-decoration: none;
  background-color: transparent;
  justify-content: center;
  align-items: center;
  position: relative;
}
.anim-5:hover {
  color: black;
}
.anim-5:hover:after {
  left: 0px;
  top: 10px;
  transform: perspective(1000px) rotateX(-75deg);
}
.anim-5:hover:before {
  left: 0px;
  top: -10px;
  transform: perspective(1000px) rotateX(75deg);
}
.anim-5:before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: -3px;
  background-color: #c221d6;
  top: -3px;
  z-index: -1;
  mix-blend-mode: multiply;
  transition: all 0.2s;
  transform-origin: top;
}
.anim-5:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: #72137e;
  left: 3px;
  top: 3 px;
  z-index: -1;
  mix-blend-mode: multiply;
  transition: all 0.2s;
  transform-origin: bottom;
}

.anim-6 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  text-decoration: none;

  color: #9a1aaa;
  letter-spacing: 6px;

  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.1s;
  transition-duration: 1s;
}
.anim-6:before {
  content: "";
  border-top: 2px solid #9a1aaa;
  border-bottom: 2px solid green;
  position: absolute;
  z-index: 9;
  width: 120%;
  height: 100%;
  top: 0;
  bottom: 0;
  margin-top: auto;
  margin-bottom: auto;
  transition: all 0.4s;
}
.anim-6:after {
  content: "";
  border-left: 2px solid #9a1aaa;
  border-right: 2px solid #4a0c52;
  position: absolute;
  z-index: 9;
  width: 100%;
  height: 150%;
  top: 0;
  bottom: 0;
  margin-top: auto;
  margin-bottom: auto;
  transition: all 0.4s 0.2s;
}
.anim-6:hover {
  color: #4a0c52;
}
.anim-6:hover:before {
  transform: rotateX(180deg);
}
.anim-8:hover:after {
  transform: rotateY(180deg);
}

.anim-7 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;

  text-decoration: none;
  color: #fff;
  background-color: #9a1aaa;
  letter-spacing: 6px;
  justify-content: center;
  align-items: center;
  position: relative;
}
.anim-7:before {
  content: "";
  border-left: 2px solid #9a1aaa;
  border-top: 2px solid #9a1aaa;
  width: 20px;
  height: 20px;
  position: absolute;
  left: -4px;
  top: -4px;
  transition: all 0.4s;
}
.anim-7:after {
  content: "";
  border-right: 2px solid #9a1aaa;
  border-bottom: 2px solid #9a1aaa;
  width: 20px;
  height: 20px;
  position: absolute;
  right: -4px;
  bottom: -4px;
  transition: all 0.4s;
}
.anim-7:hover:before {
  width: 90%;
  height: 90%;
}
.anim-7:hover:after {
  width: 90%;
  height: 90%;
}

.anim-8 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;

  text-decoration: none;
  color: white;
  letter-spacing: 6px;
  font-size: 1.2rem;
  justify-content: center;
  align-items: center;
  position: relative;
  background: transparent;
  border: none;
}
.anim-8:before {
  content: "";
  position: absolute;
  width: 50%;
  height: 100%;
  background-color: blue;
  left: -1%;
  z-index: -1;
  top: -3%;
  transform: skewx(30deg);
  transition: all 0.2s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.anim-8:after {
  content: "";
  position: absolute;
  width: 50%;
  height: 100%;
  background-color: red;
  right: -1%;
  z-index: -1;
  top: 3%;
  transform: skewx(30deg);
  transition: all 0.2s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.anim-8:hover:before {
  left: 50%;
  top: 0;
  transform: skewx(0deg);
  background-color: blue;
}
.anim-8:hover:after {
  right: 50%;
  top: 0;
  transform: skewx(0deg);
  background-color: red;
}

.anim-9 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;
  text-decoration: none;
  color: white;
  background-color: #c221d6;
  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.2s;
  border-radius: 2rem;
  letter-spacing: 6px;
  text-decoration: none;
  color: white;
  background-color: #c221d6;
  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.2s;
  border-radius: 2rem;
  letter-spacing: 6px;
}
.anim-9:before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: #c221d6;
  transition: all 0.2s;
  border-radius: inherit;
  z-index: -1;
}
.anim-9:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}
.anim-9:hover:before {
  transform: scaleX(1.4) scaleY(1.6);
  opacity: 0;
}
.anim-9:active {
  transform: translateY(-1px);
  box-shadow: 0 5px 7px rgba(0, 0, 0, 0.2);
}

.anim-10 {
  min-width: max-content;
  min-height: max-content;
  display: inline-flex;
  padding-inline: 1em;
  padding-block: 0.5em;
  font-size: 1rem;
  cursor: pointer;
  font-family: sans-serif;

  text-decoration: none;
  color: black;
  background-color: transparent;
  border: 2px solid #9a1aaa;

  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
  transition: all 0.7s;
  border-radius: 2rem;
  letter-spacing: 6px;
}
.anim-10:hover {
  color: white;
}
.anim-10:before {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  border-top: 2rem solid #9210a3;
  border-bottom: 2rem solid #9210a3;
  border-right: 2rem solid transparent;
  transform: translateX(-100%);
  transition: all 0.7s;
}
.anim-10:after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  border-top: 2rem solid #9210a3;
  border-bottom: 2rem solid #9210a3;
  border-left: 2rem solid transparent;
  transform: translateX(100%);
  transition: all 0.7s;
}
.anim-10:hover:before {
  transform: translateX(0);
}
.anim-10:hover:after {
  transform: translateX(0);
}
</style>
