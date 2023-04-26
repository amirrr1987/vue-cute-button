<template>
  <div class="btn">
    <a href="#" v-if="props.btnStyle == '1'" :class="`anim-${props.btnStyle}`">Hover Me</a>
    <!-- <a href="#" v-if="props.btnStyle == '2'" class="anim-2">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '3'" class="anim-3">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '4'" class="anim-4">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '5'" class="anim-5">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '6'" class="anim-6"><span>Hover Me</span></a>
    <a href="#" v-if="props.btnStyle == '7'" class="anim-7"><span>Hover Me</span></a>
    <a href="#" v-if="props.btnStyle == '8'" class="anim-8">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '9'" class="anim-9">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '10'" class="anim-10"><span>H</span>over Me</a>
    <a href="#" v-if="props.btnStyle == '11'" class="anim-11">Hover Me <span></span></a>
    <a href="#" v-if="props.btnStyle == '12'" class="anim-12">Hover Me <span></span></a>
    <a href="#" v-if="props.btnStyle == '13'" class="anim-13">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '14'" class="anim-14">Hover Me</a>
    <a href="#" v-if="props.btnStyle == '15'" class="anim-15">Hover Me</a> -->
  </div>
</template>

<script setup lang="ts">
interface Props {
  btnStyle: string
}
const props = withDefaults(defineProps<Props>(), {
  btnStyle: '1'
})

</script>

