<template>
  <div class="FAQ">
    <div class="background-gradient">
      <div class="white-pill column is-three-fifths-desktop is-hidden-touch is-hidden-tablet-only">
        <div class="columns">
          <div class="column left"></div>
          <div class="column right">
            <div class="right-content">
              <h1 class="title-faq">FAQ</h1>
              <div class="collapse-container">
                <Collapse :collapses="collapses" :isOpen="isOpen"></Collapse>
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
  }
  .left {
    height: 65vh;
  }
  .right {
    height: 65vh;
    padding-top: 3.5em;
    padding-bottom: 3.5em;
    .right-content {
      height: 100%;
      .collapse-container {
        max-height: 90%;
        overflow: auto;
      }
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
  }
}
</style>
