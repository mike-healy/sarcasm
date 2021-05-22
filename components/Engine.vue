<template>
  <form>
      <div>
          <label for="original">Your Text</label>
          <input v-model="input" type="text" id="original">
      </div>
      <div style="margin: 2rem 0;">
          <div class="output">{{ sarcasticize() }}</div>
      </div>
  </form>
</template>

<script>
export default {
    data() {
        return {
            input: 'Everyone is unique'
        }
    },

    methods: {
        sarcasticize() {
            let t = this.input.split('')
            let len = t.length
            let out = ''

            const u = c => c.toUpperCase()
            const l = c => c.toLowerCase()

            for (let i=0; i<len; i++) {
                let fn = (i%2 !== 0) ? u : l
                out += fn(this.input[i])
            }

            return out
        }
    }
}
</script>

<style>
form {
    padding: 2rem;
    margin: 0 12px;
    background: linear-gradient(30deg, #f09703, #f1e69d);
    color: #111;
    text-align: left;
    border-radius: 8px;
    box-shadow: -4px 4px 8px 8px rgba(0, 0, 0, 0.17);
}

label {
    display: block;
    margin-bottom: 4px;
    font-weight: 500;
}
input[type=text] {
    display: block;
    width: 100%;
    padding: 16px;
    background: #efefef;
    border-radius: 4px;
    color: #333;
}

div.output {
    background: #333;
    color: #fff;
    border-radius: 4px;
    border: 1px solid #787;
    padding: 16px;
    margin-top: 32px;
}
</style>