<style>
.anim-1 {
  width: 12rem;
  aspect-ratio: 3/1;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
  font-size: 1.4rem;
  font-family: sans-serif;
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
  content: '';
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
  content: '';
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
  width: 12rem;
  aspect-ratio: 3/1;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
  font-size: 1.4rem;
  font-family: sans-serif;
}
.anim-2:hover {
  color: white;
}
.anim-2:hover:before {
  transform: translatex(0px);
}
.anim-2:before {
  content: '';
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
  width: 12rem;
  aspect-ratio: 3/1;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
  font-size: 1.4rem;
  font-family: sans-serif;
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
  content: '';
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
  content: '';
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
  width: 12rem;
  aspect-ratio: 3/1;
  border: 3px solid #9a1aaa;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #4a0c52;
  position: relative;
  overflow: hidden;
  font-size: 1.4rem;
  font-family: sans-serif;
}
.anim-4:hover {
  color: white;
}
.anim-4:hover:before {
  transform: translatey(0%);
}
.anim-4:before {
  content: 'Want to Send?';
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
  letter-spacing: 6px;
  font-size: 1rem;
  font-weight: bold;
  transition: all 0.4s;
  color: #fff;
  text-decoration: none;
  background-color: transparent;
  text-transform: uppercase;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  font-size: 1.2rem;
  font-family: sans-serif;
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
  content: '';
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
  content: '';
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
  letter-spacing: 6px;
  font-size: 1.4rem;
  font-weight: bold;
  color: #4a0c52;
  text-transform: uppercase;
  width: 12rem;
  aspect-ratio: 3/1;
  text-decoration: none;
  overflow: hidden;
  position: relative;
  border: 3px solid #9a1aaa;
  font-size: 1.2rem;
  font-family: sans-serif;
  transition: all 0.4s;
}
.anim-6:hover {
  color: #fff;
}
.anim-6:hover:before {
  left: 0;
}
.anim-6:hover:after {
  top: 0;
}
.anim-6:before {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: 0;
  left: -25%;
}
.anim-6:after {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: -100%;
  left: 25%;
}
.anim-6 span {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.anim-6 span:hover:before {
  right: 0;
}
.anim-6 span:hover:after {
  bottom: 0;
}
.anim-6 span:before {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: 0;
  right: -25%;
}
.anim-6 span:after {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  bottom: -100%;
  right: 25%;
}

.anim-7 {
  letter-spacing: 6px;
  font-size: 1.4rem;
  font-weight: bold;
  color: #4a0c52;
  text-transform: uppercase;
  width: 12rem;
  aspect-ratio: 3/1;
  text-decoration: none;
  overflow: hidden;
  position: relative;
  border: 3px solid #9a1aaa;
  font-size: 1.2rem;
  font-family: sans-serif;
  transition: all 0.1s;
}
.anim-7:hover {
  color: #fff;
}
.anim-7:hover:before {
  top: 0;
}
.anim-7:hover:after {
  top: 0;
}
.anim-7:before {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: 100%;
  left: 0%;
  transition-delay: 0.2s;
}
.anim-7:after {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: -100%;
  left: 25%;
  transition-delay: 0.4s;
}
.anim-7 span {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.anim-7 span:hover:before {
  top: 0;
}
.anim-7 span:hover:after {
  bottom: 0;
}
.anim-7 span:before {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  top: -100%;
  right: 0%;
  transition-delay: 0.8s;
}
.anim-7 span:after {
  content: '';
  position: absolute;
  width: 25%;
  height: 100%;
  background-color: #9a1aaa;
  z-index: -1;
  transition: all 0.2s;
  bottom: -100%;
  right: 25%;
  transition-delay: 0.6s;
}

.anim-8 {
  text-decoration: none;
  text-transform: uppercase;
  color: #9a1aaa;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.1s;
  transition-duration: 1s;
}
.anim-8:before {
  content: '';
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
.anim-8:after {
  content: '';
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
.anim-8:hover {
  color: green;
  font-weight: bold;
}
.anim-8:hover:before {
  transform: rotateX(180deg);
}
.anim-8:hover:after {
  transform: rotateY(180deg);
}

.anim-9 {
  text-decoration: none;
  text-transform: uppercase;
  color: #fff;
  background-color: #9a1aaa;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
.anim-9:before {
  content: '';
  border-left: 2px solid #9a1aaa;
  border-top: 2px solid #9a1aaa;
  width: 20px;
  height: 20px;
  position: absolute;
  left: -4px;
  top: -4px;
  transition: all 0.4s;
}
.anim-9:after {
  content: '';
  border-right: 2px solid #9a1aaa;
  border-bottom: 2px solid #9a1aaa;
  width: 20px;
  height: 20px;
  position: absolute;
  right: -4px;
  bottom: -4px;
  transition: all 0.4s;
}
.anim-9:hover:before {
  width: 90%;
  height: 90%;
}
.anim-9:hover:after {
  width: 90%;
  height: 90%;
}

.anim-10 {
  text-decoration: none;
  color: #9a1aaa;
  border: 2px solid #9a1aaa;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
.anim-10:before {
  content: 'BB';
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  transition: all 2s;
}
.anim-10 span {
  transition: all 2s;
  transform-origin: center top;
}
.anim-10:hover {
  color: #fff;
}
.anim-10:hover:before {
  content: 'BB';
  background-color: #4a0c52;
}
.anim-10:hover span {
  transform: rotate(-360deg);
}

.anim-11 {
  text-decoration: none;
  color: #9a1aaa;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
}
.anim-11:before {
  content: '';
  border-left: 2px solid #9a1aaa;
  position: absolute;
  left: 0;
  top: 0;
  width: 0px;
  height: 0px;
  transition: all 0.2s;
}
.anim-11:after {
  content: '';
  border-top: 2px solid #9a1aaa;
  position: absolute;
  top: 0;
  right: 0;
  width: 0px;
  height: 0px;
  transition: all 0.2s;
}
.anim-11 span:before {
  content: '';
  border-right: 2px solid #9a1aaa;
  position: absolute;
  right: 0;
  bottom: 0;
  width: 0px;
  height: 0px;
  transition: all 0.2s;
}
.anim-11 span:after {
  content: '';
  border-bottom: 2px solid #9a1aaa;
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0px;
  height: 0px;
  transition: all 0.2s;
}
.anim-11:hover:before {
  width: 100%;
  height: 100%;
}
.anim-11:hover:after {
  width: 100%;
  height: 100%;
}
.anim-11:hover span:before {
  width: 100%;
  height: 100%;
}
.anim-11:hover span:after {
  width: 100%;
  height: 100%;
}

.anim-12 {
  text-decoration: none;
  color: #9a1aaa;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
}
.anim-12 span {
  z-index: -1;
  position: absolute;
  background-color: transparent;
  border: 2px solid #9a1aaa;
  left: 0;
  top: 0;
  width: calc(100% - 4px);
  height: calc(100% - 4px);
  transition: all 0.4s;
}
.anim-12 span:before {
  content: '';
  width: 8%;
  height: 500%;
  background-color: white;
  position: absolute;
  left: 50%;
  right: 50%;
  transform: translate(-50%, -50%) rotate(-60deg);
  transition: all 0.3s;
}
.anim-12:hover {
  color: white;
}
.anim-12:hover span:before {
  width: 120%;
  background-color: #9a1aaa;
  transform: translate(-50%, -50%) rotate(60deg);
}

.anim-13 {
  text-decoration: none;
  color: white;
  letter-spacing: 6px;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  background: transparent;
  border: none;
}
.anim-13:before {
  content: '';
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
.anim-13:after {
  content: '';
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
.anim-13:hover:before {
  left: 50%;
  top: 0;
  transform: skewx(0deg);
  background-color: blue;
}
.anim-13:hover:after {
  right: 50%;
  top: 0;
  transform: skewx(0deg);
  background-color: red;
}

.anim-14 {
  text-decoration: none;
  color: white;
  background-color: #c221d6;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.2s;
  border-radius: 2rem;
  letter-spacing: 6px;
}
.anim-14:before {
  content: '';
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
.anim-14:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}
.anim-14:hover:before {
  transform: scaleX(1.4) scaleY(1.6);
  opacity: 0;
}
.anim-14:active {
  transform: translateY(-1px);
  box-shadow: 0 5px 7px rgba(0, 0, 0, 0.2);
}

.anim-14 {
  text-decoration: none;
  color: white;
  background-color: #c221d6;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  transition: all 0.2s;
  border-radius: 2rem;
  letter-spacing: 6px;
}
.anim-14:before {
  content: '';
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

.anim-15 {
  text-decoration: none;
  color: black;
  background-color: transparent;
  border: 2px solid #9a1aaa;
  font-size: 1.2rem;
  font-family: sans-serif;
  width: 12rem;
  aspect-ratio: 3/1;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
  transition: all 0.7s;
  border-radius: 2rem;
  letter-spacing: 6px;
}
.anim-15:before {
  content: '';
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  border-top: 2rem solid green;
  border-bottom: 2rem solid green;
  border-right: 2rem solid transparent;
  transform: translateX(-100%);
  transition: all 0.7s;
}
.anim-15:after {
  content: '';
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  border-top: 2rem solid green;
  border-bottom: 2rem solid green;
  border-left: 2rem solid transparent;
  transform: translateX(100%);
  transition: all 0.7s;
}
.anim-15:hover:before {
  transform: translateX(0);
}
.anim-15:hover:after {
  transform: translateX(0);
}
</style>
