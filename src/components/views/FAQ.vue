<template>
  <div class="FAQ">
    <div class="background-gradient">
      <div class="white-pill column is-two-thirds-desktop is-10-mobile is-10-tablet">
        <img class="bk-woman-img-mobile is-hidden-desktop is-hidden-widescreen is-hidden-fullhd" src="../../assets/patterns/bg-pattern-mobile.svg" alt="">
        <img class="woman-img-mobile is-hidden-desktop is-hidden-widescreen is-hidden-fullhd" src="../../assets/images/illustration-woman-online-mobile.svg" alt="">
        <div class="columns">
          <div class="column left is-hidden-touch is-hidden-tablet-only">
            <div class="woman-img"></div>
            <img class="box-img" src="../../assets/images/illustration-box-desktop.svg" alt="">
          </div>
          <div class="column right">
            <div class="right-content">
              <h1 class="title-faq">FAQ</h1>
              <div class="collapse-container">
                <Collapse :collapses="collapses" :initial="isOpen"></Collapse>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Collapse from '../elements/Collapse.vue'

export default {
  name: 'FAQ',
  components: {
    Collapse
  },
  data () {
    return {
      isOpen: -1,
      collapses: [
        {
          title: 'How many team members can I invite?',
          text: 'No more than 2GB. All files in your account must fit your allotted storage space.'
        },
        {
          title: 'What is the maximum file upload size?',
          text: 'No more than 2GB. All files in your account must fit your allotted storage space.'
        },
        {
          title: 'How do I reset my password?',
          text: 'No more than 2GB. All files in your account must fit your allotted storage space.'
        },
        {
          title: 'Can I cancel my subscription?',
          text: 'No more than 2GB. All files in your account must fit your allotted storage space.'
        },
        {
          title: 'Do you provide additional support?',
          text: 'No more than 2GB. All files in your account must fit your allotted storage space.'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.FAQ {
  .background-gradient {
    width: 100vw;
    height: 100vh;
    background-image: linear-gradient(hsl(273, 75%, 66%), hsl(240, 73%, 65%));
    display: table-cell;
    vertical-align: middle;
  }
  .white-pill {
    height: 65vh;
    background-color: white;
    margin: auto;
    border-radius: 25px;
    box-shadow: 0px 22px 57px -22px rgba(77,77,77,1);
    -webkit-box-shadow: 0px 22px 57px -22px rgba(77,77,77,1);
    -moz-box-shadow: 0px 22px 57px -22px rgba(77,77,77,1);
    @media screen and (max-width: 1024px) {
      height: 73vh;
      margin-top: 70px;
    }
    .woman-img-mobile {
      min-width: 266px;
      position: fixed;
      top: 17%;
      left: 50%;
      transform: translate(-50%, -50%);
      margin-left: -15px;
    }
    .bk-woman-img-mobile {
      position: fixed;
      top: 24.5%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .left {
    height: 65vh;
    background-image: url("../../assets/patterns/bg-pattern-desktop.svg");
    // background-position: 120% 68%;
    background-position: -550px -290px;
    background-repeat: no-repeat;
    padding-left: 0;
    padding-right: 0;
    .woman-img {
      background-image: url("../../assets/images/illustration-woman-online-desktop.svg");
      height: 100%;
      background-repeat: no-repeat;
      // background-position: -280% 45%;
      background-position: -60px 60px;
    }
    .box-img {
      position: absolute;
      top: 44%;
      left: 10.3%;
      // top: 340px;
      // left: 165px;
    }
  }
  .right {
    height: 65vh;
    padding-left: 2em;
    padding-top: 3.5em;
    padding-bottom: 3.5em;
    .right-content {
      height: 100%;
      .collapse-container {
        max-height: 90%;
        overflow: auto;
      }
    }
    @media screen and (max-width: 1024px) {
      padding-left: 2em;
      padding-right: 2em;
    }
  }
  h1 {
    font-size: 2em;
    font-weight: bold;
  }
  p {
    font-size: 14px;
  }
  .title-faq {
    margin-bottom: 10px;
    @media screen and (max-width: 1024px) {
      margin-top: 80px;
      text-align: center;
    }
  }
}
</style>
