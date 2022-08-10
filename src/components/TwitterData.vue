<template>
  <div>
   <button id="grid">Toggle </button>
    </div>
    
</template>

<script>
export default {
    // Mount will add Event listener //
  mounted() {
    this.show_tweet();
    let grid = document.getElementById(`grid`);
    grid.addEventListener(`click`, this.column_list);
  },

  methods: {
    // Displays data from the data  //
    show_tweet() {
      let box = document.getElementById(`box`);
      for (let i = 0; i < this[`data`].length; i++) {
        box[`innerHTML`] += `<div class="content_item">
            <h2> ${this[`data`][i][`user`]} </h2>
            <p>${this[`data`][i][`date`]}</p>
            <h2>${this[`data`][i][`tweet`]}</h2>
            </div>`;
      }
    },
    // Function will check for style property grid and auto flow and will convert them //
    column_list() {
      let box = document.getElementById(`box`);
     if(box[`style`][`gridAutoFlow`] === `column`){
        box[`style`][`gridAutoFlow`] =`row`;
     } else {
        box[`style`][`gridAutoFlow`] =`column`;
     }
    },
  },
// All the date for tweets: tweets,user name and date tweet was posted //
  data() {
    return {
      data: [
        {
          tweet: `Hello, have a nice day!`,
          user: `Hani`,
          date: `01-03-2002`,
        },
        {
          tweet: `Ramadan Mubarak!!`,
          user: `Siham`,
          date: `05-06-2014`,
        },
        {
          tweet: `Salaam!!`,
          user: `Maya`,
          date: `02-04-2013`,
        },
        {
          tweet: `Eid Mubarak!!`,
          user: `Hanad`,
          date: `09-02-2011`,
        },
      ],
    };
  },
};
</script>
<style scoped>
</style>